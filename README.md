# fish

[![Ansible Galaxy](https://img.shields.io/badge/ansible-galaxy-green.svg?style=flat-square)](https://galaxy.ansible.com/list#/roles/4029)

[![Debian](https://img.shields.io/badge/os-debian-red.svg?style=flat-square)](#)
[![Ubuntu](https://img.shields.io/badge/os-ubuntu-orange.svg?style=flat-square)](#)

> fish is a smart and user-friendly command line shell for OS X, Linux, and the rest of the family.

This role installs fish shell. Optionally change the shell for a number of users. This role uses opensuse repositories, the repository key is **not** added, for security.

## Role Variables

- `fish_users` - List of users whose shell will be changed to fish.
- `fish_completions` - List of completions to download from [GitHub][github_fish].

## Example Playbook

```yml
- hosts: all
  roles:
    - { role: SobanVuex.fish, fish_users: ['soban', 'vagrant'], fish_completions: ['composer'] }
```

## License

MIT

## Author Information

[Alex Soban](https://github.com/SobanVuex)

[github_fish]: https://github.com/fish-shell/fish-shell/tree/master/share/completions
