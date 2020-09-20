Learn Kubernetes
===================================

This lessons focus on setting up kubernetes on a "bare" machine, what is called single node Kubernetes.

This tutorials were motivated by the long winding road I took while learning Kubernetes and wished if I had similar resource.

I will focus on making it simple and painless so that you can quickly getted started with kubernetes.

The only assumption I make is modest knowledge of containers and linux system.

# What is Kubernetes

Kubernetes is defined on the Kubernetes website as "an open source system for automating deployment, scaling, and management of containerized applications".

It's composed of a collection programs which work together to automate the management of container applications.

# Terminology

  a. Pod

A pod is a "collection" of containers which together form a unit of deployment.

For example, modern web application are composed of a web app that is connected to an API backend. The two applications would be containerized separately but be connected in some way in order to form a single unit. Its this single unit that is considered as a unit of deployment.

But in other times we might not have mutiple separate apps, but instead just a single app, for example an API service. This also are considered as single unit of deployments.

  b. Service

  c. Cluster

  d. Node

  e. Controller


# Control plane


# Lessons

  1. Docker

  2. Etcd

  3. Kubernetes

    a. kubectl

    b. kube-apiserver

    c. kubelet

    d. kube-controller-manager

    e. kube-scheduler

    f. kube-proxy

# 5. Next steps
