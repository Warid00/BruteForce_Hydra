# BruteForce_Hydra

Target: http://testasp.vulnweb.com/Login.asp?RetURL=%2FDefault%2Easp%3F
Login name: admin

Command: 
## hydra -l admin -P /usr/share/wordlists/rockyou.txt testasp.vulnweb.com http-post-form "/Login.asp?RetURL=%2FDefault%2Easp%3F:tfUName=^User^&tfUPass=^PASS^:S=logout" -vV -f

what the command does:
Using **hydra**. **-l admin** = using admin as login name. **-P /usr/share/wordlists/rockyou.txt** = Using rockyou.txt dictionary and where it is located. **testasp.vulnweb.com** = IP ADDRESS. **http-post-form** = http module. **"/Login.asp?RetURL=%2FDefault%2Easp%3F:tfUName=^User^&tfUPass=^PASS^:S=logout"** = 3parts, part 1 **/Login.asp?RetURL=%2FDefault%2Easp%3F:** = URL, part 2 **tfUName=^User^&tfUPass=^PASS^:** = where to input username and password, part 3 **S=logout** = find whatever is in the page after succesfully logged in. **-vV** 2 part, part 1 **v** = Verbose mode detailed information or printout during the execution of a program, part 2 **V** = show login:pass for each attempt. **-f** = Terminate program if pair login:password is found.

How hydra is build:

[-l LOGIN|-L FILE] [-p PASS|-P FILE] [-u] [-f] [IP ADDRESS] [-s PORT] [MODULE] [URL]

1. [-l LOGIN|-L FILE]: Using login name or dictionary 
2. [-p PASS|-P FILE]: using password or dictionary
3. [-u]: every user  
4. [-f]: stop on first name
5. [IP ADDRESS]:
6. [-s PORT]: Target Port
7. [MODULE]: Which section (ssh, http, etc.)
8. [URL]:




