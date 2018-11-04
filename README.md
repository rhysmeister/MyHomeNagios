# MyHomeNagios

A Ansible Role to create Nagios Server for my Home Network. My home network is basically a bunch of Raspberry Pis and a few other devices.

MyHomeNagios
=========

Install Nagios, plugins and associated software and configures some basic checks.

https://www.howtoforge.com/tutorial/install-nagios-4-3-on-debian-9/
 1. Run apt update and apt upgrade.
 2. Reboot if needed. (handler)
 3. Ensure required utilities are installed, i.e. wget unzip zip net-tools.
 4. Install Apache and PHP7.
 5. Configure firewall to allow http and https traffic.
 6. Enable Apache modules. (inc ssl)
 7. Restart Apache if needed (handler?)
 8. Configure PHP.
 9. Restart Apache if needed (handler?)
10. Configure SSL and restart apache if needed.
11. Install tools to compile Nagios from source: autoconf gcc libc6 make apache2-utils libgd-dev.
12. Ensure nagios Linux System user exists.
13. Download Nagios source.
14. Execute Nagios shell script, custom bash script to build Nagios, if required.
15. Ensure Nagios service starts and enabled on boot.
16. Create nagiosadmin http user if required.
17. Using waitfor... wait for the Nagios Server page to be loaded.
18. Ensure libararies for compiling Nagios plugins are installed. i.e. libmcrypt-dev make libssl-dev bc gawk dc build-essential snmp libnet-snmp-perl gettext libldap2-dev smbclient fping default-libmysqlclient-dev
19. Download Nagios Plugins source.
20. Execute Nagios Plugins custom build script if required.
21. Add Nagios Config files and restart Nagios if needed. - TODO
22. Install script to auto-launch browser to full screen at Nagios home page. - TODO

Requirements
------------

- Ansible 2.7+
- Raspian 9.4 Linux plex 4.14.34-v7+ #1110 SMP Mon Apr 16 15:18:51 BST 2018 armv7l GNU/Linux


Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

ansible-playbook -i inventory nagios.yml -u pi --ask-vault-pass

License
-------

BSD

Author Information
------------------

Rhys Campbell - http://github.com/rhysmeister
