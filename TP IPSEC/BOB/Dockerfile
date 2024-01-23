FROM ubuntu:bionic

RUN apt-get update \
    && apt-get install -y net-tools iputils-ping iproute2 nano openssl strongswan kmod iptables-persistent \
    && mkdir exchange_bob \
    && cd / && mkdir bob  \
    && echo "route add default gw 192.168.112.3 eth0" > /bob/add_default_gateway.sh \
    && chmod +x  /bob/add_default_gateway.sh\
    && mkdir /ca

COPY ipsec.conf /etc/ipsec.conf
COPY ipsec.secrets /etc/ipsec.secrets

WORKDIR /exchange_bob
