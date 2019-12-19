helm install --name elasticsearch-exporter -f values.yaml --version 2.0.0 --namespace monitoring stable/elasticsearch-exporter



helm delete --purge elasticsearch-exporter