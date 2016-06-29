**Links**  
http://www.justinweiss.com/blog/2014/07/28/4-simple-memoization-patterns-in-ruby-and-one-gem/  


<pre>
<b>rails console</b>
</pre>

Should give <b>irb</b> prompt

####[<b>Find Tables In Database</b>](http://stackoverflow.com/questions/24880956/rails-console-database-schema-checking)  
<pre>
# <em>list the tables in the database</em>
ActiveRecord::Base.connection.tables
</pre>

can also check the tables in <b>db/schema.rb</b>

To recreate <b>db/schema.rb</b>:
<pre>
<b>bundle exec rake db:schema:dump</b>
</pre>

***table_print**
- add **table_print** to Gemfile
- bundle install

In <b>rails console</b> type "tp" to see if it's installed, or
<pre>
show data_directory;
</pre>

###Capybara
cheatsheet: https://gist.github.com/zhengjia/428105  
http://stackoverflow.com/questions/22872955/make-capybara-click-a-dropdown-option  
https://github.com/jnicklas/capybara/blob/3ae284460b1af35d40b077bf14f7222c2982c120/lib/capybara/spec/session/has_select_spec.rb#L15  

Look at the underlying html code on the webpage to find the variable names to test  


####Postgres
[**start server**](http://www.postgresql.org/docs/9.1/static/server-start.html)    
Possibly have to edit <b>posgresql.conf</b> for localhost and port  

<pre>
<b>postgres -D</b> <em>directory-for-postgres.conf</em>
</pre>
To find postgres.conf file directory:
<pre>
<b>rails dbconsole</b>
<b>show config_file;</b>
</pre>

####[<b>dump restore</b>](http://www.postgresql.org/docs/9.4/static/backup-dump.html)   
<pre>
<b>pg_dump</b> <em>database-name<em> <b>&gt</em> <em>text-dump-file</em>

<b>psql</b> <em>database-name</em> <em>&lt</em> <em>text-dump-file</em>
<pre>

psql will not create a data base, to <b>create</b> a database:
<pre>
<b>createdb -T template0</b> <em>database-name</em>
</pre>

####To <b>DELETE</b> a database:
<pre>
<b>rails dbconsole</b>
<b>/\c</b> <em>a-different-database</em>    # <em>connect to a different database than the one being deleted</em>
<b>DROP DATABASE</b> <em>database-name</em>
</pre>

###Sublime 2
http://www.chrishjorth.com/blog/turn-sublime-text-into-the-best-web-development-editor-on-mac/  
