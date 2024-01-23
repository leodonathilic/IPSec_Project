FROM ubuntu:bionic

RUN apt-get update \
    && apt-get install -y net-tools iputils-ping  iptables nano iproute2 tcpdump \
    && echo 'net.ipv4.ip_forward = 1' >> /etc/sysctl.conf
    #tcpdump -i eth0 -s 65535 -w eth0.pcap
    

WORKDIR /exchange_eve 


