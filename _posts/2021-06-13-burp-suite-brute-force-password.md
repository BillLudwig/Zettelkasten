---
title: Using Burp Suite to Brute Force Password
date: 2021-06-13 19:00:00 -0700
tags: [Pentesting, Burp Suite]
---

1. Intercept the form submit with Burp Suite and `Send to Intercepter`
2. Switch to Intruder and the Positions tab.
   1. Make sure attack type is set to `Sniper`
   2. Clear the automatically hilighted fields.
   3. Hiligh the fields that will be attacked and hit the `Add` button.
3. Switch to the payload tab.
   1. Load a wordlist
4. Hit the `Start Attack` button.
5. Go make a sandwich or watch Netflix because this will take a while.