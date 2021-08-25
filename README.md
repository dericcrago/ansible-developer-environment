# Ansible Developer Environment

A quick start role for getting your Ansible Developer Environment ready. This role will install Docker, Python (version is configurable), VS Code, and Ansible. See the configuration details [below](#Role-Variables).

## Requirements

A recent Fedora or Ubuntu environment (maybe a VM if you're looking for a clean separation).

## Role Variables

| Variable               | Default Value | Description                                                                                   |
| ---------------------- | ------------- | --------------------------------------------------------------------------------------------- |
| `install_docker`       | `true`        | Whether or not to install Docker                                                              |
| `install_python`       | `true`        | Whether or not to install the Python version specified by the `pyenv_python_version` variable |
| `install_vscode`       | `true`        | Whether or not to install VS Code                                                             |
| `install_ansible`      | `false`       | Whether or not to install Ansible                                                             |
| `pyenv_python_version` | `3.9.6`       | What version of Python to install if `install_python` is `true`                               |

## Dependencies

- None

## Example Playbook

```yaml
---
- hosts: all
  roles:
    - role: ansible-developer-environment
      vars:
        install_ansible: true
```

## License

BSD-3-Clause

## Author Information

Deric Crago
