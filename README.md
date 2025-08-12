# /etc/sysctl.conf Multiple ISP Load Balancing Config

Note: Requires preconfigured multipath routing

## Edit:`nano /etc/sysctl.conf`
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
net.core.default_qdisc=fq_codel
net.ipv4.tcp_fastopen=3
net.netfilter.nf_conntrack_tcp_loose=1
```
## Save
```
sysctl -p
```
