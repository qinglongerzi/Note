- slow log

**AWS parameter group**

shared_preload_libraries = 'pg_stat_statements'

pg_stat_statements.max = 2048

**login postgresql**

=> create extension pg_stat_statements;

=> \dx

=> \d pg_stat_statements

**export to csv** 

psql96 -c "copy (select * from pg_stat_statements) to stdout with DELIMITER ',' csv header;" -h hostname -p port -U user -d postgres > sql_query_log.csv


**ref**
https://blog.dbi-services.com/sql-monitoring-in-postgresql-2-pg_stat_statements/
