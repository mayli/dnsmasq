# dnsmasq + rfc2317 hack to allow rdns < /24, mostly for dn42 fun

/etc/dnsmasq.d/dn42.conf
```
# common section
log-queries
no-resolv
selfmx
except-interface=eth0
server=169.254.169.254
server=/dn42/172.20.0.53
server=/20.172.in-addr.arpa/172.20.0.53
server=/21.172.in-addr.arpa/172.20.0.53
server=/22.172.in-addr.arpa/172.20.0.53
server=/23.172.in-addr.arpa/172.20.0.53
server=/d.f.ip6.arpa/fd42:d42:d42:54::1

# zone
auth-server=m.dn42,lax
auth-zone=m.dn42,172.22.172.32/27

host-record=xn--kcr700j.m.dn42.,172.22.172.35
host-record=xn--vcsu3i.m.dn42.,172.22.172.36
host-record=xn--onqt01estg.m.dn42.,172.22.172.37
host-record=xn--1bsx4k.m.dn42.,172.22.172.38
host-record=xn--2jzvb.m.dn42.,172.22.172.39
host-record=xn--9iqw55m13b.m.dn42.,172.22.172.40
```
