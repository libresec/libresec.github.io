---
layout: post
title:  "tshark cheatsheat"
date:   2015-03-30 00:09:59
categories: cheatsheats
---

### **tshark**: dump and anaylze network traffic
A quick cheatsheet for tshark and related cli utilites.

*******************************************************

#### **tashark**: common switches

- get interfaces (-D)
- specify interface for capture (-i)
- tshark -i <interface number>
- capture for some wduration (-a autostop condition)
    - tshark -i 1 -a duration:3
- write out to a file (-w)
    - tshark -i 1 -a duration:3 -w output.pcap
- capture filter (-f)
- display filter (-R)
- snaplen (-s)
- write out to file (-w)
- read from pcap file (-r)
- disable name resolution (-n)
- timestamps (-t<format>)
- decode as (-d tc.port==8080,http)

#### **capinfo**: get info about a pcap

    $ capinfos out.pcap 
    File name:           out.pcap
    File type:           Wireshark/... - pcapng
    File encapsulation:  Ethernet
    Packet size limit:   file hdr: (not set)
    Number of packets:   400 
    File size:           362 kB
    Data size:           348 kB
    Capture duration:    1 seconds
    Start time:          Sun Mar 29 21:50:18 2015
    End time:            Sun Mar 29 21:50:19 2015
    Data byte rate:      239 kBps
    Data bit rate:       1,916 kbps
    Average packet size: 872.09 bytes
    Average packet rate: 274 packets/sec
    SHA1:                df5328f61cea55bf8afdc514f9016b37aa576230
    RIPEMD160:           efd2adfdce387c2e614df02389abc89389c35f93
    MD5:                 b0d340cead63517f69fbe771d8fa558e
    Strict time order:   True
