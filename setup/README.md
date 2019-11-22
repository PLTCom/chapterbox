# README
Ansible setup playbooks and roles

## Architecture

### Option 1 - Ansible
Apps installed via package manager and native configuration. This option is easy to set up, but difficult to maintain and secure.

### Option 2 - Docker + Ansible
Apps installed via Docker or Podman, Ansible setup and maintenance. More difficult to configure the first time, but highly repeatable afterwards. Would require custom development of playbooks and roles.

### Option 3 - Operators on Microk8s
Operators for kubernetes, running on a minimalist all-in-one k8s solution like microk8s from Canonical. Much of the work is already done via operators (except Nextcloud), making installation and maintenance easy. Potential learning curve problem, as well as potential performance issues TBD.