#ARG PROM_VERSION=2.16.0
FROm alpine:latest as builder
COPY prometheus-2.16.0.linux-amd64.tar.gz .
#for final only
#ADD https://github.com/prometheus/prometheus/releases/download/v2.16.0/prometheus-2.16.0.linux-amd64.tar.gz .
RUN tar -xzf prometheus-*.linux-amd64.tar.gz
COPY *.yml /prometheus-2.16.0.linux-amd64/

FROM alpine:latest
#ENV PV=${PROM_VERSION}
EXPOSE 9090
COPY --from=builder /prometheus-2.16.0.linux-amd64 /prometheus
WORKDIR /prometheus
CMD ./prometheus --web.external-url http://localhost:9090/prometheus
