curl -X POST "https://prometheus.shixh.com/-/reload"

node-exporter
curl http://172.18.0.205:9100/metrics

redis-exporter
curl http://172.18.0.206:9121/metrics


es-exporter
curl http://172.18.0.206:9108/metrics