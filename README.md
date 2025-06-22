# ansible-role-sd-mux-ctrl

Ansible Role -- Build and Install sd-mux-ctrl for SD-Wire

An Ansible Role that builds and installs `sd-mux-ctrl`.

## Requirements


## Role Variables

Available variables are listed below, along with default values (see 'defaults/main.yaml'):

```yaml
sdmuxctrl_build_deps_are_installed: false
sdmuxctrl_is_cloned: false
sdmuxctrl_is_built: false
sdmuxctrl_is_upgraded: false
sdmuxctrl_group_is_installed: false
sdmuxctrl_extra_packages_are_installed: false
sdmuxctrl_runtime_deps_are_installed: false
```

Variables which control the Debian installation are listed below (see `vars/Debian.yml`):

```yaml
sdmuxctrl_runtime_dependencies:
sdmuxctrl_build_dependencies:
sdmuxctrl_repo_url:
sdmuxctrl_version:
sdmuxctrl_package_name:
sdmuxctrl_extra_packages:
```

## Example Playbook

Example playbook for a `labgrid-exporter`:

```yaml
    - hosts: exporters
      gather_facts: yes
      become: yes

    vars:
    # Uncomment the following to skip build and installation
    #sdmuxctrl_is_built: true
    #sdmuxctrl_is_upgraded: true

    tasks:
    - name: Include the sdmuxctrl role
      ansible.builtin.include_role:
        name: sdmuxctrl
```

## License

Apache-2.0

## Author Information

The role was created in 2025 by (moto-timo)[https://github.com/moto-timo/].
