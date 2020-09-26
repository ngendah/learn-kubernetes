Learn Kubernetes
===================================

This lessons focus on setting up kubernetes on a "bare" machine, what is called single node Kubernetes.

I will focus on making it simple so that you can quickly get started with kubernetes.

The only assumption I make is modest knowledge of the linux system and [linux containers](https://www.docker.com/resources/what-container) with [docker](https://www.docker.com/get-started).

### What is Kubernetes

Kubernetes is defined on the Kubernetes website as "an open source system for automating deployment, scaling, and management of containerized applications".

It's composed of a collection programs which work together to automate the process of building, deploying and managing of container applications on available computing resources. This is accomplished by the fact that kubernetes offers a single unified view of all the available computing resources.

Before embarking on the hands-on tutorial of Kubernetes, let's first understand the various parts/terms that forms the Kubernetes world.

### Terms

  a. Pod

A pod is the basic unit of scheduling, deployment and scaling of a containerized application. It's an abstraction on top of containers that mask out details of container management such scheduling containers for deployment, scaling of the containers et.c.

Modern web applications are composed of a web frontend that is connected to an API backend. The two applications are usually containerized separately and loosely connected together through some network layer in order to form a complete solution. Each containerized unit, in this case the frontend web app and the API backend constitute a pod that can scheduled for deployment and scaling. 

In those cases where more than one container maybe tightly coupled together a pod would constitutes the involved containers.

Each pod is given an IP address that its only visible and accessible within the Kubernetes cluster.

Pods are given a label that helps kubernetes to identify and organize them. Labels are a delimited key and value text, for example "name: awesome-api" where the key is the "name", the value is "awesome-api" with the delimeter ":".

Labels should not be abitrary and should be thought out early and follow the rules set out by Kubernetes.

  b. Node

A node is the computing resource in which a pod or pods are deployed.

  c. Service

A service is a "collection" of  "similar" pods that provide access to the resources hosted by those pods through some well defined and dependable entry point.

A service is connected to its pods by use of label selectors, which is a special type of label that helps kubernetes service find the pods it's supposed to schedule and manage. For example on yaml file;

```yaml
selector:
  name: awesome-api
```

  d. Cluster
A cluster is a collection of nodes plus their controlling hub cobbled together. 

  e. Controller


  f. LifeCycle

### Control plane


### Lessons

  1. Docker

  2. Etcd

  3. Kubernetes

    a. kubectl

    b. kube-apiserver

    c. kubelet

    d. kube-controller-manager

    e. kube-scheduler

    f. kube-proxy

### 5. Next steps
