helm install --name mysql \
  --set mysqlRootPassword=root,mysqlUser=my-user,mysqlPassword=my-password,service.type=LoadBalancer \
    stable/mysql --version 0.12.0 --namespace ops