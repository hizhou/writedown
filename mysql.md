
## Tool

### mysql

**-e** Execute command and quit. (Disables --force and history file.)
>mysql -hlocalhost -uroot -e "show databases";

>mysql -hlocalhost -uroot mysql -e "show tables";

**--prompt** Set the mysql prompt to this value.
>mysql -uroot --prompt="\u@\h : \d \r:\m:\s>"

**--tee** Append everything into outfile.
>mysql -uroot --tee=E:\record.txt

### mysqladmin

**ping**  Check if mysqld is alive.
>mysqladmin -uroot ping

**status** Gives a short status message from the server.
>mysqladmin -uroot status

**processlist** Show list of active threads in server.
>mysqladmin -uroot processlist

### mysqlimport
Loads tables from text files in various formats.  The base name of the text file must be the name of the table that should be used.

>mysqlimport -uroot test E:\some.txt


### mysqlbinlog
Dumps a MySQL binary log in a format usable for viewing or for piping to the mysql command line client.

>mysqlbinlog E:\amp\mysql\data\mysql-bin.000055

### mysqlcheck

This program can be used to CHECK (-c, -m, -C), REPAIR (-r), ANALYZE (-a), or OPTIMIZE (-o) tables.

>mysqlcheck -uroot mysql

### myisamchk

Description, check and repair of MyISAM tables.

>myisamchk E:\amp\mysql\data\mysql\user
>
>myisamchk E:\amp\mysql\data\mysql\user.MYI


## Optimize

### profiling

check the bottleneck in IO or CPU

> set profiling=1;

> //do some query

> show profiles;

> show profile cpu , block io for query 1;

### explain
