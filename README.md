# Ansible Role: libvirt

This role is to setup libvirtd on a host.

## Mandatory Role Variables

None.

## Optional Role Variables

To use virt-manager wihtout a password prompt users need to be added to the
groups libvirt and kvm. This should be done by setting the variable
libvirt\_\_privileged_users.

```
libvirt__privileged_users:
  - someuser
```

To use a bridged network for the virtual machines it is possible to define the
bridge interface for which a network called _bridged_network_ will be created:

```
libvirt__bridge_interface: br0
```

To automatically add filesystem storage pools of premounted filesystems it is 
possible to add an array of names and paths:

```
libvirt__fs_pools:
  - name: iso_base
    target_path: "/var/lib/libvirt/iso_base"
  - name: vmpool01
    target_path: "/var/lib/libvirt/vmpool01"
```
