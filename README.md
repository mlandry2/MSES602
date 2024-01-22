# Week 1 README.md
Morgan Landry
MSES 602

I used vagrant to install the VirtualBox machine. I created a vagrantfile from a screengrab of the class video. 

Images are stored in the images folder. 

The Screen Grab: See vagrantfile.png

Screenshots of the installation: vagrantinit.png, installinprogress.png installcomplete.png


Finished: 


** PART 2B **

**IP ADDRESSES**
vagrant@vagrant:~$ host regis.edu

regis.edu has address 216.54.215.129

regis.edu mail is handled by 20 d174024b.ess.barracudanetworks.com.

regis.edu mail is handled by 10 d174024a.ess.barracudanetworks.com.

vagrant@vagrant:~$ host programmingkitchen.com

programmingkitchen.com has address 172.200.38.66

programmingkitchen.com mail is handled by 0 smtp.secureserver.net

vagrant@vagrant:~$ host google.com

google.com has address 142.250.113.139

google.com has address 142.250.113.138

google.com has address 142.250.113.100

google.com has address 142.250.113.113

google.com has address 142.250.113.101

google.com has address 142.250.113.102

google.com has IPv6 address 2607:f8b0:4023:1000::71

google.com has IPv6 address 2607:f8b0:4023:1000::64

google.com has IPv6 address 2607:f8b0:4023:1000::8b

google.com has IPv6 address 2607:f8b0:4023:1000::66

google.com mail is handled by 10 smtp.google.com.


**A, MX, CNAME for Regis.edu**

vagrant@vagrant:~$ dig -t A regis.edu

; <<>> DiG 9.16.1-Ubuntu <<>> -t A regis.edu
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 46115
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;regis.edu.                     IN      A

;; ANSWER SECTION:
regis.edu.              300     IN      A       216.54.215.129

;; Query time: 40 msec
;; SERVER: 127.0.0.53#53(127.0.0.53)
;; WHEN: Mon Jan 22 03:29:17 UTC 2024
;; MSG SIZE  rcvd: 54

vagrant@vagrant:~$ dig -t MX regis.edu

; <<>> DiG 9.16.1-Ubuntu <<>> -t MX regis.edu
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 24217
;; flags: qr rd ra; QUERY: 1, ANSWER: 2, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;regis.edu.                     IN      MX

;; ANSWER SECTION:
regis.edu.              3600    IN      MX      10 d174024a.ess.barracudanetworks.com.
regis.edu.              3600    IN      MX      20 d174024b.ess.barracudanetworks.com.

;; Query time: 52 msec
;; SERVER: 127.0.0.53#53(127.0.0.53)
;; WHEN: Mon Jan 22 03:29:24 UTC 2024
;; MSG SIZE  rcvd: 113

vagrant@vagrant:~$ dig -t CNAME regis.edu

; <<>> DiG 9.16.1-Ubuntu <<>> -t CNAME regis.edu
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 7137
;; flags: qr rd ra; QUERY: 1, ANSWER: 0, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;regis.edu.                     IN      CNAME

;; Query time: 52 msec
;; SERVER: 127.0.0.53#53(127.0.0.53)
;; WHEN: Mon Jan 22 03:29:29 UTC 2024
;; MSG SIZE  rcvd: 3

**A, MX, CNAME for ProgrammingKitchen.com**

vagrant@vagrant:~$ dig -t A programmingkitchen.com

; <<>> DiG 9.16.1-Ubuntu <<>> -t A programmingkitchen.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 23209
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;programmingkitchen.com.                IN      A

;; ANSWER SECTION:
programmingkitchen.com. 600     IN      A       172.200.38.66

;; Query time: 100 msec
;; SERVER: 127.0.0.53#53(127.0.0.53)
;; WHEN: Mon Jan 22 03:30:53 UTC 2024
;; MSG SIZE  rcvd: 67

vagrant@vagrant:~$ dig -t MX  programmingkitchen.com

; <<>> DiG 9.16.1-Ubuntu <<>> -t MX programmingkitchen.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 11925
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;programmingkitchen.com.                IN      MX

;; ANSWER SECTION:
programmingkitchen.com. 3600    IN      MX      0 smtp.secureserver.net.

;; Query time: 92 msec
;; SERVER: 127.0.0.53#53(127.0.0.53)
;; WHEN: Mon Jan 22 03:31:03 UTC 2024
;; MSG SIZE  rcvd: 88

vagrant@vagrant:~$ dig -t CNAME programmingkitchen.com

; <<>> DiG 9.16.1-Ubuntu <<>> -t CNAME programmingkitchen.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 19107
;; flags: qr rd ra; QUERY: 1, ANSWER: 0, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;programmingkitchen.com.                IN      CNAME

;; Query time: 56 msec
;; SERVER: 127.0.0.53#53(127.0.0.53)
;; WHEN: Mon Jan 22 03:31:13 UTC 2024
;; MSG SIZE  rcvd: 51


**A, MX, CNAME For Google.com**

; <<>> DiG 9.16.1-Ubuntu <<>> -t A google.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 60076
;; flags: qr rd ra; QUERY: 1, ANSWER: 6, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;google.com.                    IN      A

;; ANSWER SECTION:
google.com.             290     IN      A       142.250.113.102
google.com.             290     IN      A       142.250.113.101
google.com.             290     IN      A       142.250.113.113
google.com.             290     IN      A       142.250.113.100
google.com.             290     IN      A       142.250.113.138
google.com.             290     IN      A       142.250.113.139

;; Query time: 95 msec
;; SERVER: 127.0.0.53#53(127.0.0.53)
;; WHEN: Mon Jan 22 03:32:18 UTC 2024
;; MSG SIZE  rcvd: 135

vagrant@vagrant:~$ dig -t MX  google.com

; <<>> DiG 9.16.1-Ubuntu <<>> -t MX google.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 63342
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;google.com.                    IN      MX

;; ANSWER SECTION:
google.com.             300     IN      MX      10 smtp.google.com.

;; Query time: 56 msec
;; SERVER: 127.0.0.53#53(127.0.0.53)
;; WHEN: Mon Jan 22 03:32:25 UTC 2024
;; MSG SIZE  rcvd: 60

vagrant@vagrant:~$ dig -t CNAME google.com

; <<>> DiG 9.16.1-Ubuntu <<>> -t CNAME google.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 48513
;; flags: qr rd ra; QUERY: 1, ANSWER: 0, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;google.com.                    IN      CNAME

;; Query time: 36 msec
;; SERVER: 127.0.0.53#53(127.0.0.53)
;; WHEN: Mon Jan 22 03:32:30 UTC 2024
;; MSG SIZE  rcvd: 39


**TTL for each portion of the DNS hierarchy**

**Regis.edu**

A: 300 ms
MX: 3600 ms
CNAME: n/a

**programmingkitchen.com**

A: 300 ms
MX: 3600 ms
CNAME: n/a

**google.com**
A: 290 ms
MX: 300 ms
CNAME: n/a

**Reverse DNS Lookup**

vagrant@vagrant:~$ dig -x 8.8.8.8

; <<>> DiG 9.16.1-Ubuntu <<>> -x 8.8.8.8
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 39795
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;8.8.8.8.in-addr.arpa.          IN      PTR

;; ANSWER SECTION:
8.8.8.8.in-addr.arpa.   24346   IN      PTR     dns.google.

;; Query time: 48 msec
;; SERVER: 127.0.0.53#53(127.0.0.53)
;; WHEN: Mon Jan 22 01:37:49 UTC 2024
;; MSG SIZE  rcvd: 73

vagrant@vagrant:~$ dig -x 8.8.4.4

; <<>> DiG 9.16.1-Ubuntu <<>> -x 8.8.4.4
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 2675
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;4.4.8.8.in-addr.arpa.          IN      PTR

;; ANSWER SECTION:
4.4.8.8.in-addr.arpa.   23725   IN      PTR     dns.google.

;; Query time: 48 msec
;; SERVER: 127.0.0.53#53(127.0.0.53)
;; WHEN: Mon Jan 22 01:38:02 UTC 2024
;; MSG SIZE  rcvd: 73


**Answers to the following questions:**

**a. How did you ensure that you downloaded an Ubuntu image that was not corrupt?**

I did not do any manual checking as I used a vagrantfile script to download and install the VM.

**b. Whare are the different ways you can access your VM via SSH. What are the advantages of each method?**

I used both cmd.exe and PuTTY. cmd.exe is very simple. However, PuTTY provides a graphical user interface where I can save and reuse settings later. 

**c. What is the purpose of DNS?**

Domain name servers allow humans to assign easy-to-remember domain names instead of being forced to remember IP addresses. 

**d. Research the kinds of attacks that could use "Discovery Vulnerabilities" (DNS is an example) to hack into a victim's computer. Tip: Search for "Network Chuck" on YouTube and look for Man In The Middle Attacks, ARP Poisoning, etc.**

Discovery vulnerabilities are software flaws that can be exploited by malicious actors through using a tool such as nmap to scan ports, software, DNS files, and other files available on the server. 

* DNS hijacking is when you change a DNS nameserver to point to your server instead of the correct server.
* DNS tunneling is moving data through DNS servers to where it does not belong.
* DNS cache poisoning is when a malicious actor intercepts a DNS query and puts in an incorrect answer. The DNS server then caches the incorrect answer for future use.  

**e. What were your biggest difficulties with this lab?**

The biggest difficulty was the time constraint as I started class near the end of the first week, so I took some liberties in doing the Vagrant install. 