# cloud-init with ansible-pull

odm-worker
```
#cloud-config
package_update: true
package_upgrade: false

packages:
  - git
  - ansible
runcmd:
 - [ sh, -c, echo "========= cloud-init -- odmworker =========" ]
 - ansible-pull -U https://github.com/commandnet/ansible-playbooks -d /opt/org/repo odm-worker.yml
```
