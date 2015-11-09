# consul-dnsmasq

Installs and Configures [Hasicorp's Consul] (https://consulproject.io)
and DNSMasq.



## Role Variables
```yml

---
app:
  name: consul
  version: 0.5.2

install:
  dir : /usr/local/bin
  download_location: https://dl.bintray.com/mitchellh/consul
  file_list:
    - consul

consul:
  suffix: consul
  ip: 127.0.0.1
  port: 8600
  dnsmasq_config_file: /etc/dnsmasq.d/10-consul

```


Example Playbook
----------------
```yml

---
- hosts: local
  sudo: true
  gather_facts: true

  roles:
    - { role: marcelocorreia.apt, tags: ['install','apt']}
    - { role: marcelocorreia.nomad-install, tags: ['install','hashicorp','nomad']}
    - { role: marcelocorreia.consul-dnsmasq, tags: ['install','hashicorp','consul', 'dnsmasq','config']}


  vars_files:
    - ../vars/consul.yml

```

License
-------

MIT

Author Information
------------------

Some useful stuff at:
- [https://github.com/marcelocorreia](https://github.com/marcelocorreia)
-  [https://galaxy.ansible.com/list#/users/15516](https://galaxy.ansible.com/list#/users/15516)
-  [https://hub.docker.com/u/marcelocorreia/](https://hub.docker.com/u/marcelocorreia/)
-  Any issues, pull-request are welcome
