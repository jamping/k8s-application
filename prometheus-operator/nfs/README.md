# prometheus-operator使用nfs做持久化
[安装nfs-storageClass](https://github.com/happinesslijian/k8s-application/tree/master/nfs)
- prometheus-operator安装
```
git clone https://github.com/coreos/kube-prometheus.git
cd kube-prometheus/
kubectl create -f manifests/setup
kubectl get crd |grep coreos
kubectl create -f manifests/
```
安装完成后，修改`prometheus-prometheus.yaml`文件
```
vi prometheus-prometheus.yaml
```
[安装完成如图](https://i.loli.net/2019/09/09/sgJ1VLBMRk8CK4h.png)
- 因为现在是没有持久化的，所以要更改一下`prometheus-prometheus.yaml`文件
```
vi prometheus-prometheus.yaml
```
[更改前如图](https://i.loli.net/2019/09/09/DPh2mbxsBtlcvLf.png) \
[更改后如图](https://i.loli.net/2019/09/29/r5gmDZ3lGCsMn4d.png) \
更改完成后更新prometheus-prometheus.yaml文件即可
