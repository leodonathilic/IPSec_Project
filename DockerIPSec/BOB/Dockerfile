FROM ubuntu:bionic

RUN apt-get update \
    && apt-get install -y net-tools iputils-ping iproute2 nano strongswan

RUN cd / && mkdir exchange_bob \
    && mkdir /ca

COPY ipsec.conf /etc/ipsec.conf
COPY ipsec.secrets /etc/ipsec.secrets

WORKDIR /exchange_bob
