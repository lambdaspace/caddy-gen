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

* `docker_socket`: Location of docker socket on host machine. Defaults to: `/var/run/docker.sock`
* `acme_storage`: Where ACME will be stored, the path will be created if not present. Defaults to: `/etc/certs/acme`
* `cert_storage`: Where Certs will be stored, the path will be created if not present. Defaults to: `/etc/certs/ocsp`

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
