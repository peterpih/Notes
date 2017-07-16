<h2>Scedule the backup</h2>

$ <b>heroku pg:backups:schedule DATABASE_URL --at '02:00 America/Chicago'</b>

<pre>
Scheduling automatic daily backups of postgresql-silhouetted-69904 at 02:00 America/Chicago... done
</pre>

<h2>Check the backup schedule</h2>

$ <b>heroku pg:backups:schedules</b>

<pre>
=== Backup Schedules
DATABASE_URL: daily at 2:00 America/Chicago
</pre>

<h2>Check backups</h2>

$ <b>heroku pg:backups</b>

<pre>
=== Backups
ID    Created at                 Status                               Size     Database
────  ─────────────────────────  ───────────────────────────────────  ───────  ────────
b005  2017-07-16 04:33:50 +0000  Completed 2017-07-16 04:33:52 +0000  12.77kB  DATABASE
b004  2017-07-10 14:00:30 +0000  Completed 2017-07-10 14:00:33 +0000  12.31kB  DATABASE

=== Restores
No restores found. Use heroku pg:backups:restore to restore a backup

=== Copies
No copies found. Use heroku pg:copy to copy a database to another
</pre>
