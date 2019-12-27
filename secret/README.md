### 1. 创建 ssl 证书 (sxh.com)
kubectl create secret tls ssl-sxh --key=2647800__shixh.com.key --cert=2647800__shixh.com.pem -n kube-system


kubectl create secret docker-registry harbor --docker-server=http://harbor.jq.cn --docker-username=admin --docker-password=Harbor12345