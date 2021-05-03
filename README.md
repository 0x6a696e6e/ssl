# ssl
$ Socat

┌──(kali㉿kali)-[~/ssl]
└─$ openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -days 365


┌──(kali㉿kali)-[~/ssl]
└─$ cat * > name.pem

┌──(kali㉿kali)-[ssl]
└─$ socat TCP-LISTEN:51000,fork,reuseaddr OPENSSL:remotehost:51000,cafile=name.pem,verify=0



