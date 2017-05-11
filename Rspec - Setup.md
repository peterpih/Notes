<h2>In Gemfile</h2>
<em>&#35; Gemfile</em> need to add gem

<pre>
group :development, :test do
  &#35; Call 'byebug' anywhere in the code to stop execution and get a debugger console
  gem 'byebug', platform: :mri
  <b>gem 'rspec-rails'</b>
end
</pre>
