```
└─$ nmap -Pn -T4 -A -v 10.10.11.247
Starting Nmap 7.94SVN ( https://nmap.org ) at 2025-02-01 04:12 EST
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
Initiating NSE at 04:12
Completed NSE at 04:12, 0.00s elapsed
Initiating NSE at 04:12
Completed NSE at 04:12, 0.00s elapsed
Initiating NSE at 04:12
Completed NSE at 04:12, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 04:12
Completed Parallel DNS resolution of 1 host. at 04:12, 0.03s elapsed
Initiating SYN Stealth Scan at 04:12
Scanning 10.10.11.247 [1000 ports]
Discovered open port 53/tcp on 10.10.11.247
Discovered open port 22/tcp on 10.10.11.247
Discovered open port 21/tcp on 10.10.11.247
Completed SYN Stealth Scan at 04:12, 9.19s elapsed (1000 total ports)
Initiating Service scan at 04:12
Scanning 3 services on 10.10.11.247
Completed Service scan at 04:12, 0.65s elapsed (3 services on 1 host)
Initiating OS detection (try #1) against 10.10.11.247
Retrying OS detection (try #2) against 10.10.11.247
Retrying OS detection (try #3) against 10.10.11.247
Retrying OS detection (try #4) against 10.10.11.247
Retrying OS detection (try #5) against 10.10.11.247
Initiating Traceroute at 04:12
Completed Traceroute at 04:12, 0.41s elapsed
Initiating Parallel DNS resolution of 2 hosts. at 04:12
Completed Parallel DNS resolution of 2 hosts. at 04:12, 0.04s elapsed
NSE: Script scanning 10.10.11.247.
Initiating NSE at 04:12
NSE: [ftp-bounce] PORT response: 500 Illegal PORT command.
Completed NSE at 04:12, 9.14s elapsed
Initiating NSE at 04:12
Completed NSE at 04:12, 2.09s elapsed
Initiating NSE at 04:12
Completed NSE at 04:12, 0.01s elapsed
Nmap scan report for 10.10.11.247
Host is up (0.27s latency).
Not shown: 997 closed tcp ports (reset)
PORT   STATE SERVICE    VERSION
21/tcp open  ftp        vsftpd 3.0.3
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
| -rw-r--r--    1 ftp      ftp          4434 Jul 31  2023 MigrateOpenWrt.txt
| -rw-r--r--    1 ftp      ftp       2501210 Jul 31  2023 ProjectGreatMigration.pdf
| -rw-r--r--    1 ftp      ftp         60857 Jul 31  2023 ProjectOpenWRT.pdf
| -rw-r--r--    1 ftp      ftp         40960 Sep 11  2023 backup-OpenWrt-2023-07-26.tar
|_-rw-r--r--    1 ftp      ftp         52946 Jul 31  2023 employees_wellness.pdf
| ftp-syst: 
|   STAT: 
| FTP server status:
|      Connected to ::ffff:10.10.16.4
|      Logged in as ftp
|      TYPE: ASCII
|      No session bandwidth limit
|      Session timeout in seconds is 300
|      Control connection is plain text
|      Data connections will be plain text
|      At session startup, client count was 1
|      vsFTPd 3.0.3 - secure, fast, stable
|_End of status
22/tcp open  ssh        OpenSSH 8.2p1 Ubuntu 4ubuntu0.9 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 48:ad:d5:b8:3a:9f:bc:be:f7:e8:20:1e:f6:bf:de:ae (RSA)
|   256 b7:89:6c:0b:20:ed:49:b2:c1:86:7c:29:92:74:1c:1f (ECDSA)
|_  256 18:cd:9d:08:a6:21:a8:b8:b6:f7:9f:8d:40:51:54:fb (ED25519)
53/tcp open  tcpwrapped
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=2/1%OT=21%CT=1%CU=32506%PV=Y%DS=2%DC=T%G=Y%TM=679DE
OS:596%P=x86_64-pc-linux-gnu)SEQ(SP=106%GCD=1%ISR=10A%TI=Z%CI=Z%II=I%TS=A)S
OS:EQ(SP=107%GCD=1%ISR=10A%TI=Z%CI=Z%II=I%TS=A)OPS(O1=M53AST11NW7%O2=M53AST
OS:11NW7%O3=M53ANNT11NW7%O4=M53AST11NW7%O5=M53AST11NW7%O6=M53AST11)WIN(W1=F
OS:E88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE88)ECN(R=Y%DF=Y%T=40%W=FAF0%O=M
OS:53ANNSNW7%CC=Y%Q=)T1(R=Y%DF=Y%T=40%S=O%A=S+%F=AS%RD=0%Q=)T2(R=N)T3(R=N)T
OS:4(R=Y%DF=Y%T=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=)T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+
OS:%F=AR%O=%RD=0%Q=)T6(R=Y%DF=Y%T=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=)T7(R=Y%DF=Y
OS:%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)U1(R=Y%DF=N%T=40%IPL=164%UN=0%RIPL=G%
OS:RID=G%RIPCK=G%RUCK=G%RUD=G)IE(R=Y%DFI=N%T=40%CD=S)

Uptime guess: 39.956 days (since Mon Dec 23 05:15:49 2024)
Network Distance: 2 hops
TCP Sequence Prediction: Difficulty=262 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 554/tcp)
HOP RTT       ADDRESS
1   405.58 ms 10.10.16.1
2   182.32 ms 10.10.11.247

NSE: Script Post-scanning.
Initiating NSE at 04:12
Completed NSE at 04:12, 0.00s elapsed
Initiating NSE at 04:12
Completed NSE at 04:12, 0.00s elapsed
Initiating NSE at 04:12
Completed NSE at 04:12, 0.00s elapsed
Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 42.37 seconds
           Raw packets sent: 1493 (69.742KB) | Rcvd: 1138 (50.090KB)
```
まず anonymous FTP login っぽい。


```
sudo -l
find / -perm 4000 2>/dev/null
for port in {1..65535}; do echo > /dev/tcp/127.0.0.1/$port && echo "$port open"; done 2>/dev/null
getcap -r / 2> /dev/null
```

```
wlan1     Scan completed :
          Cell 01 - Address: 02:00:00:00:00:00
                    Channel:1
                    Frequency:2.412 GHz (Channel 1)
                    Quality=70/70  Signal level=-30 dBm  
                    Encryption key:on
                    ESSID:"OpenWrt"
                    Bit Rates:1 Mb/s; 2 Mb/s; 5.5 Mb/s; 11 Mb/s; 6 Mb/s
                              9 Mb/s; 12 Mb/s; 18 Mb/s
                    Bit Rates:24 Mb/s; 36 Mb/s; 48 Mb/s; 54 Mb/s
                    Mode:Master
                    Extra:tsf=00062d11c70c5623
                    Extra: Last beacon: 4184ms ago
                    IE: Unknown: 00074F70656E577274
                    IE: Unknown: 010882848B960C121824
                    IE: Unknown: 030101
                    IE: Unknown: 2A0104
                    IE: Unknown: 32043048606C
                    IE: IEEE 802.11i/WPA2 Version 1
                        Group Cipher : CCMP
                        Pairwise Ciphers (1) : CCMP
                        Authentication Suites (1) : PSK
                    IE: Unknown: 3B025100
                    IE: Unknown: 7F080400400200000040
                    IE: Unknown: DD5C0050F204104A0001101044000102103B00010310470010362DB47BA53A519188FB5458B986B2E41021000120102300012010240001201042000120105400080000000000000000101100012010080002210C1049000600372A000120
```