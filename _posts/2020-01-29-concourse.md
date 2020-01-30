---
layout: default
title:  "Concourse in minikube"
date:   2020-01-26 22:04:55 -0500
categories: notes
---
# Concourse installation in minikube

### Download the official helm chart
- [https://github.com/concourse/concourse-chart](https://github.com/concourse/concourse-chart)

### Create charts folder in concourse-chart
- cd concourse-chart
- mkdir charts

### Copy postgresql chart into the charts folder
- copy from helm stable charts
- [https://github.com/helm/charts/tree/master/stable/postgresql](https://github.com/helm/charts/tree/master/stable/postgresql)
- In: councourse-chart/charts/postgresql

### Run Helm
- helm install --name concourse .