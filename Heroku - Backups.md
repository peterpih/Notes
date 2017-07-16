[<h1>Heroku PGBackups</h1>](https://devcenter.heroku.com/articles/heroku-postgres-backups)

<h2>Do a backup (now)</h2>

$ <b>heroku pg:backups:capture</b>
<pre>
Starting backup of postgresql-silhouetted-69904... done

Use Ctrl-C at any time to stop monitoring progress; the backup will continue running.
Use heroku pg:backups:info to check progress.
Stop a running backup with heroku pg:backups:cancel.

Backing up DATABASE to b006... done
</pre>

<h2>Schedule a backup</h2>

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
