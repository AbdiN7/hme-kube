```
kubectl create -f metallb-namespace.yaml

kubectl apply -f metallb-frr.yaml
```


```
kubectl create -f metallb-configmap.yaml
kubectl create -f metallb-bgp.yaml
```