# DNS-Spoofer
This is a python program used for DNS spoofing in Linux only.
You can use it in Linux or Windows, make sure you have the interpreter installed and the necessary libraries.
Make sure to enable Windows iptables queue and portforwarding.
Python 2.7 + compatible.
HTTP and HTTPS supported ( sslstrip ).

You need to enable port forwarding on your Linux Machine and enable queue system for packets.

Use:
>iptables -I FORWARD -j NFQUEUE --queue-num 0

in linux terminal to enable queue for iptables packets.

If you want to test it on your own local computer instead of
>iptables -I FORWARD -j NFQUEUE --queue-num 0 

you'll need to type the following two commands in the linux terminal in this order:
>iptables -I INPUT -j NFQUEUE --queue-num 0

>iptables -I OUTPUT -j NFQUEUE --queue-num 0

Use:
>echo 1 > /proc/sys/net/ipv4/ip_forward

in Linux terminal to enable port forrwarding in chase you want to enable packets to flow.
#
Change the IP at line 13 with any other IP you want the target to be redirected to.
Change "www.bing.com" to whatever DNS you want to spoof, but be aware that only works with HTTP at the moment..
#
