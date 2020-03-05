FROM utils:latest
EXPOSE 9100

#for local testing only
COPY node_exporter-1.0.0-rc.0.linux-amd64.tar.gz .
#for final only
#ADD https://github.com/prometheus/node_exporter/releases/download/v1.0.0-rc.0/node_exporter-1.0.0-rc.0.linux-amd64.tar.gz .
RUN tar -xzf node_exporter-1.0.0-rc.0.linux-amd64.tar.gz

WORKDIR /node_exporter-1.0.0-rc.0.linux-amd64
CMD ./node_exporter