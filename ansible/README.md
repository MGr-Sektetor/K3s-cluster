**K3s Cluster Ansible Playbook**
This repository contains an Ansible playbook for setting up a K3s cluster on Raspberry Pi devices or any other compatible hardware.

Playbook Overview

*k3s_install.yml performs the following tasks:*

Includes the K3s token from a separate k3s_token.yml file.
Updates and upgrades packages on all nodes.
Installs required dependencies, such as curl and unzip.
Installs K3s on the remaining control plane nodes using the K3s token, specifying the TLS SAN and server address.


*k3s_init.yml performs the following tasks:*

Updates the /boot/cmdline.txt file with cgroup_memory=1 cgroup_enable=memory settings, enabling cgroup memory and memory settings.
Reboots the node if the /boot/cmdline.txt file was updated.

*nfs_install.yml performs the following tasks:*

Installs the required NFS server packages.
Creates an NFS shared directory with the appropriate permissions.
Configures NFS exports, allowing access to the shared directory for a specific IP range.
Restarts the NFS server to apply changes.

*setup_env.yml performs the following tasks:*

Updates and upgrades packages on all nodes.
Installs Python 3 pip on all nodes.
Installs Ansible and a specific version of Ansible Core using pip.

*k3s_token.yml performs the following tasks:*

This repository contains a vault-encrypted file called k3s_token.yml. The file stores the K3s token used to join new nodes to the K3s cluster. The Ansible Vault provides encryption to securely store sensitive information.