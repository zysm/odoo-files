Docker https://labs.play-with-docker.com/

```
git clone  https://github.com/zysm/odoo-files.git
cd odoo-files
unzip om_account_accountant-17.0.2.0.2.zip
rm om_account_accountant-17.0.2.0.2.zip
```


Start a PostgreSQL server

```$ docker run -d -e POSTGRES_USER=odoo -e POSTGRES_PASSWORD=odoo -e POSTGRES_DB=postgres --name db postgres:15```


```$ docker run -v /root/odoo-files:/mnt/extra-addons -p 8069:8069 --name odoo --link db:db -t odoo```


Activate the Developer Mode, then click ‘Update Apps List’ on the Apps page menu bar. Wait until Odoo successfully updates modules lists.

