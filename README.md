Introduction
============

Repository containing my Verisure Wireless alarm scripts. 
For now, only contains a GNU Radio flowgraph which demodulates and dissects radio messages. If '-k <key>' is provided, messages are also decrypted.

Author
======
- Name: Jerome Nokin
- E-mail: jerome.nokin@gmail.com
- Web: http://funoverip.net
- Twitter: @funoverip.net

See also
=============
- http://funoverip.net/2014/11/reverse-engineer-a-verisure-wireless-alarm-part-1-radio-communications/


Receiver HOWTO
==============

```
$ cd receiver/
$ ./verisure_rx.py -k 1abbd3085124d092aeccfa7802c9fe0d
linux; GNU C++ version 4.8.2; Boost_105400; UHD_003.007.002-0-unknown

Using Volk machine: sse4_2_32_orc
gr-osmosdr v0.1.3-1-g4bb2fa4e (0.1.4git) gnuradio 3.7.5git-214-g94562c93
built-in source types: file fcd rtl rtl_tcp uhd hackrf rfspace 
Using HackRF One with firmware 2014.08.1 
[13:10:11.803448] AES key provided. Decryption enabled
[13:10:11.803569] AES-128 IV : 00000000000000000000000000000000
[13:10:11.803626] AES-128 key: 1abbd3085124d092aeccfa7802c9fe0d
[13:10:11.803682] Starting flowgraph
[13:10:11.804074] Frequency tuned to: 869037.22 KHz
[13:10:20.175256] 0f 14 14 0100c3a7 ffffffff 81 00 00 00 00
[13:10:20.175462] 0f 14 18 0100c3a7 ffffffff 81 00 0a 00 00
[13:10:20.175559] 0f 14 1c 0100c3a7 ffffffff 81 00 14 00 00
[13:10:20.175693] 0f 14 00 0100c3a7 ffffffff 81 00 1e 00 00
[13:11:00.365623] 1a 08 d8 050232d1 0100c3a7 58 f9 87 00 1e 9e f9 82 62
[13:11:00.365757] 1a 0c c7 0100c3a7 050232d1 01 8d 88 00 00 85 85 70 bb
[13:11:20.115119] 0f 14 08 0100c3a7 ffffffff 81 00 00 00 00
[13:11:20.115237] 0f 14 0c 0100c3a7 ffffffff 81 00 0a 00 00
[13:11:20.222030] 0f 14 10 0100c3a7 ffffffff 81 00 14 00 00
[13:11:20.222251] 0f 14 14 0100c3a7 ffffffff 81 00 1e 00 00
[13:12:20.135730] 0f 14 18 0100c3a7 ffffffff 81 00 00 00 00
[13:12:20.136097] 0f 14 1c 0100c3a7 ffffffff 81 00 0a 00 00
[13:12:20.136260] 0f 14 00 0100c3a7 ffffffff 81 00 14 00 00
[13:12:20.136453] 0f 14 04 0100c3a7 ffffffff 81 00 1e 00 00
[13:12:40.267982] 1a 08 dc 050232db 0100c3a7 0a 68 87 00 1e 32 f4 a9 77
[13:12:40.368316] 1a 0c cb 0100c3a7 050232db 01 bb 88 00 00 0b 3a 0c 8a
[13:13:12.124306] 1a 08 db 0301fa45 0100c3a7 0e cc 87 00 94 3d 0a 7d 87
[13:13:12.224630] 1a 0e cf 0100c3a7 0301fa45 08 10 88 00 00 8e 26 2d 50
```
