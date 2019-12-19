helm install --name redis-exporter -f values.yaml --version 3.1.0 --namespace monitoring stable/prometheus-redis-exporter

helm delete --purge redis-exporter