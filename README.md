# Automatic System Updates

[![Build Status](https://travis-ci.org/rvalente/ansible-role-autoupdate.svg?branch=master)](https://travis-ci.org/rvalente/ansible-role-autoupdate)

Configure automatic updates on Debian-based or RedHat-based distributions.

## Requirements

There are no prerequisites for this role. It will install the required auto-update mechanisms and configure them.

## Role Variables

### Main Variables

``` yaml
autoupdate_notification_email: root
```

### Debian

Variables specific to Debian.

``` yaml
autoupdate_update_package_lists: 1
autoupdate_download_upgradable_packages: 1
autoupdate_autoclean_interval: 7
autoupdate_unattended_upgrade: 1
autoupdate_allowed_origins: []
autoupdate_blacklist: []
autoupdate_auto_fix_inturrupted_dpkg: "true"
autoupdate_minimal_steps: "false"
autoupdate_install_on_shutdown:  "false"
autoupdate_mail: "{{ autoupdate_notification_email }}"
autoupdate_mail_only_on_error: "true"
autoupdate_remove_unused_dependencies: "true"
autoupdate_automatic_reboot: "false"
autoupdate_automatic_reboot_time: "now"
autoupdate_bandwidth_limit: ""
```

### RedHat

Variables specific to RedHat.

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
