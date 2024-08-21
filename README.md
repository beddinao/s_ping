# S_PING
## about
s_ping: A lightweight utility designed to emulate a simplified version of the ping command. It provides basic network connectivity testing by sending ICMP echo requests to a specified host and displaying response times.
While offering a core functionality, s_ping may have limitations compared to the full-featured ping command, such as missing advanced options or detailed statistics.
## requirements
- linux
- root privilege
## usage
```
./s_ping DEST [timeout]
  DEST: domain name/ipv4 address of the target host
  timeout: optional number of seconds until host response
```
## example output
```
$ ./s_ping google.com
google.com (142.250.201.78)
	icmp_echo 142.250.201.78 : icmp_echoreply t=39.927 ms, echo.id=27659, icmp_seq=0
	icmp_echo 142.250.201.78 : icmp_echoreply t=39.865 ms, echo.id=27659, icmp_seq=1
	icmp_echo 142.250.201.78 : icmp_echoreply t=39.879 ms, echo.id=27659, icmp_seq=2
	icmp_echo 142.250.201.78 : icmp_echoreply t=39.850 ms, echo.id=27659, icmp_seq=3
	icmp_echo 142.250.201.78 : icmp_echoreply t=39.711 ms, echo.id=27659, icmp_seq=4
	icmp_echo 142.250.201.78 : icmp_echoreply t=40.211 ms, echo.id=27659, icmp_seq=5
^Cquiting..
=== 142.250.201.78 stats ===
packets sent: 7, packet received: 6
time: 693.764 ms
```
