# home-KTHW
Kubernetes The Hard Way (arm64).

### Description
Following along with the [Kubernetes The Hard Way](https://github.com/kelseyhightower/kubernetes-the-hard-way) tutorial.

Using [Hashicorp Vagrant](https://www.vagrantup.com/) running [Debian 12 for Arm64](https://app.vagrantup.com/bento/boxes/debian-12-arm64) using [Parallels](https://www.parallels.com/).

This will create the following 4 VMs.

| Name      | Description            | CPU | RAM   | Storage | IP             |
|-----------|------------------------|-----|-------|---------|----------------|
| `jumpbox` | Administration host    | 1   | 512MB | 10GB    | 10.25.11.5     |
| `server`  | Kubernetes server      | 1   | 2GB   | 20GB    | 10.25.11.6     |
| `node-0`  | Kubernetes worker node | 1   | 2GB   | 20GB    | 10.25.11.10    |
| `node-1`  | Kubernetes worker node | 1   | 2GB   | 20GB    | 10.25.11.11    |

### Prerequisites

1. Installation of the above
1. Installation of [Ansible](https://www.ansible.com/)

### Ansible

To test if Ansible is installed:

- `ansible --version`
- `ansible-community --version`
- `ansible localhost -m ansible.builtin.ping`

### To provision the 4 VMss required to start this tutorial

1. Navigate to the `vagrant` folder
1. Run 
    `vagrant up`

