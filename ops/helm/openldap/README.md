helm install --name openldap stable/openldap --namespace ops --version 1.2.3 -f values.yaml 

helm upgrade openldap stable/openldap --namespace ops --version 1.2.3 -f values.yaml


ldapsearch -x -H ldap://openldap.ops.svc.cluster.local:389 -b dc=example,dc=org -D "cn=admin,dc=example,dc=org" -w $LDAP_ADMIN_PASSWORD
