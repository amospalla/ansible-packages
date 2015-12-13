This role installs packages on Debian, Ubuntu and Centos hosts.

Those are specified in a list like this:

packages:
  - name: logrotate
  - name: vim-enhanced
    Debian:
	  name: vim-nox
	  versions: ['6', '8']
    Ubuntu:
	  disabled: True

In this example:
- logrotate is installed on every host.
- vim-enhanced is:
  - installed on all Centos hosts.
  - installed on Debian 6 and 8 using vim-nox name for the package.
  - not installed on any Ubuntu host.
