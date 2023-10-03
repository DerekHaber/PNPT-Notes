Stages:
1. Reconnaissance - Active vs Passive
2. Scanning & Enumeration -Nmap, Nessus, Nikto
3. Exploitation
4. Maintain access
5. Cover tracks

Reconnaissance:
TAKE SCREENSHOTS OF DISCLOSED INFORMATION
	Passive:

	Location info, Employee information (name, title, number, manager, badge photo or number, etc)
	1. Target Validation - WHOIS, nslookup, dnsrecon
	2. Subdomain search - Google Fu, dig, nmap, subfinder, Bluto, crt.sh
	3. Fingerprinting - Nmap, wappalyzer, WhatWeb, BuiltWith, Netcat
	4. Data Breaches - HaveIBeenPwned, Breach-Parse, WeLeakInfo


	Active:

	arp-scan -l OR netdiscover -r 10.0.2.0/24

	1. Nmap  - (nmap -T4 -p- -A <IP>) OR (nmap -T4 -p- <ip> THEN nmap -T4 -p port,port,port -A <ip>)
		1. Frequent weak points: SSH, HTTP (80,443), SMB
			1. for HTTP,HTTPS goto http://<ip> and https://<ip>. Look for poor hygeine, services, OS, any other information findable
 

