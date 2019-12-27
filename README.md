# About
Ansible role for SoftEther VPN server

## Example Playbook
```
- hosts: vpnservers
  vars_files:
    - vars/vpn.yml
  roles:
    - { role: lda.ansible-softether-vpn }
```

Inside `vars/vpn.yml`:

```
vpn_ipsec_preshared_key: "SomeSharedKey"
vpn_server_password: "SomeServerPassword"
vpn_users:
  - name: "some.login"
    password: "some.password"
    groups: [users]
vpn_protocols:
  - l2tp_ipsec
```
