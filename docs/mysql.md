### Backup DB with GZ

`mysqldump -u user_name -p  db_name  | gzip > backup.sql.gz`

### Restore DB from GZ backup

`gunzip < backup.sql.gz | mysql -u user_name -p db_name`

### Restore DB from sql backup

mysql -u root -p dbname < dump.sql

### Add prefix for all emails in the table

`UPDATE  `table` SET email = CONCAT(  'prefix_', email );`