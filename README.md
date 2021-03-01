Learn Kubernetes
===================================

These lessons focus on setting up Kubernetes on a "bare" machine, what is called single-node Kubernetes.

I will focus on making it simple so that you can gain knowledge of running the main Kubernetes components.

The only assumption I make is modest knowledge of the Linux system and [linux containers](https://www.docker.com/resources/what-container) with [docker](https://www.docker.com/get-started).

### What is Kubernetes

Kubernetes is defined on the Kubernetes website as "an open-source system for automating deployment, scaling, and management of containerized applications".

It's composed of programs that work together to automate the process of building, deploying, and managing container applications on available computing resources. This is accomplished by the fact that Kubernetes offers a single unified view of all the available computing resources.

Before embarking on the hands-on tutorial of Kubernetes, let's first understand the main components that form the Kubernetes world.

### Components

  a. Pod

A pod is the basic unit of scheduling, deployment, and scaling of a containerized application. It's an abstraction on top of containers that masks out details of container management such as scheduling containers for deployment, scaling of the containers, etc.

Modern web applications are composed of a web frontend that is connected to an API backend. The two applications are usually containerized separately and loosely connected through some network layer to form a complete solution. Each containerized unit, in this case, the frontend web app and the API backend constitute a pod that can be scheduled for deployment and scaling. 

In those cases where more than one container may be tightly coupled together, a pod would constitute the involved containers.

Each pod is given an IP address that is only visible and accessible within the Kubernetes cluster.

Pods are given a label that helps Kubernetes to identify and organize them. Labels are a delimited key and value text, for example, "name: awesome-app" where the key is the "name", the value is "awesome-app" with the delimiter ":".

Labels should not be arbitrary and should be thought out early and follow the rules set out by Kubernetes.

  b. Node

A node is the computing resource in which a pod or pods are deployed and executed. Nodes are managed by a controlling hub, and this requires the following services to be run on each node;

1. Kubelet

2. Kube-proxy

  c. Service

A service is a "collection" of  "similar" pods that provide access to the resources hosted by those pods through some well-defined and dependable entry point.

A service is connected to its pods by use of label selectors, which is a special type of label that helps Kubernetes service find the pods it's supposed to schedule and manage. For example on the YAML file;

```yaml
selector:
  name: awesome-app
```

  d. Cluster

A cluster is a collection of nodes plus their controlling hub cobbled together. The control hub also called the master hub, is comprised of the following programs;

1. Etcd

2. Kubernetes API server

3. Kubernetes scheduler

4. Kubernetes control manager

### Lessons

Before running Kubernetes the following dependencies need to be running

  1. [Etcd](https://github.com/etcd-io/etcd) and

  2. [Docker](https://www.docker.com/get-started)

Also, download [Kubernetes](https://kubernetes.io/docs/setup/release/notes/) binaries and unpack in your preferred local directory. 

I will assume at this point they are, and pick up from there;

a. kubectl

b. kube-apiserver

c. kubelet

d. kube-controller-manager

e. kube-scheduler

f. kube-proxy

### 5. Next steps
While this is a good way to gain knowledge of the main components required in running Kubernetes, it's cumbersome and not scalable.

However, there are many viable alternatives, including;

1. [Rancher](https://github.com/rancher/rancher), my choice.

2. Openshift

3. Cloud services such as Amazon Fargate, Google Kubernetes Engine, etc
