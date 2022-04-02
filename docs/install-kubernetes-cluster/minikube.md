# Minikube

## Setup local env for Mac

https://minikube.sigs.k8s.io/docs/

## Mac

### Install docker

```shell
$ brew install docker
```

### Install Hypervisor(amd)

Install hyperkit https://minikube.sigs.k8s.io/docs/drivers/hyperkit/

```shell
$ git clone https://github.com/moby/hyperkit.git
$ cd hyperkit
$ make
$ cp ./build/hyperkit /usr/local/bin/hyperkit
```

### Download minikube https://github.com/kubernetes/minikube/releases
### minikube url list https://github.com/kubernetes/minikube/releases/ (arm | amd)
For MacOS amd

```shell
$ curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-amd64 \
  && chmod +x minikube
$ sudo mv minikube /usr/local/bin
```

### Config minikube
### hyperkit doesn't support mac(arm64)

```shell
## $ minikube config set driver docker
$ minikube config set driver hyperkit
```

### Start minikube

```shell
$ minikube start \
    --cpus=8 \
    --v=4 \
    --memory=8192 \
    --network-plugin=cni \
    --enable-default-cni \
    --bootstrapper=kubeadm \
    --kubernetes-version v1.18.3 \
    --image-mirror-country=cn \
    --image-repository=registry.cn-hangzhou.aliyuncs.com/google_containers
```

### Install kubectl
### https://kubernetes.io/releases/
Download kubectl for Mac, unzip and put into your OS path

```shell
$ curl -LO https://dl.k8s.io/v1.18.6/kubernetes-client-darwin-amd64.tar.gz
```

## Setup local env for Linux

https://minikube.sigs.k8s.io/docs/

### Install docker

Ubuntu:

```shell
$ sudo apt-get install docker.io
```

CentOS:

```shell
$ sudo yum install docker-ce
```

### Install VMtool

For Linux

Install VirtualBox, access and find right version for your OS

```shell
https://www.virtualbox.org/wiki/Linux_Downloads
```

### Download minikube https://github.com/kubernetes/minikube/releases

For Linux

```shell
$ curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 \
  && chmod +x minikube
sudo install minikube /usr/local/bin/
```

### Config minikube

```shell
$ minikube config set driver virtualbox
```

### Start minikube

```shell
$ minikube start \
    --cpus=8 \
    --v=4 \
    --memory=8192 \
    --network-plugin=cni \
    --enable-default-cni \
    --bootstrapper=kubeadm \
    --kubernetes-version v1.18.3 \
    --image-mirror-country=cn \
    --image-repository=registry.cn-hangzhou.aliyuncs.com/google_containers
```

### Install kubectl

Download kubectl for Linux

```shell
$ curl -LO  https://dl.k8s.io/v1.18.6/kubernetes-client-linux-amd64.tar.gz
```
