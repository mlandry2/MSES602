The ip address 172.200.38.66 is invalid.
Get the IP address of its DNS Servers:
vagrant@vagrant:~$ dig ns24.domaincontrol.com

; <<>> DiG 9.16.1-Ubuntu <<>> ns24.domaincontrol.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 60176
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;ns24.domaincontrol.com.                IN      A

;; ANSWER SECTION:
ns24.domaincontrol.com. 86400   IN      A       173.201.69.12

;; Query time: 68 msec
;; SERVER: 127.0.0.53#53(127.0.0.53)
;; WHEN: Mon Jan 22 05:28:02 UTC 2024
;; MSG SIZE  rcvd: 67
3. My public IP address is: 72.109.195.118. 
4. My name server info:
vagrant@vagrant:~$ dig -x 72.109.195.118

; <<>> DiG 9.16.1-Ubuntu <<>> -x 72.109.195.118
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 777
;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;118.195.109.72.in-addr.arpa.   IN      PTR

;; ANSWER SECTION:
118.195.109.72.in-addr.arpa. 7200 IN    PTR     118.sub-72-109-195.myvzw.com.

;; Query time: 96 msec
;; SERVER: 127.0.0.53#53(127.0.0.53)
;; WHEN: Mon Jan 22 05:13:37 UTC 2024
;; MSG SIZE  rcvd: 98