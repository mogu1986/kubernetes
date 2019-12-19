helm install --name nfs-client-provisioner stable/nfs-client-provisioner --version 1.2.8 --namespace kube-system --set nfs.server=192.168.123.10 --set nfs.path=/home/nfs

kubectl patch storageclass nfs-client -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}'