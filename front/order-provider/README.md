#### 1. 创建 secret
kubectl -n prod create secret generic apiclient --from-file="apiclient_key.pem,apiclient_cert.pem,apiclient_cert.p12"

#### 2. 创建Deployment
kubectl create -f kubernetes.yml