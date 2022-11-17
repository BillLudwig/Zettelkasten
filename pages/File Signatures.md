tags:: #CompSci

- File signatures (aka Magic Numbers) are a method of validating the type of file that is generally safer and more accurate than trusting file extensions. [Wikipedia has a list](https://en.wikipedia.org/wiki/List_of_file_signatures) for most common file types.
- ## Spoofing File Signatures
	- Check the initial filetype with `file filename`
	  Open the file in the texteditor of your choice.
	  * Add a string of random characters to the top that is the same length as the HEX signature.Save.
	  * Save
	  Open the file in `hexeditor` and you should see the characters you added first.
	  * Replace those characters with the signature for the desired filetype.
	  * Save.
	  Verify the filetype has changed with `file filename`