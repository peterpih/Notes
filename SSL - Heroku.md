[Let's Encrypt](https://letsencrypt.org)

[HOWTO setup SSL with Rails & Heroku](http://readysteadycode.com/howto-setup-ssl-with-rails-and-heroku)

In Rails:need to add
<pre>
config.force_all = true
</pre>
to config/environments/production.rb

and possibly change
<pre>
&lt;script src="http://code.jquery.com/jquery-2.1.0.js"&gt;&lt;/script&lt
to
&lt;script src="//code.jquery.com/jquery-2.1.0.js"&gt;&lt;/script&gt;
</pre>

to secure assets and not get "mixed" content warnings.

The external resource will then be requested with whichever 
protocol the page was requested with, i.e. either https or http. 
So it’ll work just fine with or without SSL.