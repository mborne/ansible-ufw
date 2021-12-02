mborne.ufw
=========

Configure UFW default policies and rules.

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml)


Sample playbook
---------------

```yaml
---
- hosts: all
  vars:
    ufw_default_outgoing_policy: allow
    ufw_default_incoming_policy: deny
    ufw_rules:
    - { rule: 'limit', port: '22', proto: 'tcp' }
    - { rule: 'allow', port: '80', proto: 'tcp' }
    - { rule: 'allow', port: '443', proto: 'tcp' }
  roles:
    - mborne.ufw
```

Credits
-------

Widely inspired by an old version of [weareinteractive/ansible-ufw](https://github.com/weareinteractive/ansible-ufw).

License
-------

MIT

