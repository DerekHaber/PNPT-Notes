arp-scan -l OR netdiscover -r 10.0.2.0/24

	1. Nmap  - (nmap -T4 -p- -A <IP>) OR (nmap -T4 -p- <ip> THEN nmap -T4 -p port,port,port -A <ip>)
	2. Frequent weak points: SSH, HTTP (80,443), SMB
		1. for HTTP,HTTPS goto http://<ip> and https://<ip>. Look for poor hygeine, services, OS, any other information findable
	3. Web vulnerability scan 
		1. (nikto -h https://<address>) notate findings of OOD software, potential RCE, Overflow, rewrite, remote buffer overflow, and XSS/XST. Keep an eye out for REMOTE. Check webpage source code
	4. Directory scan (dirbuster&) - Choose php for file extensions. 
	5. Use BurpSuite to try different request methods, as well as check server headers for server information
	6. Enumerate SMB 
		7. (msfconsole) (search <service> e.x. search smb) Auxiliary is enumeration, exploit is exploitation, post is post exploitation
			1. use <tool name>
			2. info - information about the selected tool
			3. options - shows available options for the tool
			4. set <option> <value>
			5. run - runs the tool
	7. Enumerate SMB 
		1. (smbclient) - smbclient -L \\\\<ip>\\
			1. Attempt to connect to specific sharenames (smbclient \\\\<ip>\\<sharename>)
			2. trying anonymous login skips the password field
	8. Enumerate SSH
		1. Try to connect via host (if no matching key exchange, ssh <ip> -oKexAlgorithms=+<end group>)
		2. If cipher is required, add -c <cipher>
		3. Look for any banner or header for disclosed info
	9. Identify and research possible vulnerabilities
		1. Use exploit-db, searchsploit, and github for exploits to different services and versions
	10. Nessus Vulnerabillity Scanner (free version can only scan 16 IP addresses per 90 days)
		1. Basic Scan
			1. Basic Network Scan - provide target
			2. Scan type - known web vullnerabilities
			3. all other settings left on default
		2. Advanced Scan
			1. Set PING settings
			2. set what to scan for (printers, ports, etc)
			3. Adjust settings based on client
 