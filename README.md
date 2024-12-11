Dependencias
```
brew install eksctl
brew install kubectl
brew install awscli
aws configure
```

Crear k8s cluster:
```
eksctl create cluster --name k8s-goat --region us-east-1 --node-type t3.medium --nodes 2
aws eks list-clusters --region us-east-1
aws eks update-kubeconfig --name k8s-goat --region us-east-1

kubectl cluster-info
kubectl get nodes
```

Instalacion
```
git clone https://github.com/madhuakula/kubernetes-goat.git
cd kubernetes-goat/

bash setup-kubernetes-goat.sh
kubectl get pods

bash access-kubernetes-goat.sh
```

Navegar http://localhost:1234/
