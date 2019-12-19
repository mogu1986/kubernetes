helm install --name apollo-mysql \
  --set mysqlRootPassword=4gB5BTuZN3,mysqlUser=my-user,mysqlPassword=my-password,service.type=LoadBalancer \
    stable/mysql --version 0.12.0 --namespace apollo