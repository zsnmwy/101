# Kind

## What's kind

kind is a tool for running local Kubernetes clusters using Docker container “nodes”.

kind was primarily designed for testing Kubernetes itself, but may be used for local development or CI.

## Create kind cluster on mac

```sh
brew install kind
kind create cluster
```

Reference: https://kind.sigs.k8s.io/docs/user/quick-start/#installation


## Install Kind

!!! Tip
    Reference: [Kind Installation](https://kind.sigs.k8s.io/docs/user/quick-start/#installationReference)

=== "macOS"

    ```shell
    brew install kind
    ```

=== "Linux"

    ```shell
    curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.12.0/kind-linux-amd64
    chmod +x ./kind
    mv ./kind /some-dir-in-your-PATH/kind
    ```

=== "Windows"

    ```powershell
    curl.exe -Lo kind-windows-amd64.exe https://kind.sigs.k8s.io/dl/v0.12.0/kind-windows-amd64
    Move-Item .\kind-windows-amd64.exe c:\some-dir-in-your-PATH\kind.exe
    ```

## Creating a Cluster

!!! tip
    If network hard to access the dockerhub, you can use mirror image.

=== "Default Image"

    ```shell
    kind create cluster
    ```

=== "Mirror Image"

    ```shell
    kind create cluster --image docker.m.daocloud.io/kindest/node:v1.17.0
    ```

## Check your Cluster

```shell
kubectl cluster-info --context kind-kind
```
