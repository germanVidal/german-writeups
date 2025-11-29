# Lame

Scan: 

![image.png](image.png)

Puertos:

- 21 FTP
- 22 SSH
- 139
- 445 SMB

Sabiendo que estamos contra SMB ejecutamos Enun4linux

```jsx
enum4linux -a 10.129.6.222
```

Este nos da información super importante de esta maquina las cuales son: Usuarios,Grupos,Versiones,Compartidos,Dominios etc..

![image.png](image%201.png)

![image.png](image%202.png)

![image.png](image%203.png)

## Dentro de tmp no habia nada importante ya que no iba por ahi.

![image.png](image%204.png)

# Explotación

Buscamos  —> How to exploit Samba 3.0.20

Encontre el siguiente exploit (**Samba "username map script" Command Execution CVE-2007-2447)**

<aside>
💡

This module exploits a command execution vulnerability in Samba
versions 3.0.20 through 3.0.25rc3 when using the non-default
"username map script" configuration option. By specifying a username
containing shell meta characters, attackers can execute arbitrary
commands.

</aside>

Sabiendo esto abrimos MsfConsole buscando asi el exploit para samba < 3.0.2

![image.png](image%205.png)

Ejecutamos:

![image.png](image%206.png)

Configuramos las opciones de este exploit:

![image.png](image%207.png)

### Confirmamos con Ip -a que estamos dentro de la maquina:

![image.png](image%208.png)

Obtenemos las flags:

![image.png](image%209.png)