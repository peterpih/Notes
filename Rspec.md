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





[RSpec Testing for Beginners, Part 1](https://code.tutsplus.com/articles/rspec-testing-for-beginners-part-1--cms-26716)

[Great link for setting up Rspec](https://blog.codeship.com/install-rspec-tutorial/)
