# neocon, or neo container

FROM python:3.7

RUN apt-get update && apt-get -y install \
        build-essential \
        git \
        curl \
        jq \
        dnsutils \
	nmap

RUN pip3 install tqdm pyyaml paramiko fpdf requests bs4
RUN pip3 install elasticsearch==6.3.1
RUN pip3 install cryptography==2.4.2

RUN mkdir -p /usr/localcw/opt/neo
RUN mkdir -p /var/log/neo
RUN touch /etc/default/logstash

RUN mkdir -p /root/.ssh
COPY ./id_rsa /root/.ssh
COPY ./config /root/.ssh
RUN chmod 600 /root/.ssh/id_rsa

#
# github won't store large files, like logstash-6.4.0.deb
# a plan
# host a maven repository at tgndomains
# store logstash-6.4.0.deb
# deploy maven, here
# pull logstash-6.4.0.deb
# continue neo deployment
#

# RUN mkdir -p /root/.ssh
# COPY ./id_rsa /root/.ssh
# COPY ./config /root/.ssh
# RUN chmod 600 /root/.ssh/id_rsa

# RUN curl -L -O https://artifacts.elastic.co/downloads/logstash/logstash-7.1.0.deb

# COPY ./logstash-6.4.0.deb /tmp





