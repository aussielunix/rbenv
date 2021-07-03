# [rbenv](#rbenv)

<img src="https://docs.ansible.com/ansible-tower/3.2.4/html_ja/installandreference/_static/images/logo_invert.png" width="10%" height="10%" alt="Ansible logo" align="right"/>
<img alt="Ansible Quality Score" src="https://img.shields.io/ansible/quality/55443?style=plastic">
<img alt="Ansible Role" src="https://img.shields.io/ansible/role/55443?style=plastic">

[![CI](https://github.com/aussielunix/ansible-role-rbenv/actions/workflows/ci.yml/badge.svg?event=push "CI")](https://github.com/aussielunix/ansible-role-rbenv/actions)

Ansible role for installing [rbenv](https://github.com/sstephenson/rbenv) on Linux.

## Example Playbook

```yaml
- hosts: web
  gather_facts: true
  vars:
    rbenv_owner: 'ubuntu'
    rbenv_users: ['ubuntu']
    rbenv_user_profile: false
    rbenv:
      env: user
      version: v0.4.0
      default_ruby: 3.0.1
      rubies:
      - version: 2.7.3
      - version: 3.0.1
  roles:
    - role: aussielunix.rbenv
      rbenv_users:
        - user
```

## Role Variables

See [defaults/main.yml](./defaults/main.yml) for all variables and their defaults.

## Requirements

None.

## Compatibility

This role has been tested on Ubuntu Focal Fossa (20.04) only.

## Testing

[Tests](https://github.com/aussielunix/ansible-role-rbenv/actions) are run on every commit, pull request, release and periodically.  
If you find issues, please register them in [GitHub](https://github.com/aussielunix/ansible-role-rbenv/issues)  
Testing is done using [GitHub Actions](https://github.com/features/actions) and Ansible itself.

## License

[MIT](./LICENSE)

## Author Information

[Mick Pollard](https://aussielunix.io/) [@aussielunix](https://twitter.com/aussielunix)  
[Andrew Kumanyaev](http://github.com/zzet)
