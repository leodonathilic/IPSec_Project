FROM ubuntu:latest 

RUN apt-get update && \
    apt-get install -y nano inetutils-ping strongswan openssl

RUN openssl rand -base64 32 | awk '{print "10.0.0.100 10.0.0.200 : PSK \""$1"\""}' > /etc/ipsec.secrets


COPY ipsec.conf /etc/ipsec.conf


CMD ["ipsec", "start", "--nofork"] #ici ça start strongswan
