# 安装
helm install --name phpmyadmin stable/phpmyadmin -f values.yaml --version 4.2.6 --namespace ops 

helm upgrade phpmyadmin stable/phpmyadmin -f values.yaml --version 4.2.6 --namespace ops