### Metasploitable SMB Lab — One‑Page Report



Target: 192.168.229.130 (Metasploitable)



* ###### **Actions performed**



SSH to target for basic checks:

ssh msfadmin@192.168.229.130





Full TCP port scan with Nmap:

nmap -sS -Pn -p- -T4 192.168.229.130   (find put open ports with this scan)





Service/version scan on open ports:

nmap -sC -sV -p <open-ports> 192.168.229.130   (find out open services and service) 





SMB enumeration (users, shares, host info):

enum4linux -a 192.168.229.130 





* ###### **Key findings (topline)**





Found many open services (FTP, SSH, Telnet, SMB, ).



Found available user accounts, workstation, domain details including msfadmin.







###### screenshot and logs





enum4linuxSMB scan.txt



open services ports.txt



ssh\_session.log



ssh from kali to metesplaitable (target).png



finding tcp open ports .png



Serviceversion scan on open ports1.png



smb scan of metaspliatable1.png



smb scan of metaspliatable 2.png 



