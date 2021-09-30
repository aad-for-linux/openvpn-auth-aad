# openvpn-auth-aad [![Build Status][![GPL-2.0-only][gpl-badge]][gpl-license] [![Download]

_Azure Active Directory (AAD) OpenVPN Plugin_

## Installation

```terminal
./bootstrap.sh
make
sudo make install
```

## Configuration

Edit `/etc/openvpn/server.conf` and add the following lines:

```txt
plugin /usr/lib/openvpn/openvpn-auth-aad.so
client-cert-not-required
username-as-common-name
```

Note: A valid [pam_aad configuration file](https://github.com/CyberNinjas/pam_aad#configuration-file) is also required.

## See also

- https://github.com/fac/auth-script-openvpn
- https://github.com/mozilla-it/openvpn_defer_auth

[gpl-badge]: https://img.shields.io/badge/license-GPL-green.svg
[gpl-license]: COPYING
