ansible-rhel-logging
--------------------

Ansible Role for configuring Logging on RHEL

### Requirements & Dependencies
- Ansible >= 2.10

#### Operating systems
- Red Hat Enterprise Linux >= 8

### Example Playbook

Just include this role in your list.
For example

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

- As auditd is linked to the kernel, role will not affect containers.

### References

* https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/Security_Guide/chap-system_auditing.html
* https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/Security_Guide/sec-starting_the_audit_service.html
* https://github.com/bfuzzy/auditd-attack
* https://github.com/Neo23x0/auditd/

License
-------

MIT

Author Information
------------------

[Chad Zimmerman](https://github.com/PrymalInstynct)