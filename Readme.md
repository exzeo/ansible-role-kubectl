Role Name
=========

Installs kubectl Command Line Interface on Debian/Ubuntu servers. 

Description
===========
```
# This will download the binary straight to directory. The role will auto-detect OS. 
```

Role Variables
--------------
```
# Version of 'kubectl' to install.
kubectl_version: "1.21.2"

# Toggling this will uninstall from the server
uninstall: "false"

# Where to install "kubectl" binary
kubectl_bin_directory: "/usr/local/bin"
```

Example Playbooks
----------------

Minimal:
```
- name: Install CLI
  hosts: all
  roles:
    - role: kubectl
```

Specific Version:
```
- name: Install CLI
  hosts: all
  roles:
    - role: kubectl
      vars:
        kuebctl_version: "1.23.2"
```

Uninstall:
```
- name: Install CLI
  hosts: all
  roles:
    - role: kubectl
      vars:
        uninstall: true
```
