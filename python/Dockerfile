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
