OpenShift Online GateIn Cartridge
=================================

Version 0.0.3 for OpenShift Online
Approach to use a .zip distribution downloaded from jboss repository.

Databases
---------

Tested with mysql cartridge.
Tested with postgresql-8.4 cartridge.
Not supported with postgresql-9.2 cartridge.

Usage
-----

From GateIn rhc command line tool:

rhc create-app mygatein https://raw.github.com/lucasponce/openshift-online-cartridge-gatein/master/metadata/manifest.yml

Where "mygatein" is your app name in your openshift domain.

Adding databases to your GateIn cartridge
------------------------------------------

Add a mysql cartridge

rhc cartridge add mysql-5.1 --app mygatein
rhc app restart mygatein

or add a postgresql-8.4 cartridge

rhc cartridge add postgresql-8.4 --app mygatein
rhc app restart mygatein