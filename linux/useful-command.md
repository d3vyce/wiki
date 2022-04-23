# Useful Command

## Network

{% hint style="info" %}
**Good to know:** a good vision statement shows the long-term goals of the company without getting too deep into strategy, implementation, or product specifics.
{% endhint %}

Copy file over SSH

```
scp [FILE] [user]@[IP]:[folder]
```

SSH port forwarding

```
ssh -L [local_port]:127.0.0.1:[target_port] -N [target_user]@[target_ip]
```

Open port

```
nc -nlvp [port]
```

File server

```
python3 -m http.server 8080
```

Download from file server

```
wget [ip]:81/[file]
```

List open port

```
netstat -lntu
```

Telnet with user

```
telnet [IP] -l [user]
```

## Pentest

Search exploit

```
searchsploit [NAME]
```

Download exploit

```
searchsploit -x [CODE] > [OUTPUT FILE]
```

## File Manipulation

File listing including hidden

```
ls -la
```

Size of folder/file

```
du -sh [folder]
```

Find file

```
find / -name [name] 2>/dev/null
```

## String Manipulation

Decode Base64

```
base64 -d <<< [string]
```

Encode Base64

```
base64 <<< [string]
```

Decode Hexa

```
xxd -r -p <<< [string]
```
