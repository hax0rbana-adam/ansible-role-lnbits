A simple role to install LNBits on Debian. This has only been tested with the
LND (GRPC) backend wallet.

After this playbook runs, the service will be running but you'll need to create
an administrative account. After that's done, you can install Extensions such
as LndHub to access LNbits from mobile wallets such as BlueWallet or Zeus.

# Variables

See defaults/main.yml for the variables and an explanation as to what they do.

# Examples
## Playbook
Here's an example of a playbook to install Lemur on the local machine. It does
not require you have SSH running.

```yaml
- hosts: localhost
  connection: local
  become: true
  roles:
    - role: hax0rbana_adam.lnbits
```

To make a playbook to run this role on a remote host:

```yaml
- hosts: all
  remote_user: root
  roles:
    - role: hax0rbana_adam.lnbits
```

# Official repo location
All activity takes place on the official GitLab instance:
[https://gitlab.hax0rbana.org/public-repos/ansible/lnbits](https://gitlab.hax0rbana.org/public-repos/ansible/lnbits)

Any other hosting providers, such as GitHub.com and GitLab.com, are just mirrors
and we do not monitor the issue trackers over there.

# Support
## Matrix channel
You can also join our Matrix channel: #ansible:hax0rbana.org

This is a good place to ask questions or make requests without having to sign
up for another account.

# Contributing
See [contributor guidelines](CONTRIBUTING.md).

# License
This project is licensed under MIT License. See [LICENSE](LICENSE) for more details.
