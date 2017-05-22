[Update Your Gems Early and Often](https://robots.thoughtbot.com/keep-your-gems-up-to-date)
- Update gems one at a time  
- Each update has it's own commit
- links to Release Notes should be included with the commits

<h2>Gemfile.lock</h2>

<b>Great explaination of Gemfile.lock:</b>  
http://stackoverflow.com/questions/6927442/what-is-the-difference-between-gemfile-and-gemfile-lock-in-ruby-on-rails

<b>Gemfile.lock</b> records the **exact** version used  
Gemfile records preferences ie "~>"  

<h2>Always version control Gemfile.lock</h2> Heroku needs it

<h2>bundler-audit</h2> 
<pre>
<em>for checking vulnerabilities  </em>
$ <b>gem install bundler-audit</b>
<br>
<em>then in the same directory as Gemfile.lock</em>
$ <b>bundle-audit</b>
</pre>

<h2>Bundler Commands</h2>
<pre>
<b>bundle -v</b>                    # show bundler version number
<b>bundle install</b>                # install a gem in this scope
<b>bundle install</b> <em>gem</em>
<br>
<b>bundle update</b>                 # update gems and Gemfile.lock
<b>bundle update</b> <em>gem</em>
<b>bundle update --source</b> <em>gem</em>
<br>
<b>bundle outdated</b>              # show which gems are outdated
<b>bundle outdated --strict</b>
</pre>
