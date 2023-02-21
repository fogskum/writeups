# LazyAdmin

This is an easy box from TryHackMe. It has two flags - user and root.

## Enumeration

We start by scanning for open ports:

```console
foo@bar$ nmap -sC -sV -oN nmap/init <target_ip>
```
```
-sC for non-intrusive default scripts
-sV for version detection
-oN for output as normal format
```

todo: add result

We can we SSH on port 22 and Apache running on port 80.
