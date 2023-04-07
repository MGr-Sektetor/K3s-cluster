# Raspberry Pi K3s Cluster
This project sets up a lightweight Kubernetes cluster on Raspberry Pi devices using K3s. The cluster includes high availability, load balancing with MetalLB, GitOps with Flux, monitoring using Grafana and Prometheus, and NFS storage.

## Features
- Kubernetes cluster using K3s
- High availability with multiple control plane nodes
- Load balancing using MetalLB
- GitOps workflow with Flux
- Monitoring and observability using Grafana and Prometheus
- NFS storage across Raspberry Pi nodes
- Example applications: Node.js and Python
- Update management with Ansible playbooks


## Directory Structure

my-rpi-cluster/
├── ansible/
│   ├── inventory.ini
│   ├── k3s_install.yml
│   ├── nfs_install.yml
│   └── README.md
├── applications/
│   ├── nodejs-app/
│   │   ├── deployment.yaml
│   │   └── service.yaml
│   └── python-app/
│       ├── deployment.yaml
│       └── service.yaml
├── clusters/
│   ├── k3s/
│   │   ├── ingress.yaml
│   │   ├── namespaces.yaml
│   │   ├── network.yaml
│   │   ├── storage.yaml
│   │   └── update_management.yaml
│   └── lxe/
│       └── lxe_configuration.yaml
├── gitops/
│   ├── flux_install.yml
│   └── README.md
├── monitoring/
│   ├── grafana.yaml
│   ├── prometheus.yaml
│   └── README.md
├── network/
│   ├── cni.yaml TODO
│   └── networkpolicy.yaml TODO
└── metallb/
    ├── namespace.yaml
    ├── deployment.yaml
    ├── rbac.yaml
    └── configmap.yaml

## Setup 
- Ansible: Use the provided Ansible playbooks to set up K3s on the Raspberry Pi devices and configure NFS storage.
- K3s Cluster: Deploy the K3s cluster with high availability by having multiple control plane nodes.
- Load Balancing: Install and configure MetalLB to provide load balancing for your applications.
- GitOps: Set up a GitOps workflow using Flux to manage your Kubernetes resources from a Git repository.
- Monitoring: Deploy Grafana and Prometheus for monitoring and observability of your cluster and applications.
- Example Applications: Deploy example Node.js and Python applications to test your cluster's functionality.
- Update Management: Use Ansible playbooks to keep your cluster components and operating system up-to-date.


### TODO

Network Policies
