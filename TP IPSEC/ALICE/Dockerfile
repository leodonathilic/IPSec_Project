FROM ubuntu:bionic

RUN apt-get update \
    && apt-get install -y net-tools iputils-ping iproute2 nano openssl strongswan kmod \
    && cd / && mkdir exchange_alice  \
    && cd / && mkdir alice  \
    && echo "route add default gw 192.168.111.3 eth0" > /alice/add_default_gateway.sh \
    && chmod +x  /alice/add_default_gateway.sh\
    && mkdir /ca
    
COPY ipsec.conf /etc/ipsec.conf
COPY ipsec.secrets /etc/ipsec.secrets

WORKDIR /exchange_alice 


