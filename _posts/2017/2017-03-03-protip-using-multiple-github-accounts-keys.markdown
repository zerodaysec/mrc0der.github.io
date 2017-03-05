---
layout: "post"
title: "ProTip: Using Multiple Github Accounts & Keys"
date: "2017-03-03 07:03"
tags:
 - github
 - protip
---

Multiple SSH Keys settings for different github account

create different public key

create different ssh key according the article Mac Set-Up Git
```
$ ssh-keygen -t rsa -C "user1@gmail.com"
```
Please refer to github ssh issues for common problems.

for example, 2 keys created at:
```
~/.ssh/id_rsa_user1
~/.ssh/id_rsa_user2
```
then, add these two keys as following
```
$ ssh-add ~/.ssh/id_rsa_user1
$ ssh-add ~/.ssh/id_rsa_user2
```
you can delete all cached keys before
```
$ ssh-add -D
```
finally, you can check your saved keys
```
$ ssh-add -l
```
Modify the ssh config
```
$ cd ~/.ssh/
$ touch config
$ subl -a config
```
Then added
```
#user1 account
Host github.com-user1
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_rsa_user1

#user2 account
Host github.com-user2
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_rsa_user2
```
Clone your repo and modify your Git config

clone your repo `git clone git@github.com:user1/gfs.git gfs_user2`

cd gfs_user2 and modify git config
```
$ git config user.name "user2"
$ git config user.email "user2@gmail.com"
```

or you can set the global git config
```
$ git config --global user.name "user2"
$ git config --global user.email "user2@gmail.com"
```

then use normal flow to push your code
```
$ git add .
$ git commit -m "your comments"
$ git push
```
