<h2>Add to Gemfile</h2>

<pre>
gem 'devise' 
</pre>

$ <b>bundle install --without production</b>

$ <b>rails generate devise:install</b>

$ <b> rails generate devise User</b> <em>(note capital 'U'ser)</em>

<h2>Add to application_controller.rb</h2>

<pre>
before_action :authenticate_user!
</pre>

$ <b>rails generate bootstrap:layout application</b>

<h2>Add in Gemfile</h2>

<pre>
gem 'devise'
gem 'twitter-bootstrap-rails'
<b>gem 'devise-bootstrap-views'</b>
</pre>

$ <b>bundle install --without producation</b>

<h2>Add to application.scss</h2>

<pre>
*
<b>*= require devise_bootstrap_views</b>
*= require tree .
*= require self
</pre>

$ <b>rails generate devise:views:locale en</b>

$ <b>rails generte devise:views:bootstrap_templates</b>  <em>( to update to bootstrap format )</em>

<h2>Add to routes.rb</h2>

<pre>
devise_for :users
</pre>
