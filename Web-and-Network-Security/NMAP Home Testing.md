# NMAP Testing

This is my first time ever using NMAP. I used NMAP on Kali Linux with WSL.

I first did a scan for open TCP ports 80 and 443 by running *sudo nmap -sT -p 80,443 192.168.1.0/24*

This resulted in the following IPs with those ports open:

192.168.1.1 (Default Router)
192.168.1.151 (Secondary Router)
192.168.1.238 (HP Printer)

I figured out what each one of these IPs were by visiting them in Google Chrome (exept for 192.168.1.1, I knew that was the main router).

The scan I did was using only the built in "vuln" scripts using the command *sudo nmap --script vuln 192.168.1.X*. Each vulnerability found is listed:

192.168.1.1: None Found

192.168.1.151: CVE-2007-6750 and CVE-2014-3566

192.168.1.238: CVE-2007-6750

## CVE-2007-6750:
Description: The Apache HTTP Server 1.x and 2.x allows remote attackers to cause a denial of service (daemon outage) via partial HTTP requests, as demonstrated by Slowloris, related to the lack of the mod_reqtimeout module in versions before 2.2.15.

Source: cve.org


## CVE-2014-3566
Description: The SSL protocol 3.0, as used in OpenSSL through 1.0.1i and other products, uses nondeterministic CBC padding, which makes it easier for man-in-the-middle attackers to obtain cleartext data via a padding-oracle attack, aka the "POODLE" issue.

Source: cve.org