## Cron jobs for ZurmoCRM 2.0.18

For use move file to `/etc/cron.d`

```sh
mv zurmo-cron /etc/cron.d
```

Execute permission

```sh
chmod +x zurmo-cron
```

### Configure user and folder

Edit file

/etc/cron.d/zurmo-cron

Set variables USER and FOLDER

`USERZ`: CRM the User that will perform the task
`USERSYS`: System the user that will perform the cron
`FOLDER`: Folder where you installed the Zurmo
