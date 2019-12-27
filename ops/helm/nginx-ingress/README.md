# 安装
helm install stable/nginx-ingress -f values.yaml --version 1.27.0 --namespace kube-system --name nginx-ingress

helm upgrade nginx-ingress --version 1.27.0 stable/nginx-ingress -f values.yaml --namespace kube-system