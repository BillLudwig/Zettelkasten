---
title: Gobuster URI Discovery
date: 2021-06-07 19:35:00 -0700
tags: [Pentesting]
---

## Finding Directories

`gobuster dir -u http://target.website -w path/to/wordlist`


Source: [Gobuster](https://tools.kali.org/web-applications/gobuster)

## Finding Files by File Extension

The `-x` switch will append every word in the wordlist with the file extensions provided. Can be really useful if you are looking to see where an uploaded file is saved.

`gobuster dir -u http://target.website -x jpg,gif,etc -w path/to.wordlist`
