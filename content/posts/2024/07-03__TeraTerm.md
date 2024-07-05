---
title: "Tera Term Learning Note"
date: 2024-07-05T22:11:36+07:00
slug: /Tera-Term-Note/
description: Exploring the beauty of macro which makes repetitive tasks easier than ever.
image: images/matt-artz-qJE5Svhs2ek-unsplash.jpg
caption: Photo by Matt Artz on Unsplash.
categories:
  - tools
tags:
  - scripts
  - TTL
  - macro
draft: false
---

Tera Term and PuTTY are both popular terminal emulation program used for remote access to computers or network devices. Both could support various protocols (Telnet, SSH and serial connections). However, with the support of streamlining command sequences in its own macro, Tera Term turns out to be much more powerful in terms of automation than PuTTy.


## Why TeraTerm?

- Open-source and Free
- Multiple Protocol Support
- Lightweight and Fast  
  - Mininum system resources used and offer fast performances
- Macro scripting  
  - Create custom workflows to handle repetitive tasks
- Session logging  
  - Capture all the input and output for further analysis or reference

## How to use TeraTerm ?

1. Open Tera Term
    - Launch the Tera Term application on computer
2. Establish a connection
3. Open Macro from Macro menu
4. Run the Macro

## Macro with Tera Term Language (TTL)

### Control Commnads

  - ***goto \<label\>***  
    Moves control to the next line of the \<label\>
  - ***while \<expression\>***  
    ...  
    ...  
    ***endwhile***  
    Repeats the statement while expression is non-zero
  - ***if \<expression 1\> then***  
    ...  
    ***\[elseif \<expression 2\> then\]***  
    ...  
    ***\[elseif \<expression 3\> then\]***  
    ...  
    ***\[else\]***  
    ...  
    ***endif*** 

```TTL=
; Connect to the remote system via Telnet
connect '10.113.30.31:7003 /nossh /T=1'
sendln ''
wait '[CommonDiags]->' 'LOADER' 'garuda>'
if result = 1 then
  goto powercycle
elseif result = 2 then
  goto loader
elseif result = 3 then 
  goto garuda
endif

:powercycle
  sendln 'powercycle'
  wait 'LOADER'
  goto netboot
:loader
  sendln ''
  goto netboot
:garuda
  sendln 'exit'
  wait '[CommonDiags]->'
  goto process

:netboot
sendln 'ifconfig e0M -auto'
wait 'LOADER'
; could work with extra logs
;sendln "boot -bzimage http://.../vmlinuz"
```

 ### Communication Commands

  - ***sendln \<data\>***  
    Send characters followed by a new-line character
  - ***wait \<string1\> \[\<string2\> ...\]***  
    Pauses until one of the characters is received from the host or until the timeout occurs  
    1 -> \<string1\> is received  
    2 -> \<string2\> is received
  - ***settitle \<title\>***  
    Changes the title text of Tera Term



```TTL=
while i < 10
  i = i+1
    sprintf2 msg "loop cnt = %d" i
    settitle msg
    sendln 'diag -d fc -p fcdev -t sfpread -b 1a a0 28 38'
  wait 'Success' 'Error' '28: 00 00'
  if result != 1 then 
    goto error
  endif
    sendln 'diag -d fc -p fcdev -t sfpread -b 1b a0 28 38'
  wait 'Success' 'Error' '28: 00 00'
  if result != 1 then 
    goto error
  endif
    sendln 'diag -d fc -p fcdev -t sfpread -b 1c a0 28 38'
  wait 'Success' 'Error' '28: 00 00'
  if result != 1 then 
    goto error
  endif
    sendln 'diag -d fc -p fcdev -t sfpread -b 1d a0 28 38'
  wait 'Success' 'Error' '28: 00 00'
  if result != 1 then 
    goto error
  endif
endwhile
```

- ***inputbox \<message\> \<title\>***  
  Display \<message\> in the dialog box with the title \<title\>  
  Return value will store in system variable **\<inputstr\>**  
- ***tolower \<strvar\> \<string\>***  
  Convert all of the alphaetic characters in \<string\> to lower-case and returns it in the string variable \<strvar\>  
- ***toupper \<strvar\> \<string\>***  
  Convert all of the alphaetic characters in \<string\> to upper-case and returns it in the string variable \<strvar\>  
- ***strcompare \<string1\> \<string2\>*** 
  Compare two strings  
    \<string1\> < \<string2\> --> returns -1  
    \<string1\> = \<string2\> --> returns 0  
    \<string1\> > \<string2\> --> returns 1  

```TTL=
; Prompt the user for input
inputbox 'Enter platform name:' 'plat'
tolower plat inputstr

connect '10.113.30.31:7003 /nossh /T=1'
sendln ''

wait 'LOADER' '[CommonDiags]->' 'CL-ROOT#'

if result != 1 then
  goto powercycle
else then
  goto netboot
endif

:powercycle
  sendln 'powercycle'
  wait 'LOADER'
  goto netboot

:netboot
; Perform actions based on the input platform
strcompare plat 'apollo'
if result == 0 then
  ;sendln 'echo platform apollo'
    sendln 'ifconfig e0M -auto'
endif
```

### For SSH Connection Setup

- ***\/T=\<telnet flag\>***  
  \/T=1 Enable telnet  
  \/T=0 Disable telnet
- ***\/P=\<TCP port#\>***
- ***\/C=\<serial port#\>***  
  \/C=1 COM1  
  \/C=2 COM2  
  ...  
  \/C=256 COM256

```TTL=
; Connect using SSH
connect '/ssh username@hostname_or_ip'
waitfor 'login:'
sendln 'username'
waitfor 'Password:'
sendln 'user_password'
```
