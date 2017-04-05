# Automatic System Updates

Configure automatic updates on Debian-based or RedHat-based distributions.

## Requirements

There are no prerequisites for this role. It will install the required auto-update mechanisms and configure them.

## Role Variables

### Debian

``` yaml
apticron_email: root
periodic_update_package_lists: 1
periodic_download_upgradable_packages: 1
periodic_autoclean_interval: 7
periodic_unattended_upgrade: 1
unattended_upgrades_allowed_origins: []
unattended_upgrades_blacklist: []
unattended_upgrades_auto_fix_inturrupted_dpkg: "true"
unattended_upgrades_minimal_steps: "false"
unattended_upgrades_install_on_shutdown:  "false"
unattended_upgrades_mail: {{ apticron_email }}
unattended_upgrades_mail_only_on_error: "true"
unattended_upgrades_remove_unused_dependencies: "true"
unattended_upgrades_automatic_reboot: "false"
unattended_upgrades_automatic_reboot_time: "now"
unattended_upgrades_bandwidth_limit: ""
```

### RedHat

``` yaml
```

## Dependencies

There are no dependencies.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: rvalente.autoupdate }

## License

See `LICENSE`

## Author Information

Ronald Valente
