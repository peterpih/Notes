[How to install Bootstrap 4 in Rails](http://mixandgo.com/blog/how-to-install-bootstrap-4-in-rails)

[Bootstrap-sass Gem git repo](https://github.com/twbs/bootstrap-sass)

Copy the following line into your Gemfile (and check for version update in git repo README)
<pre>
<em># Gemfile</em>

gem 'bootstrap-sass', '~> 3.3.6'  
gem 'sass-rails', '>= 3.2'
</pre>

then  
$ <b>bundle install --without production</b>

create <em>app/assets/stylesheets/custom.css.scss</em> (must have .scss extension)   
assumes all of the <b>css</b> styling will go into <b>custom.cs.scss</b>   
add the following <b>@import</b>s  
<pre>
<em># app/assets/stylesheets/custom.css.scss</em>

<em>changes to bootstrap's constants go <b>before</b> the imports</em>
<b>@import "bootstrap-sprockets";</b>
<b>@import "bootstrap";</b>
</pre>



[Integrating Rails and Bootstrap, Part 1 - the Installation](https://launchschool.com/blog/integrating-rails-and-bootstrap-part-1)

[Bootstrap Grid Examples](http://getbootstrap.com/examples/grid/)

<h2>Adding Bootstrap</h2>


<pre>
<em># application.js</em>

// This is a manifest file that'll be compiled into application.js, which will include all the files
// listed below.
//
// Any JavaScript/Coffee file within this directory, lib/assets/javascripts, vendor/assets/javascripts,
// or any plugin's vendor/assets/javascripts directory can be referenced here using a relative path.
//
// It's not advisable to add code directly here, but if you do, it'll appear at the bottom of the
// compiled file.
//
// Read Sprockets README (https://github.com/rails/sprockets#sprockets-directives) for details
// about supported directives.
//
//= require jquery
//= require jquery_ujs
//= require turbolinks
<b>//= require bootstrap-sprockets</b>
//= require_tree .
</pre>

<b>application.css.sass</b>
<pre>
<h2>rename to .sass extension</h2>
$ <b>ren application.css -> application.css.scss</b>

/* <b>before</b>
 ...
 *
 *= require_tree .
 *= require_self
 */
</pre>

1) Delete the <b>require</b>s and change to <b>@import</b> so the bootstrap styling is available to all .css   
2) Add other <b>@import<b>s as needed and to maintain precedence.
<pre>
/* after
 ...
 */
<b>@import "bootstrap";
@import "borders";
@import "site";
@import "nav";</b>
</pre>

<h2>Adding Bootstrap Javascript</h2>

1) <b>jquery</b> needs to be before <b>jquery_ujs</b>   
2) any jquery needs to be before <b>bootstrap-sprockets</b>
<em>(should look like below)</em>
<pre>
<em># app/asets/javascript/application.js</em>

// This is a manifest file that'll be compiled into application.js, which will include all the files
// listed below.
//
// Any JavaScript/Coffee file within this directory, lib/assets/javascripts, vendor/assets/javascripts,
// or any plugin's vendor/assets/javascripts directory can be referenced here using a relative path.
//
// It's not advisable to add code directly here, but if you do, it'll appear at the bottom of the
// compiled file.
//
// Read Sprockets README (https://github.com/rails/sprockets#sprockets-directives) for details
// about supported directives.
//
<b>//= require jquery
//= require jquery_ujs
//= require turbolinks
//= require bootstrap-sprockets
//= require_tree .</b>
</pre>

<h2>Gemfile</h2>

Add following gems to Gemfile
<pre>
gem 'sprockets-rails'  
gem 'bootstrap-sass', '~> 3.2.0'  
gem 'autoprefixer-rails' 

$ <b>bundle install</b>
</pre>


<b>Column Setup</b>
<pre>
<b>%body</b>
<b>.container</b>                     <em># <b>.container</b> is for fixed width</em>
                               <em># <b>.container-fluid</b> is for full with</em>
    <b>.row</b>
    <em>#sidebar</em><b>.col-xs-5</b>          <em># each .col-x-x indent group must add to 12</em>
      <b>.container.col-xs-7</b>
        <b>.row</b>             <em># aligns the following columns</em>
        <b>.dev.col-xs-6</b>   
        <b>.dev.col-xs-6</b>
</pre>

<h2>Grid System</h2>
<b>.container</b> for fixed-width  
<b>.container-fluid</b> for full-width

<pre>
The order is <b>always</b>

<b>.container</b>
    <b>.row</b>
        <b>.col-x-x</b>  <em>only a .col can follow a .row</em>
        
</pre>

###Breakpoint Widths Used By Bootstrap
&lt;576px <b>extra small</b>  


###Overriding bootstrap formatting

Create another class <b>.navbar-xs</b> and style accordingly
<pre>
.navbar-xs { min-height:28px; height: 28px; }
.navbar-xs .navbar-brand{ padding: 0px 12px;font-size: 16px;line-height: 28px; }
.navbar-xs .navbar-nav > li > a {  padding-top: 0px; padding-bottom: 0px; line-height: 28px; }
</pre>
