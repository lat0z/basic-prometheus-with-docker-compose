FROM alpine:latest as builder 
COPY node_exporter-1.0.0-rc.0.linux-amd64.tar.gz .
#for final only
#ADD https://github.com/prometheus/node_exporter/releases/download/v1.0.0-rc.0/node_exporter-1.0.0-rc.0.linux-amd64.tar.gz .
RUN tar -xzf node_exporter-1.0.0-rc.0.linux-amd64.tar.gz

FROM alpine:latest 
EXPOSE 9100
COPY --from=builder node_exporter-1.0.0-rc.0.linux-amd64 /node_exporter
WORKDIR /node_exporter
CMD ./node_exporter