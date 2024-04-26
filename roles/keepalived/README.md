# KeepAlived Setup Role

Install And configure `keepalived` package.

## Vars

```yaml
interface_name: eth1
router_id: 78   # It should be UNIQUE
virtual_ip: 1.1.1.1
keepalived_password: "keepalived_simple_password"
```

## Tags
- `keepalived`: Runs the whole role.  
