<pre>
<a href="https://afternoon-oasis-87153.herokuapp.com">afternoon-oasis-87153 -         </a>
<a href="https://ancient-wave-4180.herokuapp.com">ancient-wave-4180 -             recaptcha testbed</a>
<a href="https://aqueous-fortress-58776.herokuapp.com" target="_blank">aqueous-fortress-58776 -        </a>
<a href="https://aqueous-spire-6633.herokuapp.com" target="_blank">aqueous-spire-6633 -            Vocab Builder</a>

<a href="https://www.andorferadvisors.herokuapp.com" target="_blank">andorferadvisors-               andorferadvisors.com</a>
<a href="https://www.andorferadvisors-fwd-blog.herokuapp.com" target="_blank">andorferadvisors-fwd-blog -     andorferadvisors.com</a>
<a href="https://andorferadvisors-fwd-mvp.herokuapp.com" target="_blank">andorferadvisors-fwd-mvp -      mvp.andorferadvisors.com</a>

<a href="https://enigmatic-brook-80258.herokuapp.com" target="_blank">enigmatic-brook-80258 -         FFF redirect to Certified Mediums page [ PHP ]</a>
<a href="https://phoenix-testbed.herokuapp.com" target="_blank">phoenix-testbed -               Phoenix testbed [ Phoenix ]</a>
<a href="https://mighty-lake-1899.herokuapp.com" target="_blank">mighty-lake-1899 -              FFF testbed</a>
<a href="https://safe-escarpment-3878.herokuapp.com" target="_blank">safe-escarpment-3878 -      </a>

<a href="https://www.soonerbaptist.herokuapp.com" target="_blank">soonerbaptist -                 Sooner Baptist</a>
<a href="https://www.soonerbaptist-fwd-calendar.herokuapp.com" target="_blank">soonerbaptist-fwd-calendar -    Sooner Baptist calendar</a>
<a href="https://www.soonerbaptist-fwd-sermons.herokuapp.com" target="_blank">soonerbaptist-fwd-sermons -     Sooner Baptist sermons</a>
</pre>

Useful links:  
<b>setup</b>: http://sourabhbajaj.com/mac-setup/Heroku/README.html  
[pg:push and pg:pull]posgres</b>: https://devcenter.heroku.com/articles/heroku-postgresql#pg-push-and-pg-pull  
**git deploy**: https://dashboard.heroku.com/apps/aqueous-spire-6633/deploy/heroku-git   
**pulling down database**: 


###Install Heroku
On OSX, use Homebrew:  
<pre>
<b>brew install heroku-toolbelt</b>
<b>heroku update</b>
</pre>

###Heroku Commands  
<b>heroku local</b>             <em>( run the app locally from heroku )</em>

add <b>--app <em>APP</em></b> to specify non default Heroku <em>APP</em>  
<pre>
<b>heroku open</b>              <em>( open a link to the app website in local browser )</em>
<b>heroku ps</b>                <em>( dynos running on Heroku )</em>

<em>( show configuration vars and the database url )</em>
<b>heroku config</b>            


<b>heroku addons</b>            <em>( show additional services )</em>

<b>heroku pg:psql</b>           <em>( for <a href="#accessing-database-remotely">postgres on Heroku</a> )</em>

<em>( dump one or more tables from a database )</em>
<b>heroku pg:dump -t</b> <em>table-name [-t database-name] database-name</em>

<em>( take site down / up for maintenance )</em>
<b>heroku maintenance:on</b>    
<b>heroku maintenance:off</b>

<em>( show log file for Heroku APP )</em>
<b>heroku logs --app</b> <em>APP</em> 

<em>( show nlines in log file for Heroku APP )</em>
<b>heroku logs --app</b> <em>APP</em> <b>-n</b> <em>nlines</em>  

<em>( tail the logs )</em>
<b>heroku logs --app</b> <em>APP</em> <b>--tail</b> 


<b>heroku restart --app</b> <em>APP</em>             <em>( restart APP )</em>

<b>heroku run bash --app</b> <em>APP</em>            <em>( remote Unix command line )</em>
</pre>
  
###Example Heroku website
<pre>
<em>( clone a local repo from heroku )</em>
<b>heroku git:clone -a</b> <em>heroku_app</em> <em>dest_dir</em>

<em>( get the example app )</em>
<b>git clone https://github.com/heroku/ruby-getting-started.git</b> 

<b>heroku create</b>                       <em>( link to Heroku )</em>

<b>git push heroku master</b> <em>branch</em><b>:master</b> <em>( deploy app to Heroku git )</em>
<b>heroku open</b>                         <em>( open the website in a local browser )</em>
</pre>

###Papertrail
<pre>
<b>heroku addons</b>                       <em>( show addons )</em>
<b>heroku addons:doc papertrail</b>        <em>( documentation for papertrail )</em>
<b>heroku addons:open papertrail</b>       <em>( open a dashboard for papertrail )</em>

<b>heroku run bash</b>                     <em>( runs a remote shell )</em>
<b>heroku run</b> <em>command</em>                  <em>( runs a commandline command )</em>
<b>heroku run bundle install</b>
<b>heroku run rake db:migrate</b>

<b>heroku config</b>                       <em>( show config settings )</em>
                                    <em>( database url is shown here )</em>
<b>heroku config:set TIMES=10</b>          <em>( set TIMES env var to 10 )</em>
</pre>

###Postgres on Heroku  
NOTE: <b>DATABASE_URL</b> and <b>DATABASE</b> are the <b>literal strings</b> not env variables  
<pre>
<b>heroku pg:info</b>                      <em>( show some info about the database )</em>

<b>heroku pg:reset DATABASE_URL</b>        <em>( empties the database <b>DO NOT DELETE THE DATABASE</b></em>
                                    <em>( empty it using this )</em>

<b>heroku pg:credentials DATABASE</b>      <em>( shows the database credentials: username, password)</em>

<b>git push heroku test:master</b>         <em>( push 'test' branch to 'master' on heroku )</em>

<b>heroku pg:push</b> <em>mylocaldb</em> <b>DATABASE_URL</b>
<em>heroku pg:push mylocaldb HEROKU_POSTGRESQL_MAGENTA --app sushi</em>
</pre>

###To pull down a database:
<pre>
<b>heroku pg:pull</b>
<b>heroku pg:pull</b> <em>AMBER fff_development</em> <b>--app</b> <em>forever-family-foundation</em>
</pre>

<id='accessing-database-remotely'>
###Accessing database remotely
Need to be made a Collaborator on the database, then:  
<pre>
<b>heroku pg:psql --app</b> <em>APP</em>  
<b>heroku pg:psql --app</b> <em>aqueous-spire-6633</em>
</pre>
**Records created since 1 month ago**  
<pre>
<b>SELECT * FROM</b> <em>table-name</em> <b>WHERE</b> <em>column-name</em> > <b>CURRENT_DATE - INTERVAL '1 month';</b>
</pre>

<id='production-check'>
###Production Check  
On the **Heroku  Dashboard**, click on hamburger in upper right-hand corner, then click **Production Check**

<id='heroku-with-godaddy'>
###Heroku with GoDaddy   
http://lifesforlearning.com/heroku-with-godaddy/

<pre>
<b>On godaddy.com</b>

Create CNAME record host="agile", target="andorferadvisors-fwd-agile.herokuapp.com"

<b>On Github</b>

Create new repository "andorferadvisors-fwd-agile"
Clone repository locally

<b>On Heroku</b>

Create a new app with name "andorferadvisors-fwd-agile"  
Add Domain (under Settings) "agile.andorferadvisors.com"

<b>Locally</b>
Write forwarding code

git remote add heroku https://git.heroku.com/andorferadvisors-fwd-agile.git
Git push heroku master


</pre>



<pre>
Add CNAME record
    host="www", target="<em>myapp</em>.herokuapp.com

Delete the '@' in the A record   

setup domain forwarding  
    To = https://www.<em>myapp</em>.herokuapp.com
    Forward Type = Permanent(301)  
    Settings = Forward only
    tick "Update my nameservers"
</pre>
