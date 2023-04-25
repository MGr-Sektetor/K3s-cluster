# Raspberry Pi K3s Cluster
This project sets up a lightweight Kubernetes cluster on Raspberry Pi devices using K3s. The cluster includes high availability, load balancing with MetalLB, GitOps with Flux, monitoring using Grafana and Prometheus, and NFS storage.

## Features
- Kubernetes cluster using K3s
- High availability with multiple control plane nodes
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
│       ├── app.py
│       ├── Dockerfile
│       └── requirements.txt
├── cluster
│   ├── applications
│   │   ├── app-namespace.yaml
│   │   ├── nodejs-deploy.yaml
│   │   ├── python-deploy.yaml
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
│       ├── monitoring-namespace.yaml
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



### TODO

- Network Policies + Loadbalancing (Cilium)
- Dashboard as Code
- StackRock
- Logging for Applications
- Use Taints for Control plane and add more RPi workers https://kubernetes.io/docs/concepts/scheduling-eviction/taint-and-toleration/
