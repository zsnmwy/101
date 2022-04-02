# Install Kubernetes Cluster


For learning Kubernetes and the Kubernetes ecosystem, installing a cluster is only a very small part of its learning process.

During the learning process, a clean cluster has the usage to allow us to perform various different experiments or tests.

But objectively speaking, installing a Kubernetes cluster is not an easy task for beginners.

In this post, several methods of installing a Kubernetes cluster will be given.

## kubeadm

通过 kubeadm 安装，需要手工安装 docker，kubelet，kubeadm 等

## kind

通过 kind 安装，全自动，无手工步骤，快捷简单，但是节点是基于容器而不是虚拟机的。

## minikube

通过 minikube 安装。

## Vagrant

如果配置 kubeadm 有困难可参考 Vagrantfile

## 跨公网安装集群

- [利用 Kilo 跨公网组建 k3s 集群](https://zsnmwy.notion.site/Kilo-k3s-a3b5c98fab14432594f6bdbaeffb7c77)
- [利用 FabEdge 跨公网组建 k3s 集群](https://zsnmwy.notion.site/FabEdge-k3s-43ef0b8662be4c70bc74185c05cd517e)
