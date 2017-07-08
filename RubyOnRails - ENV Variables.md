<h2>Setup environment variables</h2>  

"<b>01_</b>" necessary as filename prefix since loading is in alphabetic order

<pre>
<em># config/initializers/<b>01_</b>environment.rb</em>

unless Rails.env.production?
  ENV['EMAIL_USERNAME'] = '<em>username</em>'
  ENV['EMAIL_PASSWORD'] = '<em>password</em>'
  puts "check Username set: "+ ENV['EMAIL_USERNAME'] <em># to check ENV[] was loaded correctly</em>
end
</pre>

<h2>Add to .gitignore to keep ENV variables private</h2>
<pre>
<em># .gitignore</em>

config/initializers/01_environment.rb
</pre>
