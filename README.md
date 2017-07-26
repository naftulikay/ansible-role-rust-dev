# ansible-role-rust-dev [![Build Status][img-build-status]][build-status]

Installs and configures a Rust development environment for a given user using [`rustup`][rustup].

Available on Ansible Galaxy at [`naftulikay.rust-dev`][galaxy].

## Requirements

Officially tested operating systems are listed in the Galaxy manifest.

## Role Variables

<dl>
  <dt><code>rust_version</code></dt>
  <dd>Version of Rust to install. Optional.</dd>
  <dt><code>rust_user</code></dt>
  <dd>User to install Rust tools for. Required.</dd>
<dl>

## Dependencies

None.

## Example Playbook

Here are some example playbooks to get started with.

### Defaults

Simply get a Rust development environment installed:

```yaml
---
- name: install
  hosts: all
  become: true
  roles:
    - role: rust-dev
      rust_user: vagrant
```

### Install a Specific Version

Install a specific version of Rust:

```yaml
---
  - name: install
    hosts: all
    become: true
    roles:
      - role: rust-dev
        rust_user: vagrant
        rust_version: 1.19.0
```

## License

MIT

 [build-status]: https://travis-ci.org/naftulikay/ansible-role-rust-dev
 [img-build-status]: https://travis-ci.org/naftulikay/ansible-role-rust-dev.svg?branch=master
 [galaxy]: https://galaxy.ansible.com/naftulikay/rust-dev/
 [rustup]: https://github.com/rust-lang-nursery/rustup.rs
