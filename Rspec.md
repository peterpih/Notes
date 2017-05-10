<h1>Installing Rspec</h1>

In the development group in Gemfile add this:
<pre>
group :development, :test do
  gem 'rspec-rails'
end
</pre>

Then

$ <b>bundle</b>   
$ <b>rails generate rspec:</b>install
<pre>
create  .rspec
create  spec
create  spec/spec_helper.rb
create  <b>spec/rails_helper.rb</b>
</pre>

You will need to add to every _spec.rb test file
<pre>
require 'rails_helper'
</pre>

Run your tests:   
$ <b>bundle exec rspec spec/</b><em>models/dummy_model_spec.rb</em>


$ <b>cd spec</b>   
$ <b>mkdir models</b>   
$ <b>mkdir features</b>   
$ <b>touch feature_helper.rb</b>  

<pre>
# spec/feature_helper.rb

require 'rails_helper'
require 'database_cleaner'
require 'capybara/poltergeist'
</pre>


[RSpec Testing for Beginners, Part 1](https://code.tutsplus.com/articles/rspec-testing-for-beginners-part-1--cms-26716)

[Great link for setting up Rspec](https://blog.codeship.com/install-rspec-tutorial/)
