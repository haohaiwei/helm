# Grafana Helm Chart

```bash
helm install --name nginx-ingress --set "rbac.create=true,controller.service.externalIPs[0]=10.32.254.19,controller.service.externalIPs[1]=10.32.254.20,controller.service.externalIPs[2]=10.32.254.21" stable/nginx-ingress
```



