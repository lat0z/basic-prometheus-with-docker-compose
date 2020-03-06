FROM alpine:latest as builder
COPY alertmanager-0.20.0.linux-amd64.tar.gz .
#for final only 
#ADD https://github.com/prometheus/alertmanager/releases/download/v0.20.0/alertmanager-0.20.0.linux-amd64.tar.gz .
RUN tar -xzf alertmanager-0.20.0.linux-amd64.tar.gz

from alpine:latest
EXPOSE 9093
COPY --from=builder /alertmanager-0.20.0.linux-amd64 /alertmanager
WORKDIR /alertmanager
CMD ./alertmanager --config.file=alertmanager.yml --web.external-url http://localhost:9093/alertmanager