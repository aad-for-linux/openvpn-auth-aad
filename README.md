# openvpn-auth-aad

[![GPL-2.0-only](https://img.shields.io/badge/license-GPL--2.0--only-blue?style=flat-square)](https://spdx.org/licenses/GPL-2.0-only.html)
[![GitHub Actions](https://img.shields.io/github/workflow/status/aad-for-linux/openvpn-auth-aad/build?style=flat-square)](https://github.com/aad-for-linux/openvpn-auth-aad/actions)

_Azure Active Directory (AAD) OpenVPN Plugin._

## Installation

```terminal
./bootstrap.sh
make
sudo make install
```

## Configuration

Edit `/etc/openvpn/server/server.conf` and add the following lines:

```txt
plugin /usr/lib/openvpn/plugins/openvpn-auth-aad.so
client-cert-not-required
username-as-common-name
```

Note: A valid [pam_aad configuration file](https://github.com/aad-for-linux/pam_aad#configuration-file) is also required.

## See also

- https://github.com/fac/auth-script-openvpn
- https://github.com/mozilla-it/openvpn_defer_auth
