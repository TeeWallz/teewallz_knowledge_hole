# Why is backup & restore such a shit show? 

Source: https://www.reddit.com/r/PostgreSQL/comments/fxxnyt/why_is_backup_restore_such_a_shit_show/

> * pg_restore can't handle plain SQL backups, but
> * pg_dump doesn't include role privileges, but
> * pg_dumpall only emits plain SQL backups, but
> * psql doesn't know to drop databases prior to running plain SQL backups, but
> ...
> 
> How are we supposed to actually backup and restore, 100%, bit for bit, a  PostgreSQL database?
> 
> **Update**
> 
> The trick is to use pg_dumpall with the --clean / -c flag, then restore with  psql -f. Why PostgreSQL has any other defaults or applications for this, I > will never understand.
> 
> https://gist.github.com/mcandre/ea2f82249c71126b8d6605e229b33407

# POSTGRESQL BACKUP AND RESTORE

```console
$ pg_dumpall --clean -U <user> -f backup.sql
$ psql -U <user> -f backup.sql
```

## Warnings

* A PostgreSQL user with administrative privileges is required.
* Using `pg_dump` instead of `pg_dumpall` results in role privileges being reset to nothing.
* If you forget the `--clean` / `-c` flag to `pg_dumpall`, then the backup SQL script will not be idempotent, and will collide and error with any existing databases.
* Using `pg_restore` instead of `psql` will reject the plain SQL backup format.

# Other recommendation
https://pgbackrest.org/