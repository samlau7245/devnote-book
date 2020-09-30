# 安装 iptables-services

```sh
# 关闭防火墙
$ systemctl stop firewalld
$ systemctl mask firewalld

# 安装 iptables-services
$ yum install iptables-services

# 设置开机启动
$ systemctl enable iptables.service

$ systemctl stop iptables
$ systemctl start iptables
$ systemctl restart iptables
$ systemctl reload iptables
```

# 开放8080端口

在 iptables 中添加8080端口：

```sh
$ cd /etc/sysconfig/
$ vi iptables
```

在`iptables`中新增`$ -A IN_public_allow -p tcp -m tcp --dport 8080 -m conntrack --ctstate NEW,UNTRACKED -j ACCEPT`。

<img src="/assets/images/Linux/01.png">

重新启动 iptables:

```sh
$ systemctl stop iptables
$ systemctl start iptables
$ systemctl restart iptables
$ systemctl reload iptables
```

