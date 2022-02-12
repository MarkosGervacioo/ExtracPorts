# ExtracPorts
## Parsea la información más relevante de la captura grepeable de Nmap.

### Ejempl
### (root)~$ nmap -p- --open -T5 -v -n <ip> -oG allPorts
### (root)~$ nmap -p- --open -sS --min-rate 5000 -vvv -n -Pn <ip> -oG allPorts
### (root)~$ extracPorts allports
