Add
<pre>
gem 'seed_dump'
</pre>
to Gemfile, then `bundle install`

To download a local database   
$ <b>rake db:dump:seed</b>   
will create db/seeds.rb file

then  
<pre>
copy db/seeds.rb file from one app to the other  

$ <b>rake db:seed</b>
</pre>
To populate, the receiving database has to be already created.
