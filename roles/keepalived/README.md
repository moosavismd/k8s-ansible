# KeepAlived Setup Role

Install And configure `keepalived` package.

### Vars

```yaml
local_interface: eth0
target_interface: eth1
router_id: 78   # It should be UNIQUE
virtual_ip: 1.1.1.1
keepalived_password: "keepalived_simple_password"
```
