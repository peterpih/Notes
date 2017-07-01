<h2>Adding Devise gem to your Gemfile</h2>
<pre>
gem 'devise'
gem 'devise-bootstrap-views'
</pre>

then  

$ <b>bundle install --without production</b>

<hr>

<h2>Install Devise</h2>  

$ <b>rails generate devise:install</b>

<pre>
Running via Spring preloader in process 29640
      create  config/initializers/devise.rb
      create  config/locales/devise.en.yml
</pre>

Some setup you must do manually if you haven't yet:

<pre>
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
     
       &lt;p class="notice"&gt;&lt;%= notice %&gt;&lt;/p&gt;
       &lt;p class="alert"&gt;&lt;%= alert %&gt;&lt;/p&gt;

4. You can copy Devise views (for customization) to your app by running:

       rails g devise:views
</pre>

<hr>

<h2>Create User model</h2>

$ <b>rails generate devise User</b>   <em>( note: capital 'U')</em>
<em>automatically create migration and model</em>
<pre>
Running via Spring preloader in process 29767
      invoke  active_record
      create    db/migrate/20170615143127_devise_create_users.rb
      create    app/models/user.rb
      invoke    test_unit
      create      test/models/user_test.rb
      create      test/fixtures/users.yml
      insert    app/models/user.rb
       route  devise_for :users
</pre>

<hr>

<h2>Migration</h2>

<b>NOTE:</b>   
Before running <em>migration</em> make any edits necessary if you are using <b>:confirmable</b>   
see commented out portion in <b><em>migration</em></b> file and at top in <b><em>models/user.rb</em></b>

$ <b>rake db:migrate</b>
<pre>
(in /Users/peterpih/udemy/finance-tracker)
== 20170615143127 DeviseCreateUsers: migrating ================================
-- create_table(:users)
   -> 0.0060s
-- add_index(:users, :email, {:unique=>true})
   -> 0.0024s
-- add_index(:users, :reset_password_token, {:unique=>true})
   -> 0.0019s
== 20170615143127 DeviseCreateUsers: migrated (0.0105s) =======================
</pre>

<h2>Modify application_controller.rb</h2>
<pre>
<em>controller/application_controller.rb</em>
protect_from_forgery with: :exception   
<b>before_action :authenticate_user!</b>

</pre>
<h2>Logout link</h2>
It will be necessary to add a logout link, login is handled by the <b>action_before</b> in application_controller.rb
<pre>
$lt;%= link_to 'Logout', destroy_user_session_path, method: :delete %&gt;
</pre>

<h2>Add Bootstrap to Gemfile</h2>
<pre>
gem 'devise'
gem 'twitter-bootstrap-rails'
</pre>

$ <b>bundle install --without production</b>   
$ <b>rails generate bootstrap_install static</b>

<hr>

<h2>Add devise_bootstrap to application.css</h2>
<pre>
*= require devise_bootstrap_views   
*= require tree .\
*= require self
</pre>
</pre>

<h2>All set to go!</h2>

