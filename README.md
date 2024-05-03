# Ansible cAdvisor Role

This role installs and configures cAdvisor. cAdvisor is a container monitoring tool that provides container metrics.

## Requirements

None

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

| Variable               | Default Value                                          | Description                            |
| ---------------------- | ------------------------------------------------------ | -------------------------------------- |
| `cadvisor_port`        | `8080`                                                 | The port on which cAdvisor will listen |
| `cadvisor_version`     | `v0.36.0`                                              | The version of cAdvisor to install     |
| `cadvisor_digest`      | `sha256` value                                         | The digest of the cAdvisor image       |
| `cadvisor_arch`        | `amd64`                                                | The architecture of the cAdvisor image |
| `cadvisor_bin_path`    | `/usr/local/bin/cadvisor`                              | The path to the cAdvisor binary        |
| `cadvisor_release_url` | `https://github.com/google/cadvisor/releases/download` | The URL to download cAdvisor from      |

## Dependencies

None

## Example Playbook

```yaml
- hosts: all
  roles:
    - role: cadvisor
```
