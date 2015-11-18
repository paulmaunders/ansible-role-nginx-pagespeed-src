nginx-pagespeed
=========

This role automates the process for building ngx_pagespeed from source following the steps outlined here: https://developers.google.com/speed/pagespeed/module/build_ngx_pagespeed_from_source

Requirements
------------

N/A

Role Variables
--------------

nps_version: 1.9.32.10
nginx_version: 1.8.0
build_dir: /tmp/build-nginx-pagespeed
nps_release: release-{{nps_version}}-beta

Dependencies
------------

N/A

Example Playbook
----------------

Here's an example of how to use with a vagrant box...

```
- hosts: default
  user: vagrant
  sudo: True
  gather_facts: True
  roles:
    - ansible-role-nginx-pagespeed
```

License
-------

BSD

Author Information
------------------

Paul Maunders (https://github.com/paulmaunders)
