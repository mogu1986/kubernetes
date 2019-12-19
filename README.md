### 1. 部署顺序(前提 kubectl 互通)
- 设置lablel 标签  :  kubectl label nodes sit-ops2 k8s.shixh.com/group=ops
- 开启凭证、外网访问（部署完毕后关闭外网访问）
- Helm 安装, helm list 验证
- 设置告警
- 创建5命名空间 ops prod yqm log monitor (页面操作完成)
- 设置cbs cbs-ssd

```
kubectl patch storageclass cbs -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}'
```

- secret 创建 ssl 证书
- secret bash auth

- nginx-ingress
- k8s Dashboard
- Endpoints

### 2. service 说明
- 需要外部访问的才有service，也会有ingress

### 相关问题
##### 1. 跨域问题？
用k8s ingress 加入heder搞定。

##### 2. 线上需要改nginx.conf文件，该怎么办？
nginx.conf是利用一个configmap挂载上去，只需要改configmap就可以，改完重启一次服务。

##### 3. 新创建的集群，能ping通内网vpn，但是不能访问端口?
需要把新创建的集群(其实就是ecs节点)，加入到安全组里面，比如加入到prod安全组。

##### 4. 如何安全对删除节点
- 先查看 节点名称  kubectl get nodes
- 执行 kubectl drain cn-beijing.172.20.0.246 --ignore-daemonsets --delete-local-data
- 控制台删除即可