# Ansible Role to patch rsyslog.conf

[![Build Status](https://travis-ci.org/nerab/ansible-role-rsyslog-patch.svg?branch=master)](https://travis-ci.org/nerab/ansible-role-rsyslog-patch)

As described in this [commit](https://anonscm.debian.org/cgit/collab-maint/rsyslog.git/commit/?id=67bc8e5326b0d3564c7e2153dede25f9690e6839), rsyslog spams the syslog due to an unresolved bug. This Ansible role patches the default `rsyslog.conf` to correct this issue.

# TODO

* Check that the symptoms are gone:

  ```bash
  sudo grep "rsyslogd-2007: action 'action 17' suspended," /var/log/syslog
  ```

  must not show a line with a timestamp later than when we applied this patch.
