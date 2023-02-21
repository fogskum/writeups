# LazyAdmin

This is an easy box from TryHackMe. The goal is to find user and root flags.

## Enumeration
We start by scanning for open ports:

```console
foo@bar$ sudo nmap -sC -sV -oN nmap/init <target_ip>
```
```
-sC for non-intrusive default scripts
-sV for version detection
-oN for output as normal format
```

**TODO: add result**

We can we SSH on port 22 and Apache running on port 80. Let's navigate to the site using the browser to take a look. We can see that the site is using SweetRice CMS.

**TODO: add screenshot**

Let's enumeration for hidden files and directories using e.g., gobuster:
```console
foo@bar$ gobuster dir -u http://<target_ip> -w /usr/share/wordlists/dirb/common.txt
```
**TODO: add result**

The only interesting here is the /content folder. Let go there and have a look.

**TODO: add result**

We run gobuster again on the /content folder:
```console
foo@bar$ gobuster dir -u http://<target_ip>/content -w /usr/share/wordlists/dirb/common.txt
```



