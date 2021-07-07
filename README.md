# Vagrant Kubernetes Cluster (CN)

本项目演示如何使用Vagrant搭建Kubernetes集群，并针对国内的网络环境做了优化。请在使用前先安装[VirtualBox](https://www.virtualbox.org/wiki/Downloads)与[Vagrant](https://www.vagrantup.com/docs/installation)。

## 版本说明

本项目使用的版本：
```
VirtualBox: 6.1.20 r143896 (Qt5.6.2)
Vagrant: 2.2.16
```

本项目搭建的集群版本：
```
kube-apiserver: v1.21.1
kube-proxy: v1.21.1
kube-controller-manager: v1.21.1
kube-scheduler: v1.21.1
pause: 3.4.1
coredns: v1.8.0
etcd: 3.4.13-0  
```

## 使用方法

### 搭建集群
```bash
https://gitee.com/bambrow/vagrant-k8s-cluster-cn.git
cd vagrant-k8s-cluster-cn
vagrant up
```

### 连接节点
```bash
vagrant ssh master
vagrant ssh worker1
vagrant ssh worker2
```

### 暂停与启动集群
```bash
vagrant halt
vagrant up
```

### 销毁集群
```bash
vagrant destroy -f
```
