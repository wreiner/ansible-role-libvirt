# libvirt
This role is to setup libvirtd on a host.

## What tasks are performed by this role?
### Set privileged users

To use virt-manager wihtout a password prompt users need to be added to the
groups libvirt and kvm. This should be done by setting the variable
libvirt__privileged_users.

```
libvirt__privileged_users:
  - wreiner
```
