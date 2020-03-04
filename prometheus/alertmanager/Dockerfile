FROM utils:latest
EXPOSE 9093
#for local testing 
COPY binary/alertmanager-0.20.0.linux-amd64.tar.gz .
#for final only 
#ADD https://github.com/prometheus/alertmanager/releases/download/v0.20.0/alertmanager-0.20.0.linux-amd64.tar.gz .
RUN tar -xzf alertmanager-0.20.0.linux-amd64.tar.gz
#COPY alertmanager.yml /alertmanager-0.20.0.linux-amd64
WORKDIR /alertmanager-0.20.0.linux-amd64
#COPY alertmanager.yml alertmanayer.yml
CMD ./alertmanager --config.file=alertmanager.yml