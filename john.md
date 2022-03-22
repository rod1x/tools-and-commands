# John

## Transform SSH-KEYs into SSH-HASH
    python /usr/share/john/ssh2john.py <ssh.txt>  > sshhash.txt

## Brake the SSH-HASH into PlainText Password
    john --wordlist=rockyou.txt sshhash.txt
