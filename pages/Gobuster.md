tags:: #pentesting
url:: https://www.kali.org/tools/gobuster/

- Gobuster is a tool to brute force URI iteration for subdomain, directories, and file discovery.
- ## Usage
	- ### Finding Directories
		- `gobuster dir -u http://target.website -w path/to/wordlist`
	- ### Finding Files By Extension
		- The `-x` switch will append every word in the wordlist with the file extensions provided. Can be really useful if you are looking to see where an uploaded file is saved.
		- `gobuster dir -u http://target.website -x jpg,gif,etc -w path/to.wordlist`
-