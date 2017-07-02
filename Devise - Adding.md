<h2>Add to Gemfile</h2>

<pre>
gem 'devise' 
</pre>

$ <b>bundle install --without production</b>

$ <b>rails generate devise:install</b>

<pre>
      create  config/initializers/devise.rb
      create  config/locales/devise.en.yml
===============================================================================

Some setup you must do manually if you haven't yet:

  1. Ensure you have defined default url options in your environments files. Here
     is an example of default_url_options appropriate for a development environment
     in config/environments/development.rb:

       config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }

     In production, :host should be set to the actual host of your application.

  2. Ensure you have defined root_url to *something* in your config/routes.rb.
     For example:

       root to: "home#index"

  3. Ensure you have flash messages in app/views/layouts/application.html.erb.
     For example:

       <p class="notice"><%= notice %></p>
       <p class="alert"><%= alert %></p>

  4. You can copy Devise views (for customization) to your app by running:

       rails g devise:views

===============================================================================
</pre>

$ <b> rails generate devise User</b> <em>(note capital 'U'ser)</em>   
<em>Creates all the routes for user_: user_session_, user_registration_.</em>

<pre>
      invoke  active_record
      create    db/migrate/20170701235319_devise_create_users.rb
      create    app/models/user.rb
      invoke    test_unit
      create      test/models/user_test.rb
      create      test/fixtures/users.yml
      insert    app/models/user.rb
       route  devise_for :users
</pre>

<h2>Make any wanted customizaions to the model</h2>

$ <b>rake db:migrate</b>

<pre>
== 20170701235319 DeviseCreateUsers: migrating ================================
-- create_table(:users)
   -> 0.0182s
-- add_index(:users, :email, {:unique=>true})
   -> 0.0032s
-- add_index(:users, :reset_password_token, {:unique=>true})
   -> 0.0018s
== 20170701235319 DeviseCreateUsers: migrated (0.0235s) =======================
</pre>


<h2>Add to application_controller.rb to control access to logged-in users only</h2>

<pre>
before_action :authenticate_user!
</pre>

$ <b>rails generate bootstrap:layout application</b>

<pre>
    conflict  app/views/layouts/application.html.erb
Overwrite /Users/peterpih/ror/impact_report/app/views/layouts/application.html.erb? (enter "h" for help) [Ynaqdh] <b>Y</b>
       force  app/views/layouts/application.html.erb
</pre>

You will need to put your original navbar back into <b>application.html.erb</b> and the header.

<h2>Add in Gemfile</h2>

<pre>
gem 'devise'
gem 'twitter-bootstrap-rails'
<b>gem 'devise-bootstrap-views'</b>
</pre>

$ <b>bundle install --without production</b>

<h2>Add to application.scss</h2>

<pre>
*
<b>*= require devise_bootstrap_views</b>
*= require tree .
*= require self
</pre>

$ <b>rails generate devise:views:locale en</b>

$ <b>rails generate devise:views:bootstrap_templates</b>  <em>( to update views to bootstrap format )</em>

<pre>
      create  app/views/devise
      create  app/views/devise/confirmations/new.html.erb
      create  app/views/devise/mailer/confirmation_instructions.html.erb
      create  app/views/devise/mailer/reset_password_instructions.html.erb
      create  app/views/devise/mailer/unlock_instructions.html.erb
      create  app/views/devise/passwords/edit.html.erb
      create  app/views/devise/passwords/new.html.erb
      create  app/views/devise/registrations/edit.html.erb
      create  app/views/devise/registrations/new.html.erb
      create  app/views/devise/sessions/new.html.erb
      create  app/views/devise/shared/_links.html.erb
      create  app/views/devise/unlocks/new.html.erb
</pre>

<h2>Add to routes.rb</h2>

<pre>
devise_for :users
</pre>
