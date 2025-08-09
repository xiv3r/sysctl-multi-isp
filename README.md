# /etc/sysctl.conf Multi Wan Config
Multiple WAN ISP Router /etc/sysctl.conf config for load balancing without failover | Combines all isp speed. 

```
net.ipv4.ip_forward=1
net.ipv4.fib_multipath_hash_policy=1
net.ipv4.conf.all.rp_filter=0
net.ipv4.ip_nonlocal_bind=1
net.ipv4.conf.all.accept_local=1
net.ipv4.tcp_ecn=0
net.ipv4.tcp_mtu_probing=1
net.ipv4.conf.all.accept_redirects=0
net.ipv4.conf.all.send_redirects=0
```
