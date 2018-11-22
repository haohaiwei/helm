# use helm install prometheus

## create PersientVolume
```bash
cd pv
kubectl create -f PersistentVolume.yaml
kubectl create -f PersistentVolumeClaim.yaml
kubectl get pv
kubectl get pvc
```

## install prometheus
## view values.yaml


```bash
cd ..
vim values.yaml
helm install --name monitor stable/prometheus -f ./values.yaml
## edit config
kubectl edit configmap monitor-prometheus-server
```
## view configmap
```yaml
        target_label: kubernetes_pod_namealerting:
      alertmanagers:
```
## like this 
```yaml
        target_label: kubernetes_pod_name
    alerting:
      alertmanagers:
```

