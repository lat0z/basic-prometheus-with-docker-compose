#ARG PROM_VERSION=2.16.0
FROM utils:latest
#ENV PV=${PROM_VERSION}
EXPOSE 9090
#for testing in local 
COPY binary/prometheus-2.16.0.linux-amd64.tar.gz . 
#for final only
#ADD https://github.com/prometheus/prometheus/releases/download/v2.16.0/prometheus-2.16.0.linux-amd64.tar.gz .
RUN tar -xzf prometheus-*.linux-amd64.tar.gz 
COPY *.yml /prometheus-2.16.0.linux-amd64/
WORKDIR /prometheus-2.16.0.linux-amd64
CMD ./prometheus

#FROM ubuntu:latest
#RUN apt-get update && apt-get install -y wget  
