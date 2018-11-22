# install helm guide

## download helm
下载相应的版本：https://github.com/kubernetes/helm/releases
这里我下载的是helm-v2.9.1-linux-amd64.tar.gz
解压 (tar -zxvf helm-v2.9.1-linux-amd64.tar.gz)
把helm执行文件放置在： (mv linux-amd64/helm /usr/local/bin/helm)

## helm 需要k8s集群配置文件，在搭建k8s集群时生成

```bash
helm init --upgrade -i registry.cn-hangzhou.aliyuncs.com/google_containers/tiller:v2.9.1 --stable-repo-url https://kubernetes.oss-cn-hangzhou.aliyuncs.com/charts
helm ls
```
