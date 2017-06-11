[How to upgrade PostgreSQL from version 9.5 to version 9.6 without losing data?](https://stackoverflow.com/questions/24379373/how-to-upgrade-postgresql-from-version-9-5-to-version-9-6-without-losing-data)

<b>To check the current version of Postgres locally</b>   
$ <b>`psql -c 'SELECT version();'`</b>
<pre>
                                                     version                                                     
-----------------------------------------------------------------------------------------------------------------
 PostgreSQL 9.4.11 on x86_64-apple-darwin16.4.0, compiled by Apple LLVM version 8.0.0 (clang-800.0.42.1), 64-bit
(1 row)
</pre>

To run **previous version** of PostgreSQL  
<pre>
$ <b>cd /usr/local/Cellar/postgresql/9.4.11/bin</b>   
$ <b>./postgres -D /usr/local/var/postgres</b>   <em># starts program</em>
</pre>

To run the **current** version of PostgreSQL
<pre>
$ <b>cd /usr/local/Cellar/postgres</b>   
$ <b>./postgres -D /usr/local/var/postgres</b>   <em># starts program</em>
</pre>

Brew keeps versions in
<pre>
$ <b>dir /usr/local/Cellar/postgresql</b>
./	../	9.5.5/	9.6.1/	9.6.2/

<b>/usr/local/Cellar/postgresql@9.4/9.4.11/bin</b> 502 >psql
</pre>

For **rake db:migrate** commands to **up** or **down** a database look  
[RubyOnRails Rake](https://github.com/peterpih/Miscellaneous/blob/master/RubyOnRails%20Rake.md)

[PostgreSQL dcumentation](http://www.postgresql.org/docs/9.1/static/sql-altertable.html)

Useful graph of SQL joins: [difference between join and inner join](http://stackoverflow.com/questions/565620/difference-between-join-and-inner-join  )
#PSQL commands
**Show databases**
<pre>
<b>\l</b>                        # list databases letter el

<b>\c</b> <em>database</em>               # connect to a database
<b>\c</b> fff_development

<b>\d</b>                        # list tables
<b>\d+</b> <em>table-name</em>            # list columns of a table
</pre>

###SQL commands
<pre>
<b>SELECT</b> * <b>FROM</b> <em>table</em><b>;</b>                                    # select all rows

<b>UPDATE</b> <em>table</em> <b>SET</b> <em>column=value</em> <b>WHERE</b> <em>id=userid</em><b>;</b>

<b>DELETE</b> <b>FROM</b> <em>table</em> <b>WHERE</b> <em>id=userid</em><b>;</b>      <em>( delete specified row from a table )</em>
<b>DELETE</b> <b>FROM</b> <em>table</em> <b>WHERE</b> <em>=userid</em><b>;</b>      <em>( clear all rows from a table )</em>


<b>SELECT</b> * <b>FROM</b> <em>users</em> <b>WHERE</b> <em>email</em> <b>LIKE</b> <em>'ppih@panix%'</em><b>;</b>     # '%' is the wildcard
<b>SELECT</b> * <b>FROM</b> <em>users</em> <b>WHERE</b> <em>email='ppih@panix%'</em><b>;</b>  

<b>ALTER TABLE</b> <em>table-name</em> <b>RENAME TO</b> <em>new-table-name</em>;  <em>( rename a table )</em>
<b>ALTER TABLE</b> <em>table-name</em> <b>RENAME</b> <em>column-name</em> <b>TO</b> <em>new-column-name</em>;

<b>DROP TABLE</b> <em>table-name</em>
</pre>

<h2>Dump a database</h2>
<pre>
<em>creates dump file of table-name to output-file</em>
<b>pg_dump -t</b> <em>table-name</em> <b>-f</b> <em>output-file  database-name</em>
    
</pre>

<h2>Installing on Mac</h2>

$ <b>brew install postgres</b>

<h2>Download database to local dev</h2>   
<pre>
$ <b>heroku pg:backups:capture</b>    <em># creates a backup</em>   
$ <b>heroku pg:backups:download</b>   <em># downloads back to latest.dump</em>   
</pre>
<h2>Restore to local dev database</h2>
<pre>
$ pg_restore --verbose --clean --no-acl --no-owner -h localhost -U myuser -d mydb latest.dump   
$ <b>pg_restore --verbose --clean --no-acl --no-owner -h localhost -U</b> <em>peterpih</em> <b>-d</b> <em>mom_development</em> <b>latest.dump</b>   
</pre>
