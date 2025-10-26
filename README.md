Metasploitable SMB Lab


Purpose

This lab tests SMB and other services on a Metasploitable VM (target 192.168.229.130) and shows how to enumerate services and SMB info.

Target

192.168.229.130 (Metasploitable) vulnerable vm 

Actions performed / Commands used

ssh msfadmin@192.168.229.130
nmap -sS -Pn -p- -T4 192.168.229.130              # full TCP port scan to find open ports
nmap -sC -sV -p 192.168.229.130                  # service/version scan on open ports
enum4linux -a 192.168.229.130                    # SMB enumeration (users, shares, host info)

Key findings

Found many open services (FTP, SSH, Telnet, SMB, etc.)
Found available user accounts and host/domain details (including msfadmin)

Files in this repo (screenshot and logs) 

e0num4linuxSMB scan.txt
open services ports.txt
ssh_session.log
ssh from kali to metesplaitable (target).png
finding tcp open ports .png
Serviceversion scan on open ports1.png
smb scan of metaspliatable1.png
smb scan of metaspliatable 2.png

How to do this lab 

1. Start your attacker VM (Kali) and the Metasploitable VM on the same lab network.
2. SSH to the target for quick checks: ssh msfadmin@192.168.229.130
3. Run the full nmap scan to discover open ports: nmap -sS -Pn -p- -T4 192.168.229.130
4. Run service/version scan on discovered ports: nmap -sC -sV -p <ports> 192.168.229.130
5. Enumerate SMB details: enum4linux -a 192.168.229.130
6. Save screenshots and output files into the repo folder.
   
