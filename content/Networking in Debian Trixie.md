---
tags:
  - cli
  - internet
created: 2026-03-01
modified: 2026-03-01
---
Debian 13 (Trixie) ships with NetworkManager which the author struggles to utilise in the command line. The classical network configuration through `/etc/network/interfaces` still works.

NetworkManager can be configured through the file at `/etc/NetworkManager/system-connections`. It appear in the author's current implementation, the system must be rebooted for changes to take effect; reloading the daemons doesn't work...

`resolv.conf` contains the DNS nameservers. It is managed by NetworkManager.

# Further reading
 - The man pages