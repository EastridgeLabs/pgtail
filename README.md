pgtail
======

Pronounced "pig tail" this python shell script will execute the tail shell command and pipe the output through a filter showing only the log entries matching a specific Postgresql database.

Developer: Eric Goodman

Requirements: Python 2.6+, Postgresql 7+ and a Linux or Mac OS shell

Configuration: Edit postgresql.conf, set the "log_statement" parameter value to 'all' (include single quotes).

Usage:    pgtail <postgresql_log_path> [<database_name>]

Examples:
          pgtail /var/lib/pgsql9/data/pg_log/postgresql-Wed.log invoicedb
          pgtail /var/lib/pgsql9/data/pg_log/postgresql-Wed.log (shows all log entries)