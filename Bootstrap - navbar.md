Reference is:https://www.w3schools.com/bootstrap/bootstrap_navbar.asp

A standard navigation bar is created with 
<pre>
<em>(HTML)</em>  &lt;nav class="navbar navbar-default"&gt;

<em>(HAML)</em>  %nav.navbar.navbar-default 
</pre>

###Ordering of bootstrap classes
<pre>
<b>%nav.navbar.navbar-default</b>
  //navbar-default <em>*(white inverted)*</em>
  //navbar-inverted <em>*(black navbar)*</em>
  // %nav - tag
  // navbar - type of element
  // navbar-default - type of styling
  
  <b>.container-fluid</b>
    // container stretches all the way across the page
    
    <b>.navbar-header</b>
      // contents of the navbar
      
      <b>.navbar-brand</b>
        // for a logo, a nonselectable choice in navbar
        
      <b>%ul.nav.navbar-nav</b>
        // for menu items
          %li= link_to 'Link1', "#", class: 'active'
          %li= link_to 'Link2', "#"
          %li= link_to 'Link3', "#"
</pre>

Hamburger
<pre>
&lt;button type="button" class="navbar-toggle" data-toggle="collapse" data-target="#myNavbar"&gt;
  &lt;span class="icon-bar"&gt;&lt;/span&gt;
  &lt;span class="icon-bar"&gt;&lt;/span&gt;
  &lt;span class="icon-bar"&gt;&lt;/span&gt;                        
&lt;/button&gt;
</pre>

"Brand link"
usually goes in left-most side
<pre>
&lt;a class="navbar-brand" href="#">WebSiteName&lt;/a&gt;
</pre>

%nav - tag  

Navbar Menu picks

The whole &lt;div&gt;..&lt;/div&gt; gets collapsed into the hamburger
<pre>
&lt;div class="collapse navbar-collapse" id="myNavbar"&gt;
  &lt;ul class="nav navbar-nav"&gt;
    left-side picks
    &lt;/ul&gt; <em>(if this ul is not here everything will be on left side)</em>
&lt;ul class="nav navbar-nav navbar-right"&gt;
    right-side picks
  &lt;li class="active"&gt;&lt;a href="/codeforokc"&gt;Home&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="/codeforokc/projects"&gt;Projects&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="/codeforokc/about"&gt;About&lt;/a&gt;&lt;/li&gt; 
&lt;/div&gt;
</pre>

<pre>
.navbar-inverse  

.navbar-default
       -fixed-top  
       -fixed-bottom
</pre>

###Drop Down
<pre>
%nav.navbar.navbar-default
  .container-fluid
    .navbar-header
      = link_to 'WebSiteName', "#", class: "navbar-brand"
    %ul.nav.navbar-nav
      %li= link_to 'Home', "#", class: "active"
     %li.dropdown
        = link_to "#", do, class: "dropdown-toggle", {'data-toggle'=>'dropdown'}
          Page 1
          .caret
        %ul.dropdown-menu
          %li= link_to 'Page 1-1', "#"
          %li= link_to 'Page 1-2', "#"
          %li= link_to 'Page 1-3', "#" 
      %li= link_to 'Page 2', "#"
      %li= link_to 'Page3', "#"
</pre>

###Standard navbar
<pre>
&lt;body&gt;
&lt;nav class="navbar navbar-default"&gt;
  &lt;div class="container-fluid"&gt;
    &lt;div class="navbar-header"&gt;
      &lt;a class="navbar-brand" href="#"&gt;WebSiteName&lt;/a&gt;
    &lt;/div&gt;
    &lt;ul class="nav navbar-nav"&gt;
      &lt;li class="active"&gt;&lt;a href="#"&gt;Home&lt;/a&gt;&lt;/li&gt;
      &lt;li&gt;&lt;a href="#"&gt;Page 1&lt;/a&gt;&lt;/li&gt;
      &lt;li&gt;&lt;a href="#"&gt;Page 2&lt;/a&gt;&lt;/li&gt; 
      &lt;li&gt;&lt;a href="#"&gt;Page 3&lt;/a&gt;&lt;/li&gt; 
    &lt;/ul&gt;
  &lt;/div&gt;
&lt;/nav&gt;
...
</pre>
