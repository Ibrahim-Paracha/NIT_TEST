# Day 35

Understanding the ping command
PING is short for Packet InterNet Groper
Ping uses the ICMP protocol (Internet Control Message Protocol)

Google DNS Server (8.8.8.8) is commonly used for connectivity testing. (`ping 8.8.8.8`)

You can control how many packets are sent by using `ping -c 5 8.8.8.8` (for 5 packets).

If you want to receive packets in intervals, type `ping -i 7 8.8.8.8`, to receive the packets in 7 second intervals.

If you want just summary info rather than all the individual messages, use the -q option (quiet mode).

To test IPv4 Loopback: `ping 127.0.0.1`
To test IPv6 Loopback: `ping ::1`
To test localhost: `ping localhost`