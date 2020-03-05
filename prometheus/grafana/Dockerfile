FROM utils:latest
EXPOSE 3000
#For local testing
COPY grafana-6.6.2.linux-amd64.tar.gz . 
#For final only
#add https://dl.grafana.com/oss/release/grafana-6.6.2.linux-amd64.tar.gz .
RUN tar -xzf grafana-6.6.2.linux-amd64.tar.gz
WORKDIR /grafana-6.6.2
CMD ./bin/grafana-server