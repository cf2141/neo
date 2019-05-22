# neocon, or neo container

FROM python:2.7

RUN apt-get update && apt-get -y install \
        openjdk-8-jdk \
        build-essential \
        git \
        curl \
        cron \
        nano

RUN pip install mysql-python pyyaml paramiko elasticsearch fpdf requests bs4

RUN mkdir -p /usr/localcw/opt/neo
RUN mkdir -p /var/log/neo
RUN touch /etc/default/logstash

#
# github won't store large files, like logstash-6.4.0.deb
# a plan
# host a maven repository at tgndomains
# store logstash-6.4.0.deb
# deploy maven, here
# pull logstash-6.4.0.deb
# continue neo deployment
#

RUN mkdir -p /root/.ssh
COPY ./id_rsa /root/.ssh
COPY ./config /root/.ssh
RUN chmod 600 /root/.ssh/id_rsa

RUN curl -L -O https://artifacts.elastic.co/downloads/logstash/logstash-7.1.0.deb

# COPY ./logstash-6.4.0.deb /tmp





