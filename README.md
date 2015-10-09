foreman-proxy
=========

An Ansible role for installing a foreman-proxy on RHEL/CentOS 6/7.

I use it to install foreman-proxy on plain http and so this role doesn't configures SSL but PRs are welcomed.

This role only manages foreman-proxy configuration and DOESN'T configure:

- TFTP server
- DHCP server
- DNS server

## Requirements

- SELinux is expected to be enabled.

## Role Variables

| Variable                         | Default                  | Comments (type)                                                                           |
| :---                             | :---                     | :---                                                                                      |
| `foreman_proxy_user`             | `foreman-proxy`          | Under what user foreman-proxy should run                                                  |
| `foreman_proxy_protocol`         | `foreman_proxy_protocol` | Protocol foreman-proxy will operate on. Values: http or https. Note: https was not tested |
| `foreman_proxy_foreman_base_url` | `{{ ansible_fqdn }}`     | Url of Foreman Web UI                                                                     |
| `foreman_proxy_ssl`              | `false`                  | Url of Foreman Web UI                                                                     |
| `foreman_proxy_tftp`             | `http`                   | Should this role configure foreman-proxy settings for tftp AND what protocol will be user |
| `foreman_proxy_dhcp`             | `http`                   | Should this role configure foreman-proxy settings for dhcp AND what protocol will be user |
| `foreman_proxy_dns`              | `http`                   | Should this role configure foreman-proxy settings for dns AND what protocol will be user  |



## Contributing

 Send your suggestions and pull requests to https://github.com/kostyrevaa/ansible-role-foreman-proxy

 When send PR make sure your changes are backward-compatible.


Author Information
------------------

Aleksandr Kostyrev

