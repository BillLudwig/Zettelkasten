---
title: Linux File Permissions
date: 2021-06-06 17:35:00 -0700
tags: Linux
---

## Common Commands

* View permissions with `ls -l`
* Change permissions with explicit permissions `chmod [u/g/a/o][+/-][r/w/x] filename`
* Change permissions using binary `chmod 421 filename` where 4=owner, 2=group, 1=all
* Change owners with `chown user:group filename`

## Permission Groups

* (u) Owner
* (g) Group
* (a) All Users
* (o) Other (only used when explicitly defining permissions)

## Permissions

* (r) Read: *Binary 4*
* (w) Write: *Binary 2*
* (x) Execute: *Binary 1*

## Special Permissions

* _ No special permissions
* d Directory
* l Symbolic link
* s setuid/setgid
* t sticky bit

## Setuid/Setgid Special Permissions

This special permission tells the system to execute as the owner instead of as the current user. Setting this is a security vulnerability and is part of many reverse shell exploits.  To set run `chmod g+s filename`.

## Sticky Bit Special Permission

This special permission, when set on a directory, prevents anyone but the owner from renaming or deleting. `chmod +t directory`