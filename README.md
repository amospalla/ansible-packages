# ansible-packages
* * *

## Description
This role installs packages on Debian, Ubuntu and Centos hosts.

## Variables

Optional:

- _packages_ansible_distribution_: dictionary of lists defining what OS are managed, any other OS/version combination is ignored:
```
packages_ansible_distribution:
  Debian:
    - 7
    - 8
  Ubuntu:
    - ...
  CentOS:
    - ...
```

- _packages_: list of dictionaries defining the packages to be installed:
```
packages:
  - name: logrotate
  - name: vim-enhanced
    Debian:
	  name: vim-nox
	  versions: ['6', '8']
    Ubuntu:
	  disabled: True
```

In this example:
- logrotate is installed on every host.
- vim-enhanced is:
  - installed on all Centos hosts.
  - installed on Debian 6 and 8 using vim-nox name for the package.
  - not installed on an Ubuntu host.
