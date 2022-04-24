# Enumeration

{% hint style="warning" %}
This site is still under construction and aims to replace the [ToolBox](https://www.d3vyce.fr/toolbox/) page of my Blog.
{% endhint %}

On this page, you will find different tools allowing the enumeration of machine, web site, ...

## FFUF

[Wordlists](http://ffuf.me/wordlists)



Directory Scan

```
ffuf -c -u http://[IP]/FUZZ -w common.txt -recursion -recursion-depth 2
```

Subdomain Scan

```
ffuf -c -u http://[IP] -w subdomains.txt -H "Host: FUZZ.[IP]" -fw [WORD]
```

Parameter Scan

```
ffuf -c -u http://[IP]%FUZZ -w parameters.txt
```



## Nmap

[Nmap documentation](https://linux.die.net/man/1/nmap)\
[Nmap script list](https://nmap.org/nsedoc/)



Basic Scan

```
nmap -sV -T4 -Pn [IP]
```

UDP Scan

```
sudo nmap -sU --min-rate 5000 [IP]
```

SMB Scan

```
nmap -p 445 --script=smb-enum-shares.nse,smb-enum-users.nse [IP]
nmap -p445,135,139 --script="safe or smb-enum-*" [IP]
```

RPC Scan

```
nmap -p 111 --script=nfs-ls,nfs-statfs,nfs-showmount [IP]
```

