---
title: File Magic Numbers
date: 2021-06-07 19:30:00 -0700
tags: Computer Science
---

Magic numbers are a method of validating the type of file that is generally safer and more accurate than trusting file extensions. [Wikipedia has a list](https://en.wikipedia.org/wiki/List_of_file_signatures) for most common file types.

## Spoofing Magic Numbers

1. Check the initial filetype with `file filename`
2. Open the file in the texteditor of your choice.
   1.  Add a string of random characters to the top that is the same length as the HEX signature.
   2.  Save.
3. Open the file in `hexeditor` and you should see the characters you added first.
   1. Replace those character with the signature for the desired filetype.
   2. Save.
4. Verify the filetype has changed with `file filename`