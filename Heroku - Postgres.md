<h2>To find Postgres version of database</h2>   
$ <b>heroku pg:psql -c 'SELECT version();'</b>
<pre>
                                             version                                             
-------------------------------------------------------------------------------------------------
<b>PostgreSQL 9.5.4</b> on x86_64-pc-linux-gnu, compiled by gcc (Ubuntu 4.8.2-19ubuntu1) 4.8.2, 64-bit
(1 ro
</pre>

[Heroku PGBackups - Heroku doc](https://devcenter.heroku.com/articles/heroku-postgres-backups)

Logical backups are performed using  

$ <b>pg_dump</b>  

and are high impact,  but save the schema


<h2>Check database size</h2>
$ <b>heroku :pg:info</b> <em>--app sushi</em>
<pre>
=== DATABASE_URL
<b>Plan:        Hobby-dev</b>
Status:      Available
Connections: 2/20
<b>PG Version:  9.5.4</b>
Created:     2016-11-25 18:45 UTC
<b><em>Data Size:   7.9 MB</em></b>
Tables:      10
Rows:        26/10000 (In compliance)
Fork/Follow: Unsupported
Rollback:    Unsupported
<b>Add-on:      postgresql-horizontal-86688</b>
</pre>

<h2>To See The Backups</h2>

$ <b>heroku pg:backups</b> <em>--app forever-family-foundation</em>  <em>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# list backups</em>   
<pre>
=== Backups
ID     Created at                 Status                               Size      Database
─────  ─────────────────────────  ───────────────────────────────────  ────────  ────────
a739   2017-05-28 07:13:22 +0000  Completed 2017-05-28 07:13:55 +0000  1.80MB    AMBER
a738   2017-05-27 07:13:43 +0000  Completed 2017-05-27 07:13:57 +0000  1.80MB    AMBER
a737   2017-05-26 07:13:41 +0000  Completed 2017-05-26 07:13:45 +0000  1.80MB    AMBER
a736   2017-05-25 07:15:22 +0000  Completed 2017-05-25 07:15:47 +0000  1.80MB    AMBER
a735   2017-05-24 07:13:57 +0000  Completed 2017-05-24 07:14:26 +0000  1.78MB    AMBER
a734   2017-05-23 07:18:06 +0000  Completed 2017-05-23 07:18:10 +0000  1.78MB    AMBER
a733   2017-05-22 07:18:34 +0000  Completed 2017-05-22 07:18:35 +0000  1.78MB    AMBER
a732   2017-05-21 07:18:01 +0000  Completed 2017-05-21 07:18:03 +0000  1.78MB    AMBER
b304   2016-03-20 03:41:41 +0000  Failed 2016-03-20 03:41:41 +0000     0.00B     AMBER
b056   2015-07-15 02:31:13 +0000  Completed 2015-07-15 02:31:15 +0000  1.26MB    AMBER
ob025  2014-07-04 00:12:54 +0000  Completed 2014-07-04 00:13:01 +0000  976.56kB  AMBER
ob002  2014-01-16 16:18:16 +0000  Completed 2014-01-16 16:18:21 +0000  891.41kB  ONYX
ob001  2014-01-14 05:10:20 +0000  Completed 2014-01-14 05:10:28 +0000  176.56kB  ONYX

=== Restores
No restores found. Use heroku pg:backups:restore to restore a backup

=== Copies
No copies found. Use heroku pg:copy to copy a database to another

</pre>

$ <b>heroku pg:backups:capture:</b> <em>--app forever-family-foundation</em>     <em>make a backup</em>
<pre>
Starting backup of glowing-idly-1982... done

Use Ctrl-C at any time to stop monitoring progress; the backup will continue running.
Use heroku pg:backups:info to check progress.
Stop a running backup with heroku pg:backups:cancel.

Backing up AMBER to b740... done
</pre>
$ <b>heroku pg:backups:url</b> <em>b001 --app sushi</em> <em>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# get specific backup URL</em>   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<em>then use the URL to download the backup file locally using browser</em>

$ <b>heroku pg:backups:download</b>    <em>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;#download a backup</em>   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<em>downloads `latest.dump` to <b>current local directory</b></em>  

$ <b>heroku pg:copy</b> <em>sushi::ORANGE GREEN --app sushi-staging</em>  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<em>This would copy data from the ORANGE database of the sushi app to the GREEN database in sushi-staging.   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This could be used to copy production data into a staging app for testing purposes.</em>


<h1>Create A Backup</h1>   

$ <b>heroku pg:backups:capture</b><em>--app sushi</em>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<em># creates a backup</em> 

$ <b>heroku pg:backups</b><em>--app sushi</em>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<em># list backups</em> 
<pre>
=== Backups
ID    Created at                 Status                               Size     Database
────  ─────────────────────────  ───────────────────────────────────  ───────  ────────
b001  2017-03-29 18:16:49 +0000  Completed 2017-03-29 18:16:51 +0000  20.11kB  DATABASE
</pre>

<h1>Schedule A Backup</h1>
To check backup schedule:  

$ <b>heroku pg:backups:schedules</b> <em>--app forever-family-foundation</em>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<em># schedules a backup</em> 
<pre>
=== Backup Schedules
DATABASE_URL: daily at 7:00 UTC
</pre>

<h1>Restore a backup (after downloading)</h1>   
from: https://devcenter.heroku.com/articles/heroku-postgres-import-export   

After <b>heroku pg:backups:download</b>   

$ <b>pg_restore --verbose --clean --no-acl --no-owner -h localhost -U</b> <em>myuser</em> <b>-d</b> <em>mydb</em> <b>latest.dump</b>  

Will restore the Heroku database to the local database
