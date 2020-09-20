Learn Kubernetes
===================================

This lessons focus on setting up kubernetes on a "bare" machine, this type of setup is called single node Kubernetes instance.
It assumes prior knowledge of what is a containerization.

The only requirements for this lessons will be vagrant which will enable us to quickly create, setup and a run a machine instance.

#1. What is Kubernetes
    Kubernetes website defines Kubernetes as "an open source system for automating deployment, scaling, and management of containerized applications".
    It's composed of a collection programs which work together to automate the management of container applications.

#2. Terminology

  a. Pod
    A pod is a "collection" of containers which together form a unit of deployment.
    For example, modern web application are composed of a web app that is connected to an API backend. The two applications would be containerized separately but be connected in some way in order to form a single unit. Its this single unit that is considered as a unit of deployment.
    But in other times we might not have mutiple separate apps, but instead just a single app, for example an API service. This also are considered as single unit of deployments.

  b. Service

  c. Cluster

  d. Node

  e. Controller


#3. Control plane


#4. Lessons

  1. Docker

  2. Etcd

  3. Kubernetes

    a. kubectl

    b. kube-apiserver

    c. kubelet

    d. kube-controller-manager

    e. kube-scheduler

    f. kube-proxy

#5. Next steps
