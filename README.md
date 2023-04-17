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

<pre>
K3s-cluster/
├── ansible
│   ├── inventory.ini
│   ├── k3s_init.yml
│   ├── k3s_install.yml
│   ├── k3s_token.yml
│   ├── nfs_install.yml
│   ├── README.md
│   └── setup_env.yml
├── applications
│   ├── nodejs
│   │   ├── app.js
│   │   ├── Dockerfile
│   │   └── package.json
│   └── python
│       └── Dockerfile
├── cluster
│   ├── applications
│   │   ├── nodejs-deploy.yaml
│   │   └── README.md
│   ├── flux-system
│   │   ├── gotk-components.yaml
│   │   ├── gotk-sync.yaml
│   │   ├── kustomization.yaml
│   │   └── README.md
│   └── monitoring
│       ├── grafana
│       │   ├── grafana-datasource-config.yaml
│       │   ├── grafana-deployment.yaml
│       │   └── service.yaml
│       ├── node-exporter
│       │   ├── daemonset.yaml
│       │   └── service.yaml
│       ├── prometheus
│       │   ├── clusterRole.yaml
│       │   ├── config-map.yaml
│       │   ├── prometheus-deployment.yaml
│       │   └── prometheus-service.yaml
│       └── README.md
└── README.md
</pre>


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
