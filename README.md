# 利用Avahi库实现基于mDNS协议的服务发现机制

1.1 简介
  利用两台虚拟机模拟两台局域网设备，第一台模拟器主机名study03运行服务端，第二台模拟器主机名study02运行客户端。客户端输出服务端主机名、IPv4、IPv6地址、服务器名称（MQTTServer）、类型（_mqtt._tcp）、地址（mqtts://tb.com）。
1.2 配置环境
①确保虚拟机在同一局域网
根据IP地址可以确定两台虚拟机在同一个子网。

②确认虚拟机的网络模式
两台虚拟机均为NAT模式可以通信。

③确保防火墙没有阻止UDP 5353端口
两台虚拟机均关闭防火墙，如果开启可以用命令设置允许5353端口
sudo ufw allow 5353/udp
1.3 运行结果
开启avahi守护进程，检查状态（是否开启），第一台虚拟机运行服务端。

开启avahi守护进程，检查状态，第二台虚拟机运行客户端，输出服务端信息。
