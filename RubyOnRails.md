[**Beginning Rails 4** book](https://books.google.co.uk/books?id=KdvTAAAAQBAJ&pg=PA52&lpg=PA52&dq=%22%3D%3E%22+operator+in+rails+4&source=bl&ots=UdU7f90zix&sig=aFHc2JnL8LGYbFTnSJITeAZJFkg&hl=en&sa=X&ved=0CEMQ6AEwBWoVChMI3Yrpka-iyAIVSJ0aCh0H0gAk#v=onepage&q=%22%3D%3E%22%20operator%20in%20rails%204&f=false)  

#Installing Ruby On Rails on Windows 8.1

###Install Ruby

http://rubyinstaller.org/downloads/  

or  

http://rubyonrails.org/download/  


Be sure to check the comments and install the most recent **stable** version
**NB: currently not using 64-bit**
This video was also generally helpful: https://www.youtube.com/watch?v=j8UsSmSgVt8

**Check Ruby has been installed correctly**
<pre>
<b>Ruby -v</b>
<b>Ruby --version</b>
</pre>

> At this point I tried to run **rails server** but got an error message to install DevKit


###Install DevKit
for downloads: http://rubyinstaller.org/downloads/

**read instructions thoroughly**
instructions: https://github.com/oneclick/rubyinstaller/wiki/Development-Kit
<pre>
<b>mkdir</b> C:\RubyDevKit   # <em>install to a permanent directory</em>
<b>cd</b> C:\RubyDevKit
<b>ruby dk.rb install</b>
</pre>

**Install JSON**

<pre>
<b>gem install json --platform=ruby</b>
</pre>
**Check JSON installed correctly**
<pre>
ruby -rubygems -e "require 'json';puts JSON.load('[42]').inspect"
</pre>

####Install GEMs
<pre>
<b>bundle install</b>
</pre>

####Migrate Database
<pre>
<b>rake db:migrate</b>
</pre>

####Create New Application
<pre>
<b>cd</b> C:\rails
<b>rails new</b> blog
<b>cd</b> blog
</pre>

####Start Server
<pre>
<b>rails server</b>
</pre>

Create controller
Create route

><b>rails generate model</b> <em>model-name</em>  

creates:
- db/migrate/
- app/views/<em>model name</em>


####Rail Types
[Here's a good set of definitions for types](from http://stackoverflow.com/a/15316528/2128691)
<pre>
- <b>binary</b> - is for storing data such as images, audio, or movies.
- <b>boolean</b> - is for storing true or false values.
- <b>date</b> - store only the date
- <b>datetime</b> - store the date and time into a column.
- <b>decimal</b> - is for decimals.
- <b>float</b> - is for decimals. (What's the difference between decimal and float?)
- <b>integer</b> - is for whole numbers.
- <b>primary_key</b> - unique key that can uniquely identify each row in a table
- <b>string</b> - is for small data types such as a title. (Should you choose string or text?)
- <b>text</b> - is for longer pieces of textual data, such as a paragraph of information.
- <b>time</b> - is for time only
- <b>timestamp</b> - for storing date and time into a column.
</pre>

####Rails Commands

[Generate Model vs Scaffolding](http://stackoverflow.com/questions/17734378/difference-between-scaffold-and-model-in-rails)
<pre>
<b>rails generate model</b> <em>model-name</em>
<b>rails generate scaffold</b> <em>name</b> &ltfield:property&gt &ltfield:property&gt</em>
</pre>

###Model names are singular, controller names are plural

Controller and Class naming

Controller name file and class name:  
<pre>
controller/my_controller_name.rb  -&gt class MyControllerName
</pre>

In router.rb:  
<pre>
<b>home#new</b>
</pre>
- home is the controller
- new is the view.html.erb
