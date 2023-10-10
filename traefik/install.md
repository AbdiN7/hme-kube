############    https://doc.traefik.io/traefik/user-guides/crd-acme/  ############  


```
helm uninstall rke2-ingress-nginx -n kube-system
```

```
helm repo add traefik https://traefik.github.io/charts
```
    
```
helm show values traefik/traefik > traefik-values.yaml 
```
 
```
kubectl apply -f traefik-namespace.yaml
```

```
helm install traefik traefik/traefik -n traefik --values traefik/traefik-values.yaml
```

```
kubectl -n cattle-system create secret tls tls-rancher-ingress \
  --cert=< SOME PATH >.crt \
  --key=< SOME PATH >.key
```

```
kubectl -n traefik create secret tls tls-traefik \
  --cert=< SOME PATH >.crt \
  --key=< SOME PATH >.key
```

```
kubectl apply -f traefik-tlsstore.yaml
```





