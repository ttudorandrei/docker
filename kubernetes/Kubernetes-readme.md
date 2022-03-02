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
- Automates rollouts and rollbacks
- Container balancing
- Run everywhere

## How does it benefit the business

- Control and automate deployments and updates
- Save money by optimizing infrastructural resources thanks to the more efficient use of hardware
- Orchestrate containers on multiple hosts
- Solve many common problems deriving by the proliferation of containers by organizing them in “pods” (see the last post!)
- Scale resources and applications in real time
- Test and autocorrection of applications

## K8 self healing

Self-healing is a feature provided by the Kubernetes open-source system. If a containerized app or an application component fails or goes down, Kubernetes re-deploys it to retain the desired state. Kubernetes provides self-healing by default.

## How to use K8 rollback

After the `kubectl apply` command you can check if the deployment rolled out successfully or not and then, if necessary, the `kubectl rollout undo` command can rollback to the previous revision
