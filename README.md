caddy_gen
=========

[PROVISIONAL] `caddy_gen` role will create and start a docker container with Caddy using the image `wemakeservices/caddy-gen:latest`. This container will search for containers with 
the container labels detailed in `caddy-gen`'s [documentation](https://github.com/wemake-services/caddy-gen#usage) to auto-generate its Caddy file.

Requirements
------------

Ansible 2.1 (because of `docker_container` module)
`docker` Python library (again needed by `docker_container`). [Example installation](https://github.com/geerlingguy/ansible-role-docker#use-with-ansible-and-docker-python-library).

Role Variables
--------------

Currently none, although there is plan for providing configuration for mounted volumes.

Dependencies
------------

None.

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: panagiks.caddy_gen }
```

License
-------

MIT
