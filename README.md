tower
=========

Install Ansible Tower on a single server.

Requirements
------------

- Proper RHEL subscription to access the repositories needed
- The resulting installation will require a license to be useable. This role does not deal with that

Role Variables
--------------

| Variable        | Required | Default  | Description                                                                                                                                                                                                                                     |
| --------------- | -------- | -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `domain` | :x:      | ```example.com``` | The Domain for the environment |
| `disconnected` | :x:      | ```false``` | Boolean specifying whether the environment is disconnected or not |
| `tower_hostname` | :x:      | ```tower``` | The short hostname for the system |
| `tower_public_ip` | :heavy_check_mark:      |  | The reachable public IP for the VM |
| `tower_pwd` | :x:      | ```p@ssw0rd``` | The password for admin user in Tower |
| `tower_repos` | :x:      | ```see defaults/main.yml``` | List of repositories required for install |

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: tower
  vars:
    tower_public_ip: 192.168.1.80
  tasks:
    - name: Install Tower
      include_role:
        name: RedHatGov.tower
```

License
-------

GPLv3

Author Information
------------------

[Red Hat North American Public Sector Solution Architects](https://redhatgov.io)
