# Ansible module - `vmware_guest`

Manage VMWare guests virtual machines.

This role can:
* Create virtual machines
* Configure basic guest parameters
* Remove virtual machines

## Tags

| Tag        | Description                       |
|------------|-----------------------------------|
| `setup`    | Create and configure the guest VM |
| `teardown` | Shutdown and delete the guest VM  |

## Variables

To do: Add `vmware_guest_*` variables targeting `vmware_guest` module.

| Variable                         | Type               | Required | Default                                | Description                                                     |
|----------------------------------|--------------------|----------|----------------------------------------|-----------------------------------------------------------------|
| `vmware_sudo_init_sudo_path`     | `string`           | No       | `/etc/sudoers/00-ansible-vmware_guest` | Guest's pre-init `sudoers` file path                            |
| `vmware_guest_validate_certs`    | `bool`             | No       | `False`                                | Check VMWare API certificate nor not                            |
| `vmware_guest_networks`          | `list` of `map`    | No       | `[]` (empty list)                      | List of guest networks                                          |
| `vmware_guest_init`              | `list` or `string` | No       | `[]` (empty list)                      | Guest components to initialize                                  |
| `vmware_guest_init_netplan`      | `map`              | No       | `{}` (empty map)                       | Guest's `netplan` configuration content                         |
| `vmware_guest_init_netplan_path` | `string`           | No       | `/etc/netplan/00-automated.yaml`       | Guest's `netplan` configuration path                            |
| `vmware_guest_hardware`          | `map`              | No       | `{}` (empty map                        | Guest VM hardware                                               |
| `vmware_guest_delegated_host`    | `string`           | No       | `localhost`                            | Host accessing VMWare API (Ansible controller or dedicated node |

