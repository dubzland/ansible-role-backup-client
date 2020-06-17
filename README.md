# Ansible Role: Backup Client
[![Gitlab pipeline status (self-hosted)](https://git.dubzland.net/dubzland/ansible-role-backup-client/badges/master/pipeline.svg)](https://git.dubzland.net/dubzland/ansible-role-backup-client)

Sets up an rsync-based backup client.  This role is highly opinionated, and
therefore probably not fit for mass consumption.

## Requirements

Ansible version 2.0 or higher.

## Role Variables

Available variables are listed below, along with their default values (see
    `defaults/main.yml` for more info):

### dubzland_backup_client_host

```yaml
dubzland_backup_client_host: "localhost"
```

Rsyncd host to recieve backups.

### dubzland_backup_client_dirs

```yaml
dubzland_backup_client_dirs: []
```

List of directories on the client machine to be backed up.

## Dependencies

None

## Example Playbook

```yaml
- hosts: backup-clients
  become: yes
  roles:
    - role: dubzland-backup_client
      vars:
        dubzland_backup_client_host: "nas01:"
        dubzland_backup_client_dirs:
          - /etc
          - /home
```

## License
-------

MIT

## Author

* [Josh Williams](https://codingprime.com)
