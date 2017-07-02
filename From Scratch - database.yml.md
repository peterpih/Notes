<h2>Get rid of SQLite3 and use <b>postgresql</b></h2>  

The database names also need to change for postgresql  

<pre>
# SQLite version 3.x
#   gem install sqlite3
#
#   Ensure the SQLite 3 gem is defined in your Gemfile
#   gem 'sqlite3'
#
default: &default
  adapter: <b>postgresql</b>
  pool: 5
  timeout: 5000

development:
  &lt;&lt;: &#42;default
  database: <b>example</b>_development

# Warning: The database defined as "test" will be erased and
# re-generated from your development database when you run "rake".
# Do not set this db to the same as development or production.
test:
  &lt;&lt: &#42;default
  database: <b>example</b>_test

production:
  &lt;&lt: &#42;default
  database: <b>example</b>_production
</pre>
