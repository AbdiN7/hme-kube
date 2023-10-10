```
kubectl create -f common.yaml -f operator.yaml -f crds.yaml
```

```
kubectl create -f cluster.yaml
```

```
kubectl create -f filesystem.yaml
```

```
kubectl create -f csi/rbd/storageclass.yaml
```