# Ansible Role: Backup Client
[![Gitlab pipeline status (self-hosted)](https://img.shields.io/gitlab/pipeline/dubzland/ansible-role-backup-client/main?gitlab_url=https%3A%2F%2Fgit.dubzland.net)](https://git.dubzland.net/dubzland/ansible-role-backup-client/pipelines)
[![Ansible role](https://img.shields.io/ansible/role/50081)](https://galaxy.ansible.com/dubzland/backup_client)
[![Ansible role downloads](https://img.shields.io/ansible/role/d/50081)](https://galaxy.ansible.com/dubzland/backup_client)
[![Ansible Quality Score](https://img.shields.io/ansible/quality/50081)](https://galaxy.ansible.com/dubzland/backup_client)
[![Liberapay patrons](https://img.shields.io/liberapay/patrons/jdubz)](https://liberapay.com/jdubz/donate)
[![Liberapay receiving](https://img.shields.io/liberapay/receives/jdubz)](https://liberapay.com/jdubz/donate)

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

MIT

## Author

* [Josh Williams](https://codingprime.com)
