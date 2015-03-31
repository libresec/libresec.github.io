---
layout: post
title:  "git cheatsheat"
date:   2015-03-30 00:01:30
categories: cheatsheats
---

A quick cheatcheet for common git commands

******************************************

#### **new repo**
    1. Create repo:
        git init
    2. Add all files in directory:
        git add .
    3. Commit changes with message:
        git commit -m "message"
    4. Add remote repo:
        git remote add origin git@<host>:repo.git
    5. Push to remote server: 
        git push -u origin master

#### **reset to most recent commit**
    git reset --hard

#### **set name/email**
You can configure an individual repo to use a specific user / email address.

    git config user.name "Your Name Here"
    git config user.email your@email.com


#### **set global name/email**
The default user / email is configured in your ~/.gitconfig

    git config --global user.name "Your Name Here"
    git config --global user.email your@email.com

#### **nuke and restart**
This will overwrite everything. Be careful.

    1. Delete the .git directory locally. 
    2. Recreate the git repostory
        $ cd <project-directory>
        $ git init
        $ <add some files>
        $ git add .
        $ git commit -m 'commit message'
    3. Push to remote server, overwriting. `
        git remote add origin <url>
        git push --force

