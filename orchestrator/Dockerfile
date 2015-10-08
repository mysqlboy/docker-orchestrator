FROM debian:jessie
MAINTAINER andrew.moore@percona.com

RUN apt-get -qq update
RUN apt-get install -y golang wget
RUN wget https://github.com/outbrain/orchestrator/releases/download/v1.4.415/orchestrator_1.4.415_amd64.deb
RUN dpkg --install orchestrator_1.4.415_amd64.deb
ADD orchestrator.conf.json /etc/orchestrator.conf.json

WORKDIR /usr/local/orchestrator/
CMD ["sleep","5"]
CMD ["./orchestrator","--debug","http"]
