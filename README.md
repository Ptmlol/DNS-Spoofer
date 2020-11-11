# DNS-Spoofer
This is a python program used for DNS spoofing in linux distros only. Windows coming soon..
Works for Python3.

You need to enable port forwarding on your Linux Machine and enable queue system for packets.
Use ">iptables -I FORWARD -j NFQUEUE --queue-num 0" in linux terminal to enable queue for iptables packets(remove quotations marks).
Use "echo 1 > /proc/sys/net/ipv4/ip_forward" in Linux terminal to enable port forrwarding in chase you want to spoof another computer on the same network as you are.
Change the IP at line 13 with any other IP you want the target to be redirected to.
