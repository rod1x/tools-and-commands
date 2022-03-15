# NMAP

## Basic and efective scan
    sudo nmap -sS -sCV -Pn -p- <target> -oN nmap.txt

-sS    →  TCP SYN

-sV    →  Probe open ports to determine service

-sC    →  Scan using the default set of scripts

-Pn    →  Treat all hosts as online -- skip host discovery

-p-    →  Scan all ports

-oN    →  Save the ouput of the scan in a file

## SSH Brute Force credentials
    nmap -p 22 --script ssh-brute --script-args userdb=username.txt,passdb=password.txt <target>

## Stealth Scan

    nmap -sS <target>

Only Open Ports and Banner Grab

    nmap -n -Pn -sS <target> --open -sV

Stealth scan using FIN Scan 

    nmap -sF <target>

## Agressive scan

Without Ping scan, no dns resolution, show only open ports all and test All TCP Ports

    nmap -n -Pn -sS -A <target> --open -p-

Nmap verbose scan, runs syn stealth, T4 timing, OS and service version info, traceroute and scripts against services

    nmap –v –sS –A –T4 <target>

## OS FigerPrint

    nmap -O <target>

## Quick Scan

    nmap -T4 -F <target>

## Quick Scan Plus

    nmap -sV -T4 -O -F --version-light <target>


## Search NMAP scripts

    ls /usr/share/nmap/scripts/ | grep ftp

## Enumerate ciphers

    nmap --script ssl-unum-ciphers -p 443 <target>


