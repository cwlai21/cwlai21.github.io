---
title: "Git and GitHub Learning Note"
date: 2024-08-12T14:15:05+07:00
slug: /git-github/
description: The very First Step before becoming a Contributor at Work and Tech World.
image: images/roman-synkevych-wX2L8L-fGeA-unsplash.jpg
caption: Photo by Roman Synkevych on Unsplash
categories:
  - tools
tags:
  - git
  - github
  - Version Control System (VCS)
draft: true
---
![](/images/git_intro_file_status.png)

## Create Repository

Keyword: Modified Committed Staged

- git init  
  The very first step to start version control in this folder  
  .git folder will be created, the key to handle version control
- git clone <repoitory_url>
- Common commands  
|  Commands  | Description | Note |
|  ----  | ----  | ----  | 
| git status | check current status | |
| git add | add untracked or changes but not staged files in staging area | git add . : add all files |
| git commit | commit files from staging area to Repository (local database)  | git commit --amend: modify previous commit  git commit -m "description for this submit" |
| git log | check commit history | git log --oneline --graph  |
| git diff | show file differences | |
| git relog| show commits | git log -g : display the same result |

### git reset (goto)
|  --soft  | --mixed | --hard |
|  ----  | ----  | ----  | 
| seems to only move the head position, nothing changed | Remove changes in staging area but keep those in working directory(default setting) | both working directory and staging area are removed |
| files in commit back to previous commit | files in commit back to previous commit and so does files in staging area | discard all files in commit and back to previous commit |

Illustration for git status and git diff in GUI interface SourceTree
![](/images/git_status.png)

Illustration for git log with extra parameters
![](/images/git_log.png)

### git checkout

- Create a new branch and switch branch
  - git checkout -b <branch_name>
    - git branch <branch_name> + git checkout <branch_name> 
  - git rebase <master_branch>  
    - diff the code changes and store in temporary files
  - git checkout <master_branch>  
    - switch back to main branch
  - git merge <branch_name> 
    - merge the diff
  - git branch -d <branch_name> 
    - delete branch after commits are merged back to main branch

- Discard changes in working directory
  - git checkout - - <file_name>
  - git reset HEAD <file_name>
    - restore "status" (commited, staged, untracked) of the file not content