```
helm repo update
```


```
helm repo add rancher-stable https://releases.rancher.com/server-charts/stable
```



```
helm install rancher rancher-stable/rancher \
  --namespace cattle-system \
  --set hostname=rancher.example.com \
  --set bootstrapPassword=someSecret \
  --set ingress.tls.source="secret" \
  --set ingress.enabled=true \
  --set replicas=3 \
  --set tls="ingress" \
  --set ingress.ingressClassName="traefik"
```

### If you plan on making chanages
```
helm upgrade rancher rancher-stable/rancher \
  --namespace cattle-system \
  --set hostname=rancher.example.com \
  --set bootstrapPassword=admin \
  --set ingress.tls.source="secret" \
  --set ingress.enabled=true \
  --set replicas=3 \
  --set tls="ingress" \
  --set ingress.ingressClassName="traefik"
```
