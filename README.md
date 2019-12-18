# vpn_test

## Get started
- Define your VPN credentials as environment variables:

```
# All values MUST be placed inside 'single quotes'
# DO NOT use these special characters within values: \ " '
wget https://git.io/vpnsetup -O vpnsetup.sh && sudo \
VPN_IPSEC_PSK='your_ipsec_pre_shared_key' \
VPN_USER='your_vpn_username' \
VPN_PASSWORD='your_vpn_password' \
sh vpnsetup.sh
```

## useful command
- restart:
```bash
sudo service ipsec restart && sudo service xl2tpd restart
```
- traffic:
```bash
sudo ipsec whack --trafficstatus
```

- log:
```bash
tail -F /var/log/auth.log | grep pluto
```

- status:

```bash
sudo ipsec status
sudo ipsec verify
```
- userlist:
```bash
sudo vim /etc/ppp/chap-secrets
```

- add:
```bash
sudo sh add_vpn_user.sh 'username_to_add' 'password_to_add'
```

- delete:
```bash
sudo sh del_vpn_user.sh 'username_to_delete'
```
# source:
https://github.com/hwdsl2/setup-ipsec-vpn/blob/master/docs/manage-users-zh.md

https://elephantnose.github.io/2018/09/24/10%E5%88%86%E9%92%9F%E6%95%99%E4%BD%A0%E7%94%A8%20Google%20Cloud%20Platform%20%E6%90%AD%E5%BB%BA%E8%87%AA%E5%B7%B1%E7%9A%84VPN/

https://github.com/hwdsl2/setup-ipsec-vpn/blob/master/README-zh.md#%E9%87%8D%E8%A6%81%E6%8F%90%E7%A4%BA
