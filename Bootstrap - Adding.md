<h2>Add Bootstrap gem to Gemfile</h2>
<pre>
<b>gem</b> 'twitter-bootstrap-rails'
<b>gem</b> 'devise-bootstrap-views'
</pre>

then  

$ <b>bundle install --without production</b>

<hr>

<h2>Add Bootsrap to app</h2>
$ <b>rails generate bootstrap:install static</b>
<pre>
Running via Spring preloader in process 17720
      <b>insert</b>  app/assets/javascripts/application.js
      <b>create</b>  app/assets/javascripts/bootstrap.js.coffee
      <b>create</b>  app/assets/stylesheets/bootstrap_and_overrides.css
      <b>create</b>  config/locales/en.bootstrap.yml
        <b>gsub</b>  app/assets/stylesheets/application.css
</pre>

$ <b>rails generate bootstrap:layout application</b>
<pre>
    <b>conflict</b>  app/views/layouts/application.html.erb   
<b>Overwrite</b> /Users/peterpih/udemy/photo-app/app/views/layouts/application.html.erb? (enter "h" for help) [Ynaqdh] <b>Y</b>   
       <b>force</b>  app/views/layouts/application.html.erb   
</pre>

$ <b>rails generate devise:views:locale en</b>

$ <b>rails generate devise:views:bootstrap_templates</b>
<pre>
      <b>create</b>  app/views/devise
      <b>create</b>  app/views/devise/confirmations/new.html.erb
      <b>create</b>  app/views/devise/mailer/confirmation_instructions.html.erb
      <b>create</b>  app/views/devise/mailer/reset_password_instructions.html.erb
      <b>create</b>  app/views/devise/mailer/unlock_instructions.html.erb
      <b>create</b>  app/views/devise/passwords/edit.html.erb
      <b>create</b>  app/views/devise/passwords/new.html.erb
      <b>create</b>  app/views/devise/registrations/edit.html.erb
      <b>create</b>  app/views/devise/registrations/new.html.erb
      <b>create</b>  app/views/devise/sessions/new.html.erb
      <b>create</b>  app/views/devise/shared/_links.html.erb
      <b>create</b>  app/views/devise/unlocks/new.html.erb
</pre>
