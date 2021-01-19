---
title:  Exclude "permission denied" error messages from `find` Command
date:   2021-01-19 12:00:00 -0700
tags: [Linux]
---

`find / -name filename 2>$1 | grep -v "Permission denied"`

This command combines stderr and stdout then uses grep with the inversion `-v` flag to find everything except Permission denied responses.