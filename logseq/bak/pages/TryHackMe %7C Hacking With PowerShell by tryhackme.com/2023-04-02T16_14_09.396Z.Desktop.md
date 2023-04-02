title:: TryHackMe | Hacking With PowerShell by tryhackme.com
author:: [[tryhackme.com]]
full-title:: "TryHackMe | Hacking With PowerShell"
category:: #articles
url:: https://tryhackme.com/room/powershell
tags:: #[[powershell]]

- [[Highlights]] first synced by [[Readwise]] [[November 2nd, 2022]]
	- Powershell is the Windows Scripting Language and shell environment that is built using the .NET framework.This also allows Powershell to execute .NET functions directly from its shell. Most Powershell commands, called cmdlets, are written in .NET. Unlike otherscripting languages and shell environments, the output of these cmdlets are objects - making Powershell somewhat object oriented. This also means that running cmdlets allows you to perform actions on the output object
	- Get-Help displays information about a cmdlet
	- understand how exactly to use the command by passing in the -examples flag
	- The Pipeline(|) is used to pass output from one cmdlet to another
	- Get-Command gets all the cmdlets installed on the current Computer. The great thing about this cmdlet is that it allows for pattern matchinglikethefollowingGet-Command Verb-* or Get-Command *-Noun
	- When a cmdlet outputs a lot of information, you may need to sort it to extract the information more efficiently. You do this by pipe lining the output of a cmdlet to the Sort-Object cmdlet.
- [[TryHackMe | Hacking With PowerShell by tryhackme.com]] #Dev/Powershell #Training
  id:: 636359b8-068f-41a7-8581-57ae12ca94d4
	- Count Cmdlets: `Get-Command -CommandType Cmdlet`
	- See if Path Exists `Test-Path -Path {path}`
	- Decode Base64 encoded file `certutil -decode "C:\Users\Administrator\Desktop\b64.txt" decode.txt`
- [[TryHackMe | Hacking With PowerShell by tryhackme.com]] #Dev/Powershell #Training
  id:: 6364aa87-9d8d-43ce-8614-ee0c6b5f899a
	- [Comparison Operators](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_comparison_operators?view=powershell-7.2&viewFallbackFrom=powershell-6)
	  id:: 63653393-afc5-402a-931d-4edc0c3a3e8d
		- String comparisons are case-insensitive unless you use the explicit
		  case-sensitive operator. To make a comparison operator case-sensitive, add a
		   `c`  after the  `-` . For example,  `-ceq`  is the case-sensitive version of  `-eq` .
		  To make the case-insensitivity explicit, add an  `i`  after  `-` . For example,
		   `-ieq`  is the explicitly case-insensitive version of  `-eq`
		- When the input of an operator is a scalar value, the operator returns a
		  **Boolean** value. When the input is a collection, the operator returns the
		  elements of the collection that match the right-hand value of the expression.
		  If there are no matches in the collection, comparison operators return an empty
		  array. For example:
	- #Training completed - do not recommend.