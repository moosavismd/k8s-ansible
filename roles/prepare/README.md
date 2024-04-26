# Prepare servers ansible role  
Thist role prepares node for kubernetes cluster installation and installs some necessary packages on it.  

## Vars

```yaml
set_custom_dns: false # Set custom dnsnameserver in /etc/resolv.conf or not
custom_dns_list:
  - 4.2.2.4
  - 8.8.8.8
prepare_allow_restart: true # Allow the role to reboot the server after some changes or not. 
upgrade_all_packages: true # Allow the role to upgrade all packages
```


## Tags
- `prepare`: If you use this tag, the whole role will be applied.  
- `upgrade_all_packages` : Uses apt upgrade to upgrade all of the OS packages to latest version.    
- `prepare_change_dns`: This only changes the dns nameservers to custom servers.  
- `install_packages`: Installs the nessaccary packages.  
- `prepare_sysctl_conf`: Changes some configurations like number of open files and file limits.  
- `disable_auto_upgrades`: Disbale auto upgrade in ubuntu.  
- `prepare_unmount_swap`: Disable swap.  
