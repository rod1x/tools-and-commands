# enum4linux

## Basic and efective scan
    enum4linux <target>
    
 -a           Do all simple enumeration (-U -S -G -P -r -o -n -i). This option is enabled if you don't provide any other options.          
 -h        Display this help message and exit
 -r        enumerate users via RID cycling
 -R range  RID ranges to enumerate (default: 500-550,1000-1050, implies -r)
 -l        Get some (limited) info via LDAP 389/TCP (for DCs only)
 -s file    brute force guessing for share names
 -k user   User(s) that exists on remote system (default: administrator,guest,krbtgt,domain admins,root,bin,none)
              Used to get sid with "lookupsid known_username"
    	        Use commas to try several users: "-k admin,user1,user2"
 -o        Get OS information
 -i        Get printer information
 -w wrkg   Specify workgroup manually (usually found automatically)
 -n        Do an nmblookup (similar to nbtstat)
 -v        Verbose.  Shows full commands being run (net, rpcclient, etc.)
 -A        Aggressive. Do write checks on shares etc
