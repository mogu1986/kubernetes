# 安装
helm install stable/nginx-ingress -f values.yaml --version 1.24.5 --namespace kube-system --name nginx-ingress

helm upgrade nginx-ingress --version 1.24.5 stable/nginx-ingress -f values.yaml --namespace kube-system