tags:: Linux

- The syntax `2>$1` is used to redirect `stderr` into the stdout stream which is confusing until you break it down to understand what is happening. Understanding the Linux File Descriptors makes this less opaque as well.
- 1. The `>` character redirects stdout and is the same as `1>`. _Example `echo hello > hello.txt`_
  2. Therefore `2>` redirects stderr.
  3. The `>&` syntax redirect a stream to another Linux File Descriptor
  4. Therefore `2>$1` breaks down to mean take stream 2 and redirect it into stream 1 (stderr into stdout).
  5. It could also be reversed to `1>&2` to redirect stdout into stderr.