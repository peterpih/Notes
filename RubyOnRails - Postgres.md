<b>After setting up the local repository, the database needs to be set up</b>

<em>&#35; config/database.yml</em>
<pre>
&#35; SQLite version 3.x
&#35;   gem install sqlite3
&#35;
&#35;   Ensure the SQLite 3 gem is defined in your Gemfile
&#35;   gem 'sqlite3'
&#35;
default: &default
  adapter: <b>postgresql</b>
  pool: 5
  timeout: 5000

development:
  <<: *default
  database: <b>my_development</b>

&#35; Warning: The database defined as "test" will be erased and
&#35; re-generated from your development database when you run "rake".
&#35; Do not set this db to the same as development or production.
test:
  <<: *default
  database: <b>my_test</b>

production:
  <<: *default
  database: <b>my_production</b>
</pre>

The database can be checked using:  

$ <b>psql</b>
<pre>
<b>\c</b> <em>my_development</em>           <em>connect to development database</em>
<b>\d</b>                          <em>list table names</em>
<b>\d</b> <em>table-name</em>               <em>list columns in a table</em>
</pre>
