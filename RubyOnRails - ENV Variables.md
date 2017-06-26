<pre>
<em># config/initializers/dev_environment.rb</em>

unless Rails.env.production?
  ENV['EMAIL_USERNAME'] = '<em>username</em>'
  ENV['EMAIL_PASSWORD'] = '<em>password</em>'
  puts "check Username set: "+ ENV['EMAIL_USERNAME']
end
</pre>

And don't forget to add to <b>.gitignore</b>
<pre>
<em># .gitignore</em>

config/initializers/dev_environment.rb
</pre>
