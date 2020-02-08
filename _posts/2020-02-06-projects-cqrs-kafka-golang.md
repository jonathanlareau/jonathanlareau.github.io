---
layout: default
title:  "Implementation of CQRS with kafka and Golang"
date:   2020-02-06 11:11:11 -1111
categories: projects
permalink: /kafka-chat/
---
<h1>{{ page.title }}</h1>

*In Development...*

## Overview

![Cqrs](/images/Cqrs.jpeg)

## Flow for Query (Read)
- Client (Browser) call the Api Service Facade.
- The facade calls the right service corresponding need.
- The Microservice app use Redis for respond to the query.

## Flow for the Command (Create, Update, Delete)
- Client (Browser) call the Api Service Facade.
- The facade calls the right service corresponding need.
- The Microservice app will use a producer to push a new message in kafka
- Later the consumer will read the message from Kafka and execute the command related.
- The Redis data will be refresh with the current object state.

## ToDo
- Interaction betwwen Microservice App
- Implement a assembler
- Etc...

### Git Project
- [https://github.com/jonathanlareau/cqrs-kafka-golang](https://github.com/jonathanlareau/cqrs-kafka-golang)

