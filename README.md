Ansible Digitalocean DNS
=========

This role implements the [Digitalocean REST API](https://developers.digitalocean.com/documentation/v2/) for managing Digitalocean DNS entries.

Requirements
------------

You will need to create a Digitalocean API Key with write permission and to install the community.digitalocean collection.

Role Variables
--------------

You can find a list of the default variables and examples at [defaults/main.yml](./defaults/main.yml).
You will need to override 'do_oauth_token' with your API Key and 'do_dns_domains' with your domain info, following the pattern in [defaults/main.yml](./defaults/main.yml).
You can also set the variable 'debug' to true, if you want more output for a better error analysis.

Dependencies
------------

- community.digitalocean

Example Playbook
----------------

    - hosts: localhost
      roles:
        - digitalocean
      vars_files: group_vars/digitalocean/digitalocean.yml

Development
-------

Feel free to contribute and improve this role, you are welcome! 
The setup is quite standard, tests are only run locally with molecule as I didn't check for a possibility to test Digitalocean API interactions against some sort of dev/test API.
CI / CD Improvements are very welcome, too.

License
-------

GPLv3

Author Information
------------------

Nils Berg

- nils.berg [at] helmholtz-berlin.de
- n.berg [at] backslashseven.de
