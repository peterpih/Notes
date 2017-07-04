<h2>Setup environment variables</h2>  

"01" necessary since loading is in alphabetic order

<pre>
<em># config/initializers/01_environment.rb</em>

unless Rails.env.production?
  ENV['EMAIL_USERNAME'] = '<em>username</em>'
  ENV['EMAIL_PASSWORD'] = '<em>password</em>'
  puts "check Username set: "+ ENV['EMAIL_USERNAME']
end
</pre>

<h2>Add to <b>.gitignore</b> to keep ENV variables private</h2>
<pre>
<em># .gitignore</em>

config/initializers/01_environment.rb
</pre>
