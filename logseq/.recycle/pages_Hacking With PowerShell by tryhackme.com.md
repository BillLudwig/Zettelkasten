title:: Hacking With PowerShell by tryhackme.com
author:: [[tryhackme.com]]
full-title:: "TryHackMe | Hacking With PowerShell"
category:: #articles
url:: https://tryhackme.com/room/powershell
tags:: #[[Powershell]]

- Highlights first synced by [[Readwise]] [[Nov 2nd, 2022]]
	- Powershell is the Windows Scripting Language and shell environment that is built using the .NET framework.This also allows Powershell to execute .NET functions directly from its shell. Most Powershell commands, called cmdlets, are written in .NET. Unlike otherscripting languages and shell environments, the output of these cmdlets are objects - making Powershell somewhat object oriented. This also means that running cmdlets allows you to perform actions on the output object
	- Get-Help displays information about a cmdlet
	- understand how exactly to use the command by passing in the -examples flag
	- The Pipeline(|) is used to pass output from one cmdlet to another
	- Get-Command gets all the cmdlets installed on the current Computer. The great thing about this cmdlet is that it allows for pattern matchinglikethefollowingGet-Command Verb-* or Get-Command *-Noun
	- When a cmdlet outputs a lot of information, you may need to sort it to extract the information more efficiently. You do this by pipe lining the output of a cmdlet to the Sort-Object cmdlet.