The official Net-SNMP Perl module only supports SHA1 protocol. Newer SHA protocols, such as SHA256 or SHA512 are not supported. 
See https://www.claudiokuenzler.com/blog/1205/how-to-perl-net-snmp-v3-authentication-protocol-support-newer-sha-sha256-sha512 and also https://www.claudiokuenzler.com/blog/1167/snmp-v3-monitoring-authentication-sha1-not-working-checkpoint-gaia-r81. 

There is however a manual patch available:  https://www.mail-archive.com/ports@openbsd.org/msg106148.html

The USM.pm file in this repository is such a manually patched version, supporting newer SHA protocols for SNMPv3 authentication.
Make a backup of your existing USM.pm (**/usr/share/perl5/Net/SNMP/Security/USM.pm**) and replace it with this file.

Successfully tested on Ubuntu 20.04.
