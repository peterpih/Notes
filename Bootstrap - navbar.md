A standard navigation bar is created with 
<pre>
<em>(HTML)</em>  &lt;nav class="navbar navbar-default"&gt;

<em>(HAML)</em>  %nav.navbar.navbar-default 
</pre>

###Ordering
<pre>
<b>%nav.navbar.navbar-default</b>
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

%nav - tag  


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