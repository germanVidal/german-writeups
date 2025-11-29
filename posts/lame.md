---
layout: default
title: "Lame – HackTheBox"
---

# Lame – HackTheBox

## 🧭 Scan inicial

![Nmap](/Lame/Lame (10).png)

Puertos detectados:

- 21 FTP  
- 22 SSH  
- 139 SMB  
- 445 SMB  

## 🔍 Enumeración

```bash
enum4linux -a 10.129.6.222
