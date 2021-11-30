# Ubuntu

## Dependencies

To install on Ubuntu, the following personal package archives (PPAs),
must be installed:

- [Simple Dynamic Strings][sds-ppa]
- [Azure Active Directory for Linux][aad-for-linux-ppa]

These can be installed via the following commands:

```terminal
# Simple Dynamic Strings
add-apt-repository ppa:lramage/sds

# Azure Active Directory for Linux
add-apt-repository ppa:aad-for-linux/ppa
```

Note: __Both__ PPA's must be installed in order for all of the dependencies to be met.

## Installation

```terminal
apt update && apt install -y openvpn-auth-aad
```

## Configuration

This package depends on [libpam-aad][libpam-aad-ubuntu-config],
which should automatically install the required configuration files.

## Troubleshooting

If `add-apt-repository` is missing from your system, i.e., a docker image,
it can be installed via the following command:

```terminal
apt install -y software-properties-common
```

If the key for the PPA fails to import properly,
it can be manually added via the following command:

```terminal
# Simple Dynamic Strings
apt-key adv --keyserver keyserver.ubuntu.com --recv A2C0BCEBD63BA8C1
```

[aad-for-linux-ppa]: https://launchpad.net/~aad-for-linux/+archive/ubuntu/ppa
[libpam-aad-ubuntu-config]: https://github.com/aad-for-linux/pam_aad/blob/master/doc/ubuntu.md#configuration
[sds-ppa]: https://launchpad.net/~lramage/+archive/ubuntu/sds
