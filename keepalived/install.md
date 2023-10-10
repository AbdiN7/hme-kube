```
yum install -y keepalived
```


```
vim /etc/keepalived/keepalived.conf
```

```
systemctl enable keepalived
systemctl start keepalived


systemctl restart systemd-networkd
ip -brief address show    

```