# openvpn
### Installation

```sh
dpkg -i openvpn.deb
```

```sh
cp pyovpn-2.0-py2.7.egg /usr/local/openvpn_as/lib/python2.7/site-packages/pyovpn-2.0-py2.7.egg
```

### Configuration

```sh
/usr/local/openvpn_as/scripts/sacli --key "auth.module.type" --value "local" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "vpn.server.daemon.enable" --value "false" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "vpn.daemon.0.listen.protocol" --value "udp" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "vpn.server.port_share.enable" --value "false" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "vpn.server.daemon.udp.port" --value "1194" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "vpn.server.tls_version_min" --value "1.2" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "vpn.server.tls_auth" --value "true" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "vpn.tls_refresh.interval" --value "720" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "vpn.server.lockout_policy.n_fails" --value "5" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "vpn.server.lockout_policy.reset_time" --value "60" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "vpn.server.lockout_policy.max_history" --value "1024000" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "cs.tls_version_min" --value "1.2" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "xmlrpc.relay_level" --value "1" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "vpn.daemon.0.server.ip_address" --value "all" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "vpn.daemon.0.listen.ip_address" --value "all" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "admin_ui.https.port" --value "443" ConfigPut
/usr/local/openvpn_as/scripts/sacli --key "cs.https.port" --value "443" ConfigPut
/usr/local/openvpn_as/scripts/sacli start
```
