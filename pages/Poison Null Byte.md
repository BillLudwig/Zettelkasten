tags:: #InfoSec

- Also known as Null Byte Injection, the term poison null byte was originally coined by [Olaf Kirch](https://www.suse.com/c/author/okir/)
  id:: 636550fc-e9b2-4852-84d2-e1a4ae259691
- A null byte (or NULL terminator) is used in many languages to detect the end of a string. Systems that do not handle null bytes properly can be exploited by injecting a null byte to get around sanity checks in file names.
- Common attacks using this technique are [LFI/RFI Injection](https://billludwig.me/posts/local-remote-file-inclusion/) or bypassing file extension checks.
- ## Example:
	- `$whatever = addslashes($_REQUEST['whatever']); include("/path/to/program/" . $whatever . "/header.htm")`
	- `http://vuln.example.com/phpscript.php?whatever=../../../etc/passwd%00`
- URL Escaping:
	- The null byte `%00` must be url encoded to `%2500` for use in a web application.
- ## References:
	- [Hacker Recipes: Null-byte Injection](https://www.thehacker.recipes/web/inputs/null-byte-injection)
	-