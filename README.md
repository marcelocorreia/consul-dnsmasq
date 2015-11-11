# consul-dnsmasq

Installs and Configures [Hasicorp's Consul] (https://consulproject.io)
and DNSMasq.

## Inventories

```
[consul-servers]
consulServer1.local
consulServer2.local
consulServer3.local

[consul-bootstrap]
consulBootstrap1.local
consulBootstrap2.local

[consul-clients]
consulClient1.local
consulClient2.local
consulClient3.local
consulClient4.local
consulClient5.local
```

## Role Variables

```yml
consul_datacenter: batcave
consul_uid: 1050
consul_user: consul
consul_group: consul
consul_iface: eth1
consul_ip: 127.0.0.1
consul_log_level: info
consul_port: 8600
consul_suffix: consul
consul_ui_dir: /var/consul/ui
consul_version: 0.5.2
consul_encrypt_key: 2M2aASKoKGek05TjpHcsuw==

```

## Example Playbook

```yml
---
  - hosts:
      - consul-bootstrap
      - consul-servers
      - consul-clients
    sudo: no
    gather_facts: true

    roles:
      - { role: marcelocorreia.apt, tags: ['install','apt'], sudo: true, when: "ansible_system == 'Linux'"}
      - { role: marcelocorreia.nomad-install, tags: ['install','hashicorp','nomad']}
      - { role: marcelocorreia.consul-dnsmasq, tags: ['install','hashicorp','consul', 'dnsmasq','config']}
      - { role: HanXHX.nginx, tags: ['install','nginx'], sudo: true}


    vars_files:
      - /some_path/vars/consul.yml

    vars:
      consul_datacenter: batcave
      consul_uid: 1050
      consul_user: consul
      consul_group: consul
      consul_iface: eth1
      consul_ip: 127.0.0.1
      consul_log_level: info
      consul_port: 8600
      consul_suffix: consul
      consul_ui_dir: /var/consul/ui
      consul_version: 0.5.2
      consul_encrypt_key: 2M2aASKoKGek05TjpHczuw==
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
