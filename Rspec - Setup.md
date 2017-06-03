<h2>In Gemfile</h2>  
<em>need to add gems to Gemfile</em>

<pre>
group :development, :test do
  &#35; Call 'byebug' anywhere in the code to stop execution and get a debugger console
  gem 'byebug', platform: :mri
  <b>gem 'rspec-rails'</b>
end

group :development, :test do
  <b>gem 'rspec-rails'</b>   
  <b>gem 'factory_girl_rails'</b>
end

group :test do
  <b>gem 'faker'</b>   
  <b>gem 'capybara'</b>   
  <b>gem 'guard-rspec'</b>   
  <b>gem 'launchy'</b>   
end
</pre>

$ <b>bundle install</b>

<h2>Initialize the spec/ directory (where specs will reside) with:</h2>

$ <b>cd</b> <em>&lt;your app's root directory&gt;</em>  
$ <b>mkdir spec</b>  
$ <b> cd spec</b>   
$ <b>rails generate rspec:install</b>   
<pre>
Running via Spring preloader in process 99679
      create  .rspec
       exist  spec
      create  spec/spec_helper.rb
      create  spec/rails_helper.rb
</pre>

<h2>Change some configurations</h2>
1) <em>add the following line to the top of <b>spec/spec_helper.rb</b></em>
<pre>
require "capybara/rspec"
</pre>

2) <em>add the following line to <b>app-root/.rspec</b></em>
<pre>
--format documentation
</pre>

3) <em>add the following line to <b>config/application.rb</b></em> in <b>class Application</b> section   
<em> this will automatically generate shells for testing</em>
<pre>
config.generators do |g|
  g.test_framework :rspec,
    :fixtures => true,
    :view_specs => false,
    :helper_specs => false,
    :routing_specs => false,
    :controller_specs => true,
    :request_specs => true
  g.fixture_replacement :factory_girl, :dir => "spec/factories"
end
</pre>
<h2>To runs the specs</h2>

$ <b>bundle exec rspec</b>
