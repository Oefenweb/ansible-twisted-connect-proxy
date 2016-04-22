## twisted-connect-proxy

[![Build Status](https://travis-ci.org/Oefenweb/ansible-twisted-connect-proxy.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-twisted-connect-proxy) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-twisted--connect--proxy-blue.svg)](https://galaxy.ansible.com/Oefenweb/twisted-connect-proxy/)

Set up (the latest version of) [Twisted connect proxy](https://github.com/fmoo/twisted-connect-proxy) in Ubuntu systems.

#### Requirements

* `python-twisted` (will be installed)

#### Variables

* `twisted_connect_proxy_install_prefix` [default: `/usr/local/bin`]: Install prefix

* `twisted_connect_proxy_user` [default: `twisted-connect-proxy`]: The user that will run the `twisted-connect-proxy` daemon
* `twisted_connect_proxy_group` [default: `twisted-connect-proxy`]: The primary group of the `twisted-connect-proxy` user
* `twisted_connect_proxy_groups` [default: `[]`]: The secondary groups of the `twisted-connect-proxy` user

* `twisted_connect_proxy_port` [default: `''`]: The port on which the daemon should be listening
* `twisted_connect_proxy_options: {}`]: Options to pass to the `twisted-connect-proxy` daemon (e.g. `{ssl-cert: foo.crt, ssl-key: foo.key}`)

## Dependencies

None

#### Example (without any options)

```yaml
---
- hosts: all
  roles:
    - twisted-connect-proxy
```

#### Example (with daemon options)

```yaml
---
- hosts: all
  roles:
    - twisted-connect-proxy
  vars:
    twisted_connect_proxy_port: 3128
    twisted_connect_proxy_options: {}
```
#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-twisted-connect-proxy/issues)!
