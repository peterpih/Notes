<h2>On Local Machine</h2>
<b>To get the current database version number</b>   

$ psql   
\# SELECT version();  
<pre>
                                                    version                                                     
-----------------------------------------------------------------------------------------------------------------
<b>PostgreSQL 9.4.11</b> on x86_64-apple-darwin16.4.0, compiled by Apple LLVM version 8.0.0 (clang-800.0.42.1), 64-bit
(1 row)

</pre>

<h2>Initialize new database</h2>
$ initdb /usr/local/var/postgres9.6 -E utf8 --locale
<pre>
The files belonging to this database system will be owned by user "peterpih".
This user must also own the server process.

The database cluster will be initialized with locale "en_US.UTF-8".
The default text search configuration will be set to "english".

Data page checksums are disabled.

creating directory /usr/local/var/postgres9.6 ... ok
creating subdirectories ... ok
selecting default max_connections ... 100
selecting default shared_buffers ... 128MB
selecting dynamic shared memory implementation ... posix
creating configuration files ... ok
running bootstrap script ... ok
performing post-bootstrap initialization ... ok
syncing data to disk ... ok

WARNING: enabling "trust" authentication for local connections
You can change this by editing pg_hba.conf or using the option -A, or
--auth-local and --auth-host, the next time you run initdb.

Success. You can now start the database server using:
  pg_ctl -D /usr/local/var/postgres9.6 -l logfile start
</pre>

<h2>Run the Upgrade</h2>
<pre>
pg_upgrade -v \
    -d /usr/local/var/postgres \
    -D /usr/local/var/postgres9.6 \
    -b /usr/local/Cellar/postgresql/9.4.11/bin/ \
    -B /usr/local/Cellar/postgresql/9.6.2/bin/
    
    -d old directory   
    -D new directory   
    -b old binary/executable  
    -B new binary/executable   
<pre>

Rename the Database Directory
$ cd /usr/local/var
mv postgres postgres9.4
mv postgres9.6 postgres
