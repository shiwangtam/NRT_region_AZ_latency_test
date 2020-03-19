# NRT_region_AZ_latency_test
Latency test for between AZ in NRT region

1a  172.31.44.160
1c  172.31.1.33
1d  172.31.25.42

In NRT region, AZ mapping is fixed

So

# 1A-1C latency is 2.6ms
# 1A-1D latency is 1.8ms
# 1C-1D latency is 1ms

a-c 
~~~
[ec2-user@ia ~]$ ping 172.31.1.33
PING 172.31.1.33 (172.31.1.33) 56(84) bytes of data.
64 bytes from 172.31.1.33: icmp_seq=1 ttl=255 time=2.59 ms
64 bytes from 172.31.1.33: icmp_seq=2 ttl=255 time=2.62 ms
64 bytes from 172.31.1.33: icmp_seq=3 ttl=255 time=2.61 ms
64 bytes from 172.31.1.33: icmp_seq=4 ttl=255 time=2.68 ms
64 bytes from 172.31.1.33: icmp_seq=5 ttl=255 time=2.59 ms
64 bytes from 172.31.1.33: icmp_seq=6 ttl=255 time=2.67 ms
^C
--- 172.31.1.33 ping statistics ---
6 packets transmitted, 6 received, 0% packet loss, time 5007ms
rtt min/avg/max/mdev = 2.593/2.630/2.683/0.045 ms
~~~
a-d
~~~
[root@ia ~]# ping 172.31.25.42
PING 172.31.25.42 (172.31.25.42) 56(84) bytes of data.
64 bytes from 172.31.25.42: icmp_seq=1 ttl=255 time=1.77 ms
64 bytes from 172.31.25.42: icmp_seq=2 ttl=255 time=1.80 ms
64 bytes from 172.31.25.42: icmp_seq=3 ttl=255 time=1.82 ms
64 bytes from 172.31.25.42: icmp_seq=4 ttl=255 time=1.81 ms
64 bytes from 172.31.25.42: icmp_seq=5 ttl=255 time=1.79 ms
^C
--- 172.31.25.42 ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4007ms
rtt min/avg/max/mdev = 1.774/1.803/1.829/0.019 ms
~~~
c-d
~~~
[root@1c ~]# ping 172.31.25.42
PING 172.31.25.42 (172.31.25.42) 56(84) bytes of data.
64 bytes from 172.31.25.42: icmp_seq=1 ttl=255 time=0.982 ms
64 bytes from 172.31.25.42: icmp_seq=2 ttl=255 time=1.07 ms
64 bytes from 172.31.25.42: icmp_seq=3 ttl=255 time=1.06 ms
64 bytes from 172.31.25.42: icmp_seq=4 ttl=255 time=1.04 ms
64 bytes from 172.31.25.42: icmp_seq=5 ttl=255 time=1.03 ms
64 bytes from 172.31.25.42: icmp_seq=6 ttl=255 time=1.08 ms
64 bytes from 172.31.25.42: icmp_seq=7 ttl=255 time=1.05 ms
64 bytes from 172.31.25.42: icmp_seq=8 ttl=255 time=0.998 ms
~~~
