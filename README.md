# ExtracPorts
## Parsea la información más relevante de la captura grepeable de Nmap.
### Debemos de tener instalada la herramiento xclip
```bash
(root)~$ sudo apt install xclip
```
### Escaneamos una maquina de HackTheBox con la IP:10.10.11.111
### Haciendo un escaneo bastante rápido con Nmap. Una vez terminado, lanzamos el extracPorts seguida del nombre del archivo: 
```bash
(root)~$ nmap -p- --open -T5 -v -n <ip> -oG allPorts    (opción 1)
(root)~$ nmap -p- --open -sS --min-rate 5000 -vvv -n -Pn <ip> -oG allPorts (Opción 2)
(root)~$ cat allPort


# Nmap 7.80 scan initiated Fri Feb  4 13:40:20 2022 as: nmap -p- --open -sS --min-rate 5000 -vvv -n -Pn -oG allports 10.10.11.111
# Ports scanned: TCP(65535;1-65535) UDP(0;) SCTP(0;) PROTOCOLS(0;)
Host: 10.10.11.111 ()	Status: Up
Host: 10.10.11.111 ()	Ports: 22/open/tcp//ssh///, 80/open/tcp//http///
# Nmap done at Fri Feb  4 13:40:38 2022 -- 1 IP address (1 host up) scanned in 17.63 seconds
```
  
```bash
(root)~$ extracPorts allPorts

   [*] Extracting information...
   
       [*] IP Address: 10.10.11.111
       [*] Open Ports: 22,80
   
   [*] Ports copied to clipboard
```


### Y nos da la información mas importante del archivo **allports**, y asi mismo nos copia los puertos en la Clipboard
