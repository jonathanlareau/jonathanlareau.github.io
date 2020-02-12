---
layout: default
title:  "Zeebe in Windows"
date:   2020-02-11 11:11:11 -1111
categories: notes
permalink: /kafka-win/
---
# Zeebe installation Notes on windows

## Official documentation
[https://docs.zeebe.io/kubernetes/installing-helm.html](https://docs.zeebe.io/kubernetes/installing-helm.htmlt)

### mkdir

- cd C:\workspace\
- mkdir zeebe
- cd zeebe
- mkdir C:\workspace\zeebe\zeebe-full-helm\zeebe-full\charts\nginx-ingress
- mkdir C:\workspace\zeebe\zeebe-full-helm\zeebe-full\charts\zeebe-operate
- mkdir C:\workspace\zeebe\zeebe-full-helm\zeebe-full\charts\zeebe-cluster

### Clone git projects

- git clone http://github.com/zeebe-io/zeebe-full-helm/
- git clone https://github.com/zeebe-io/zeebe-operate-helm.git
- git clone https://github.com/zeebe-io/zeebe-cluster-helm.git
- git clone https://github.com/helm/charts.git

### Copy charts

- Xcopy /E /I C:\workspace\zeebe\charts\stable\nginx-ingress C:\workspace\zeebe\zeebe-full-helm\zeebe-full\charts\nginx-ingress
- Xcopy /E /I C:\workspace\zeebe\zeebe-operate-helm\zeebe-operate C:\workspace\zeebe\zeebe-full-helm\zeebe-full\charts\zeebe-operate
- Xcopy /E /I C:\workspace\zeebe\zeebe-cluster-helm\zeebe-cluster C:\workspace\zeebe\zeebe-full-helm\zeebe-full\charts\zeebe-cluster

### Install Helm Charts

- cd C:\workspace\zeebe\zeebe-full-helm\zeebe-full\
- helm install --name zeebe .

### Tests

- kubectl get pods,services
- 