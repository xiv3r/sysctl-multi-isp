# /etc/sysctl.conf Multi Wan Config
Multiple WAN ISP Router /etc/sysctl.conf config for load balancing without failover | Combines all isp speed. 

```
# TCP Buffer Tuning
net.core.rmem_max=16777216
net.core.wmem_max=16777216
net.ipv4.tcp_rmem=4096 87380 8388608
net.ipv4.tcp_wmem=4096 65536 8388608
net.ipv4.tcp_fastopen=3
net.ipv4.tcp_moderate_rcvbuf=1

# Connection Tracking
net.netfilter.nf_conntrack_max=262144
net.nf_conntrack_max=262144
net.netfilter.nf_conntrack_tcp_timeout_established=86400
net.netfilter.nf_conntrack_tcp_timeout_close_wait=3600

# TCP Performance
net.ipv4.tcp_window_scaling=1
net.ipv4.tcp_sack=1
net.ipv4.tcp_fac=1
net.ipv4.tcp_congestion_control=cubic
net.ipv4.tcp_mtu_probing=1
net.ipv4.tcp_base_mss=1460

# Routing and Forwarding
net.ipv4.ip_forward=1
net.ipv4.conf.all.rp_filter=0
net.ipv4.conf.default.rp_filter=0
net.ipv4.conf.all.accept_local=1
net.ipv4.conf.all.send_redirects=0
net.ipv4.conf.default.send_redirects=0
net.ipv4.ip_nonlocal_bind=1
net.ipv4.conf.all.accept_source_route=1

# Socket and Backlog
net.core.somaxconn=65535
net.core.netdev_max_backlog=5000

# ARP and Neighbor Table
net.ipv4.neigh.default.gc_thresh1=1024
net.ipv4.neigh.default.gc_thresh2=2048
net.ipv4.neigh.default.gc_thresh3=4096
```
