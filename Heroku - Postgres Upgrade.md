<h2>1. Get Database info</h2>
$ <b>heroku pg:info</b>
<pre>
=== DATABASE_URL
Plan:        Hobby-dev
Status:      Available
Connections: 0/20
PG Version:  9.5.4
Created:     2016-11-25 18:45 UTC
Data Size:   7.9 MB
Tables:      11
Rows:        26/10000 (In compliance)
Fork/Follow: Unsupported
Rollback:    Unsupported
<b>Add-on:      postgresql-horizontal-86688</b>
</pre>

<h2>2. Provision new database</h2>
$ <b>heroku addons:create heroku-postgresql:</b><em>hobby-dev</em> <b>--app</b> <em>soonerbaptist</em>
<pre>
Creating heroku-postgresql:hobby-dev on ⬢ soonerbaptist... free
Database has been created and is available
 ! This database is empty. If upgrading, you can transfer
 ! data from another database with pg:copy
Created <b>postgresql-asymmetrical-46413</b> as <b><em>HEROKU_POSTGRESQL_BRONZE_URL</em></b>
Use <b>heroku addons:docs heroku-postgresql</b> to view documentation
</pre>

<h2>3. Copy data from old database to new database</h2>
$ <b>heroku pg:copy DATABASE_URL <em>HEROKU_POSTGRESQL_BRONZE_URL</em> --app</b> <em>soonerbaptist</em>
<pre>
 ▸    WARNING: Destructive action
 ▸    This command will remove all data from BRONZE
 ▸    Data from DATABASE will then be transferred to BRONZE
 ▸    To proceed, type <b>soonerbaptist</b> or re-run this command with --confirm
 ▸    soonerbaptist

\><b><em>soonerbaptist</em></b>
Starting copy of <b>DATABASE</b> to <b><em>BRONZE</em></b>... done
Copying... done
</pre>

<h2> 4. Promote new database to be default</h2>
$ <b>heroku pg:promote <em>HEROKU_POSTGRESQL_BRONZE_URL<em> --app</b> <em>soonerbaptist</em>
<pre>
Ensuring an alternate alias for existing DATABASE_URL... <b>HEROKU_POSTGRESQL_YELLOW_URL</b>
Promoting postgresql-asymmetrical-46413 to DATABASE_URL on ⬢ soonerbaptist... done
</pre>

<h2>5. Check app databases</h2>
$ <b>heroku pg:info --app</b> <em>soonerbaptist</em>
<pre>
=== <b>DATABASE_URL, HEROKU_POSTGRESQL_BRONZE_URL</b>
Plan:        Hobby-dev
Status:      Available
Connections: 1/20
<b>PG Version:  9.6.1</b>
Created:     2017-05-31 04:23 UTC
Data Size:   7.8 MB
Tables:      11
Rows:        77/10000 (In compliance)
Fork/Follow: Unsupported
Rollback:    Unsupported
<b>Add-on:      postgresql-asymmetrical-46413</b>

<br>
=== <b>HEROKU_POSTGRESQL_YELLOW_URL</b>
Plan:        Hobby-dev
Status:      Available
Connections: 0/20
<b>PG Version:  9.5.4</b>
Created:     2016-11-25 18:45 UTC
Data Size:   7.9 MB
Tables:      11
Rows:        26/10000 (In compliance)
Fork/Follow: Unsupported
Rollback:    Unsupported
<b>Add-on:      postgresql-horizontal-86688</b>
</pre>
