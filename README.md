# DNS-Spoofer
This is a python program used for DNS spoofing in Linux only.
Windows coming soon..
Works for Python3. Python<3 coming soon..

You need to enable port forwarding on your Linux Machine and enable queue system for packets.
Use ">iptables -I FORWARD -j NFQUEUE --queue-num 0" in linux terminal to enable queue for iptables packets(remove quotations marks).
Use "echo 1 > /proc/sys/net/ipv4/ip_forward" in Linux terminal to enable port forrwarding in chase you want to enable packets to flow. Useable on the same network as your computer
Change the IP at line 13 with any other IP you want the target to be redirected to.
