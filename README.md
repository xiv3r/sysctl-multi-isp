# /etc/sysctl.conf Multiple ISP Load Balancing Config

Note: Requires preconfigured multiple isp wan multipath routing 

## Access SSH/Telnet
```
ssh root@192.168.1.1
```
```
telnet 192.168.168.1.1
```

## Edit:
```
nano /etc/sysctl.conf
```
```
net.ipv4.ip_forward=1
net.ipv4.tcp_fastopen=3
net.ipv4.tcp_mtu_probing=1
net.core.default_qdisc=fq_codel
net.ipv4.conf.all.rp_filter=0
net.ipv4.conf.all.send_redirects=0
net.ipv4.conf.all.secure_redirects=0
```
## Save
```
sysctl -p
```
<div align="center">
<img src="https://github.com/xiv3r/sysctl-multi-isp/blob/main/MultiWAN.jpg">
</div>
