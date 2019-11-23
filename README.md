# vpn_test

## useful command
- restart:
sudo service ipsec restart && sudo service xl2tpd restart

- traffic:
sudo ipsec whack --trafficstatus

- log:
tail -F /var/log/auth.log | grep pluto

- status:
sudo ipsec status
sudo ipsec verify

- userlist:
sudo vim /etc/ppp/chap-secrets

- add:
sudo sh add_vpn_user.sh 'username_to_add' 'password_to_add'

- delete:
sudo sh del_vpn_user.sh 'username_to_delete'

# source:
https://github.com/hwdsl2/setup-ipsec-vpn/blob/master/docs/manage-users-zh.md
https://elephantnose.github.io/2018/09/24/10%E5%88%86%E9%92%9F%E6%95%99%E4%BD%A0%E7%94%A8%20Google%20Cloud%20Platform%20%E6%90%AD%E5%BB%BA%E8%87%AA%E5%B7%B1%E7%9A%84VPN/
https://github.com/hwdsl2/setup-ipsec-vpn/blob/master/README-zh.md#%E9%87%8D%E8%A6%81%E6%8F%90%E7%A4%BA
