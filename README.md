# argocd-infra-tests

### Deploy ArgoCD in HA mode
```
kubectl create namespace argocd
kubectl apply -n argocd -f ./infrastructure/controllers/argocd
```

### Access ArgoCD
```
kubectl port-forward svc/argocd-server -n argocd 8080:443

argocd login 127.0.0.1:8080
```