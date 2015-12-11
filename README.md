nginx-pagespeed-src
=========

This role automates the process for building ngx_pagespeed from source following the steps outlined here: https://developers.google.com/speed/pagespeed/module/build_ngx_pagespeed_from_source

Requirements
------------

This has currently been tested against a [Centos 7 box](https://github.com/paulmaunders/vagrant-nginx-pagespeed), but I hope to add debian and other distro support in the future.

Role Variables
--------------

* nps_version: 1.9.32.10 - the nginx pagespeed version
* nginx_version: 1.8.0 - the nginx version
* build_dir: /tmp/build-nginx-pagespeed - the build directory (leave this)
* nps_release: release-{{nps_version}}-beta - the nginx page speed release file pattern (leave this unless Google change their naming conventions) 

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
