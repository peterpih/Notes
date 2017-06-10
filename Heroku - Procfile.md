<h2>Create Procfile</h2>   
In the application root directory   
<pre>
<em># Procfile</em>   

web: bundle exec puma -t 5:5 -p ${PORT:-3000} -e ${RACK_ENV:-development}
web: bundle exec puma -C config/puma.rb
</pre>
then add to git commit and push to Heroku
