ansible-rhel-logging
--------------------

Ansible Role for configuring Logging on RHEL

### Requirements & Dependencies
- Ansible >= 2.10
- Ansible <= 2.16 when configuring remote RHEL8 Hosts

#### Operating systems
- Red Hat Enterprise Linux >= 8

### Example Playbook
```
- name: Configure Logging on Red Hat Enterprise Linux
  hosts: all
  become: true

  vars:
    selinux_enabled: true
  
  roles:
    - ansible-rhel-logging
  
```

### Variables
- See `defaults/main.yml`

### Troubleshooting & Known issues

- As auditd is linked to the kernel, the role will not work on container images

License
-------
MIT

Author Information
------------------

[Chad Zimmerman](https://github.com/PrymalInstynct)