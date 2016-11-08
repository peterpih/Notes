###[Ruby Upgrade](https://github.com/rbenv/rbenv/issues/285)

https://gorails.com/setup/osx/10.11-el-capitan
<pre>
$ <b>brew upgrade</b>            # upgrade Homebrew first

<b>brew upgrade ruby-build</b>   # <em>upgrade ruby-build</em>
                          # <em>may have to run <b>brew upgrade</b> first</em>
        - or -
        
<b>brew install rbenv ruby-build</b>

                          
<b>ruby --version</b>            # <em>show the ruby version</em>  

<b>rbenv versions</b>            # <em>shows available versions of ruby</em>  

<b>rbenv install -l</b>          # <em>show a long list of available version numbers</em>

<b>rbenv install</b> <em>2.2.4</em>       # <em>install a specific version</em>  
                          # <em>if not available try upgrading <b>ruby-build</b></em>  



<b>rbenv install</b> <em>2.2.4</em>       # <em>install specific version of Ruby 2.2.4</em>

<b>rbenv global</b> <em>2.2.4</em>        # <em>sets default version number in ~/.rbenv/version</em>

<b>gem install bundler</b>       # <em>to get <b>bundler</b> for new ruby version</em>

<b>bundle install</b>             # <em>install missing gems</em>
<b>cd</b> <em>back-to-dev-directory</em>

<b>bundler</b>                   # <em>run bundler, entire list of gems will appear</em>

</pre>

To set a particular Ruby version for a project use  
<pre>
# <b>./.ruby-version</b>

2.2.4
</pre>

###NOTE:
<pre>
Had a problem that <b>rbenv</b> could not see <b>bundle</b>  
Ran <b>bundle</b> from ~/.rbenv/versions/2.2.4/bin and it was fixed
</pre>

###[Rspec install](https://www.launchacademy.com/codecabulary/learn-test-driven-development/rspec/setting-up-rpec)
<pre>
<b>cd</b> <em>project-directory</em>  
<b>rails generate rspec:install</b>
</pre>
<pre>
Can be used for <b>new</b> project or <b>existing</b> project which needs rspec
</pre>
Add to Gemfile:
<pre>
<b>group :development, :test do</b>
  <b>gem</b> 'rspec-rails', '~> 3.0'
<b>end</b>
</pre>

###Lastly
For Rails > 4.0
<pre>
<b>gem</b> 'rails_12factor', '~> 0.0.3', <b>group: :production</b>
</pre>
Add to Gemfile for Heroku

###Change database.yml to use postgres
