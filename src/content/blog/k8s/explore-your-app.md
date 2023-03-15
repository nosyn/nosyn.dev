---
title: Viewing Pods and Nodes
author: Son Nguyen
pubDatetime: 2023-03-14T22:27:40-05:00
postSlug: viewing-pods-and-nodes
featured: true
draft: false
tags:
  - kubernetes
  - k8s
  - cloud
  - clusters
  - pods
  - nodes
ogImage: ""
description: Learn about Kubernetes Pods and Nodes and how to troubleshoot deployed applications
---

# Kubernetes Pods

A Pod was generated by **Kubernetes** to hold the application instance. A Pod acts as an abstraction in **Kubernetes**, signifying a collection of one or more application containers, such as Docker, along with some shared resources for those containers. These resources consist of:

- Shared storage, as Volumes
- Networking, as a unique cluster IP address
- Information about how to run each container, such as the container image version or specific ports to use

A Pod in **Kubernetes** represents a logical host for an application and can contain multiple tightly coupled containers. For example, a Pod may contain a Node.js application container and a container that supplies data to the Node.js webserver. The containers in a Pod share IP addresses and port spaces and run on the same node. When a Deployment is created on **Kubernetes**, it creates Pods with containers inside them instead of creating containers directly. Each Pod is associated with a specific node and remains there until it's terminated or deleted. If a node fails, identical Pods are scheduled on other available nodes in the cluster.

# Pods overview

![pods-overview](https://d33wubrfki0l68.cloudfront.net/fe03f68d8ede9815184852ca2a4fd30325e5d15a/98064/docs/tutorials/kubernetes-basics/public/images/module_03_pods.svg "pods-overview")