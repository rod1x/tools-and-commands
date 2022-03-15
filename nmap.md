# NMAP

## Basic and efective scan
    sudo nmap -sS -sCV -Pn -p- 10.10.189.225 -oN nmap.txt

-sS    →  TCP SYN

-sV    →  Probe open ports to determine service

-sC    →  Scan using the default set of scripts

-Pn    →  Treat all hosts as online -- skip host discovery

-p-    →  Scan all ports

-oN    →  Save the ouput of the scan in a file

## SSH Brute Force credentials
    sudo nmap -p 22 --script ssh-brute --script-args userdb=users.txt,passdb=pass.txt \ --script-args ssh-brute.timeout=4s <target>

### Detecting Live Hosts
Only Ip's

`nmap -sn -n $netw | grep for | cut -d" " -f5`

### Stealth Scan

`nmap -sS $ip`

Only Open Ports and Banner Grab

`nmap -n -Pn -sS $ip --open -sV`

Stealth scan using FIN Scan 

`nmap -sF $ip`

### Agressive scan

Without Ping scan, no dns resolution, show only open ports all and test All TCP Ports

`nmap -n -Pn -sS -A $ip --open -p-`

Nmap verbose scan, runs syn stealth, T4 timing, OS and service version info, traceroute and scripts against services

`nmap –v –sS –A –T4 $ip`

### OS FigerPrint

`nmap -O $ip`

### Quick Scan

`nmap -T4 -F $netw`

### Quick Scan Plus

`nmap -sV -T4 -O -F --version-light $netw`

### output to a file

`nmap -oN nameFile -p 1-65535 -sV -sS -A -T4 $ip`

### output to a file Plus

`nmap -oA nameFile -p 1-65535 -sV -sS -A -T4 $netw`

### Search NMAP scripts

`ls /usr/share/nmap/scripts/ | grep ftp`

### Enumerate ciphers

`nmap --script ssl-unum-ciphers -p 443 $ip`


