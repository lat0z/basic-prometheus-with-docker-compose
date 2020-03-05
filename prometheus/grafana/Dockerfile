FROM ubuntu:latest as builder 
COPY grafana-6.6.2.linux-amd64.tar.gz . 
#For final only
#add https://dl.grafana.com/oss/release/grafana-6.6.2.linux-amd64.tar.gz .
RUN tar -xzf grafana-6.6.2.linux-amd64.tar.gz

FROM ubuntu:latest
EXPOSE 3000
COPY --from=builder /grafana-6.6.2 /grafana
WORKDIR /grafana
CMD ./bin/grafana-server