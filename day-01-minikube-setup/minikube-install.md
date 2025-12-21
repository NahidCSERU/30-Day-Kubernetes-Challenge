## Minikube Installation

### Install
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
chmod +x minikube-linux-amd64
sudo mv minikube-linux-amd64 /usr/local/bin/minikube

### Start cluster
minikube start --driver=docker

### Stop / Delete
minikube stop
minikube delete
