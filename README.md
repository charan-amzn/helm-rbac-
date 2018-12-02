# helm-RBAC

In this repository, you can find rbac-config.yaml file to create Service Account for Tiller and gp2-storage-class.yaml file to create a kubernetes Storage Class

To Install and Initiate Helm and to create storageclass:
> brew install kubernetes-helm 
> kubectl apply -f rbac-config.yaml
> helm init --service-account tiller
> kubectl create -f gp2-storage-class.yaml
> kubectl patch storageclass gp2 -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}’
> kubectl get storageclass


