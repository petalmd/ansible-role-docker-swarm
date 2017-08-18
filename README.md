# ansible-role-docker
Role for creating/managing a Docker Swarm cluster

[![license](https://img.shields.io/github/license/petalmd/ansible-role-docker.svg)](https://github.com/petalmd/ansible-role-docker)

Tested only on CoreOS

## Installation
```
$ ansible-galaxy install petalmd.docker-swarm
```

## Getting started
```
---
- name: Docker Manager
  hosts: docker-manager
  gather_facts: true
  roles:
    - { role: docker-swarm, docker_swarm_mode_kind: manager }


- name: Docker Worker
  hosts: docker-worker
  gather_facts: true
  roles:
    - { role: docker-swarm, docker_swarm_mode_kind: worker }

```

## Contributing
Contributions, questions, and comments are all welcomed and encouraged!

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## Credits

- [Julien Maitrehenry](https://github.com/jmaitrehenry)
