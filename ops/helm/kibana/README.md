### 部署命令
helm install --name kibana stable/kibana --version 3.2.4 --namespace log -f values.yaml

helm upgrade kibana stable/kibana --version 3.2.4 --namespace log -f values.yaml