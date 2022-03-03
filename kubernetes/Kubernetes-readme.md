# Kubernetes

![kubernetes diagram](./../assets/images/kubernetes-architecture.png)

## Table of Contents

- [Kubernetes](#kubernetes)
  - [Table of Contents](#table-of-contents)
  - [What is Kubernetes K8](#what-is-kubernetes-k8)
  - [Benefits of using Kubernetes](#benefits-of-using-kubernetes)
  - [How does it benefit the business](#how-does-it-benefit-the-business)
  - [K8 self healing](#k8-self-healing)
  - [How to use K8 rollback](#how-to-use-k8-rollback)
  - [Useful commands](#useful-commands)
  - [Kubernetes volumes](#kubernetes-volumes)

## What is Kubernetes K8

Kubernetes, also known as K8s, is an open-source system for automating deployment, scaling, and management of containerized applications.

It groups containers that make up an application into logical units for easy management and discovery. Kubernetes builds upon 15 years of experience of running production workloads at Google, combined with best-of-breed ideas and practices from the community

## Benefits of using Kubernetes

- Automates various manual processes
- Interacts with several groups of containers
- Provides additional services
- Self-monitoring
- Horizontal scaling
- Storage orchestration
- Automates roll-outs and rollbacks
- Container balancing
- Run everywhere

## How does it benefit the business

- Control and automate deployments and updates
- Save money by optimizing infrastructural resources thanks to the more efficient use of hardware
- Orchestrate containers on multiple hosts
- Solve many common problems deriving by the proliferation of containers by organizing them in “pods” (see the last post!)
- Scale resources and applications in real time
- Test and auto-correction of applications

## K8 self healing

Self-healing is a feature provided by the Kubernetes open-source system. If a containerized app or an application component fails or goes down, Kubernetes re-deploys it to retain the desired state. Kubernetes provides self-healing by default.

## How to use K8 rollback

After the `kubectl apply` command you can check if the deployment rolled out successfully or not and then, if necessary, the `kubectl rollout undo` command can rollback to the previous revision

## Useful commands

For the Kubernetes commands cheatsheet, [click here](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

- `kubectl get services` returns the running services
- `kubectl get pods` returns the running pods
- `kubectl get deploy` returns the running deploys
- `kubectl describe pods <name-of-pod>` returns the running deploys
- `kubectl delete deploy <name-of-deploy>` deletes a specific deploy
- `kubectl create -f <name-of-yaml-file>` runs yml file
- `kubectl delete <node/service/etc-name>` deletes the specified service

## Kubernetes volumes

On-disk files in a container are ephemeral, which presents some problems for non-trivial applications when running in containers. One problem is the loss of files when a container crashes. The kubelet restarts the container but with a clean state. A second problem occurs when sharing files between containers running together in a Pod. The Kubernetes volume abstraction solves both of these problems. Familiarity with Pods is suggested.
[source](https://kubernetes.io/docs/concepts/storage/volumes/)
