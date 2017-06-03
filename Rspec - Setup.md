<h2>In Gemfile</h2>  
<em>need to add gem</em>

<pre>
group :development, :test do
  &#35; Call 'byebug' anywhere in the code to stop execution and get a debugger console
  gem 'byebug', platform: :mri
  <b>gem 'rspec-rails'</b>
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

<h2>To runs the specs</h2>

$ <b>bundle exec rspec</b>
