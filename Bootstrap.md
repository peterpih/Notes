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
$ <b>ren application.css -> application.css.sass</b>

/*
 * This is a manifest file that'll automatically include all the stylesheets available in this directory
 * and any sub-directories. You're free to add application-wide styles to this file and they'll appear at
 * the top of the compiled file, but it's generally better to create a new file per style scope.
 *
 *= require_tree .
 *= require_self
 */
<b>@import "bootstrap-sprockets"</b>
<b>@import "bootstrap"</b>
</pre>

###Column Setup
<pre>
<b>%body</b>
<b>.container.container-fluid</b>      <em># allow for flowing</em>
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

###Breakpoints
&lt;576px <b>extra small</b>  
