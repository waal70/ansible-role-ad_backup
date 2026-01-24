ad_backup
=========

This role checks the integrity of your Samba-based AD domain and will perform an online backup.  
Following the steps that are here: [https://wiki.samba.org/index.php/Back_up_and_Restoring_a_Samba_AD_DC]

It will also transfer the backup-file to the ansible controller and (optionally) put it on a network server by ephemerally mounting a samba-share

Role Variables
--------------

```python
smb_username: Administrator
smb_password: "{{ vault_smb_password }}"
backup_path: "/tmp"
backup_max_age: "30d"
smb_backup_share: "//ip-address/backup"
smb_backup_path: "/whateverfolderis/to/follow"
local_backup_path: "/mnt/backup"
vault_smb_password: yourpasswordhere
```

License
-------

[GPLv3](https://www.gnu.org/licenses/gpl-3.0.html#license-text)

Author Information
------------------

Unless otherwise noted, this entire repository is (c) 2024 by André (waal70). [See github profile](https://github.com/waal70)

Please contact me if you need a commercial license for any of these files
