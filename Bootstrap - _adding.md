&#42;&#42;[How to install Bootstrap 4 in Rails](http://mixandgo.com/blog/how-to-install-bootstrap-4-in-rails)

[Integrating Rails and Bootstrap, Part 1 - the Installation](https://launchschool.com/blog/integrating-rails-and-bootstrap-part-1)

[Bootstrap Grid Examples](http://getbootstrap.com/examples/grid/)

###Adding Bootstrap

<b>application.js</b>
<pre>
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
//= require bootstrap-sprockets</b>
//= require_tree .
</pre>

<b>application.css.sass</b>
<pre>
<em>rename to .sass extension</em>
$ <b>ren application.css -> application.css.sass</b>

/* before
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

<b>application.js</b>

1) <b>jquery</b> needs to be before <b>jquery_ujs</b>   
2) any jquery needs to be before <b>bootstrap-sprockets</b>
<em>(should look like below)</em>
<pre>
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

###Gemfile

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

###Grid System
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
