[Heroku PGBackups - Heroku doc](https://devcenter.heroku.com/articles/heroku-postgres-backups)

<b>Logical backups are performed using  

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

$ <b>heroku pg:backups</b> <em>--app forever-family-foundation</em>  
$ <b>heroku pg:backups:url</b> <em>b001 --app sushi</em>   <em>(get specific backup URL)</em>  
<em>then use the URL to download the backup file locally using browser</em>

$ <b>heroku pg:backups:download</b>    <em>(download a backup)</em>  
<em>downloads `latest.dump` to current</em>  


<h1>Create A Backup</h1>
$ <b>heroku pg:backups:capture</b><em>--app sushi</em>


<h1>Schedule A Backup</h1>
To check backup schedule:  
$ <b>heroku pg:backups:schedules <em>--app forever-family-foundation</em></b>
<pre>
=== Backup Schedules
DATABASE_URL: daily at 7:00 UTC
</pre>
