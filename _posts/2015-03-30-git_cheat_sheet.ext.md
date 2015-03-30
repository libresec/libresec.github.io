---
layout: post
title:  "Git Cheatsheat"
date:   2015-03-30 00:09:02
categories: git, cheatsheats
---

Git Commands
------------

New repo

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

You can configure an individual repo to use a specific user / email address.

    git config user.name "Your Name Here"
    git config user.email your@email.com

The default user / email is configured in your ~/.gitconfig

    git config --global user.name "Your Name Here"
    git config --global user.email your@email.com

Completely Nuke and Restart

    1. Delete the .git directory locally. 

    2. Recreate the git repostory
    
        $ cd (project-directory)
        $ git init
        $ (add some files)
        $ git add .
        $ git commit -m 'Initial commit'

    3. Push to remote server, overwriting. Remember you're going to mess everyone else up doing this... you better be the only client.
        
        git remote add origin <url>
        git push --force

