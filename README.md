# odoo-backup-automatic
Create automatic daily backups of your Odoo databases

## Table of contents
  - [Cron](#cron)
  
## Use curl or wget
``curl -X POST -F 'master_pwd=ADMIN_PASSWORD' -F 'name=DB_NAME' -F 'backup_format=zip' -o /backup_dir/back_up_filename.zip http://localhost:8069/web/database/backup``

## Make thi backup.sh executable with chmod:
``sudo chmod +x ~/backup.sh``

## Cron
``crontab -e``

``sudo service cron start``

Create a new cron job which will run each day at 01:30 am

``30 1 * * * /home/<yourusername>/backup.sh``

Every 4 hour
``0 */4 * * * /home/backup.sh``

#### Happy coding 🎉!
