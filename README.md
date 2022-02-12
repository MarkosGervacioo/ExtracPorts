# ExtracPorts
## Parsea la información más relevante de la captura grepeable de Nmap.

### Ejemplo
```bash
(root)~$ nmap -p- --open -T5 -v -n <ip> -oG allPorts
(root)~$ nmap -p- --open -sS --min-rate 5000 -vvv -n -Pn <ip> -oG allPorts
(root)~$ extracPorts allports
       │ File: allports
───────┼────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
   1   │ # Nmap 7.80 scan initiated Fri Feb  4 13:40:20 2022 as: nmap -p- --open -sS --min-rate 5000 -vvv -n -Pn -oG allports 10.10.11.111
   2   │ # Ports scanned: TCP(65535;1-65535) UDP(0;) SCTP(0;) PROTOCOLS(0;)
   3   │ Host: 10.10.11.111 ()   Status: Up
   4   │ Host: 10.10.11.111 ()   Ports: 22/open/tcp//ssh///, 80/open/tcp//http///
   5   │ # Nmap done at Fri Feb  4 13:40:38 2022 -- 1 IP address (1 host up) scanned in 17.63 seconds

```
