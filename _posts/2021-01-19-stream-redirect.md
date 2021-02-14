---
title:  2>$1 Explained
date:   2021-01-19 12:00:00 -0700
tags: [Linux]
---

The syntax `2>$1` is used to redirect `stderr` into the stdout stream which is confusing until you break it down to understand what is happening. 
Understanding the [Linux File Descriptors]({% post_url 2021-01-19-linux-file-descriptors %}) makes this less opaque as well.

1. The `>` character redirects stdout and is the same as `1>`. *Example `echo hello > hello.txt`*
2. Therefore `2>` redirects stderr.
3. The `>&` syntax redirect a stream to another [Linux File Descriptor]({% post_url 2021-01-19-linux-file-descriptors %})
4. Therefore `2>$1` breaks down to mean take stream 2 and redirect it into stream 1 (stderr into stdout).
5. It could also be reversed to `1>&2` to redirect stdout into stderr.