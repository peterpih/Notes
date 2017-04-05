[Heroku PGBackups - Heroku doc](https://devcenter.heroku.com/articles/heroku-postgres-backups)

Logical backups are performed using  

$ <b>pg_dump</b>  

and are high impact,  but save the schema


<h2>Check database size</h2>
$ <b>heroku :pg:info</b> <em>--app sushi</em>
<pre>
=== DATABASE_URL
Plan:        Hobby-dev
Status:      Available
Connections: 2/20
PG Version:  9.5.4
Created:     2016-11-25 18:45 UTC
<b><em>Data Size:   7.9 MB</em></b>
Tables:      10
Rows:        26/10000 (In compliance)
Fork/Follow: Unsupported
Rollback:    Unsupported
Add-on:      postgresql-horizontal-86688
</pre>

<h2>To See The Backups</h2>

$ <b>heroku pg:backups</b> <em>--app forever-family-foundation</em>  <em>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# list backups</em>   
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
