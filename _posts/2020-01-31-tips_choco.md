---
layout: default
title:  "Chocolatey for Windows"
date:   2020-01-31 11:11:11 -1111
categories: tips
tags: devops
---
<h1>{{ page.title }}</h1>

## The Package Manager for Windows

## Official site
* [chocolatey](https://chocolatey.org/)

## installation
- Open PowerShell in administrator mode
- Run : Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
- Done

## Firts steps
- choco install minikube
- choco install kubernetes-helm --version=2.16.1
- choco install jekyll
- choco install gradle
- etc...