Docker
=========
Installs docker, watchtower and portainer on a host, while adding a given user to the docker group.

Requirements
------------
Requires the https://github.com/Morebec/server-init-ansible.git role which can be
added to playbooks with a `requirements.yml` file:

```yaml
- name: server-init
  src: https://github.com/Morebec/ansible-server-init.git
  scm: git
```

Role Variables
--------------
```yaml
# Corresponds to the user with which deployments of this role will be performed.
# defaults to "deploy"  just like the ansible
# This user will be added to the to the docker group.
deploy_user: <string>

# Port from which portainer is available.
# Defaults to 127.0.0.1:9000 which by adding 127.0.0.1 requires port forwarding
# in order to access.
portainer_port: <int>
```
