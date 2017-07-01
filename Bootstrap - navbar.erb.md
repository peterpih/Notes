<pre>
&lt;nav class="navbar navbar-default"&gt;
  &lt;div class="container-fluid"&gt;
    &lt;!-- Brand and toggle get grouped for better mobile display --&gt;
    &lt;div class="navbar-header"&gt;
      &lt;button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
        &lt;span class="sr-only">Toggle navigation</spanv
        &lt;span class="icon-bar">&lt;/span&gt;
        &lt;span class="icon-bar">&lt;/span&gt;
        &lt;span class="icon-bar">&lt;/span&gt;
      &lt;/button&gt;
      &lt;%= link_to 'Brand', root_path, class: 'navbar-brand' %&gt;
    &lt;/div&gt;

    &lt;!-- Collect the nav links, forms, and other content for toggling -->
    &lt;div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1"&gt;
      &lt;ul class="nav navbar-nav"&gt;
        &lt;li class="active"&gt;&lt;a href="#"&gt;Link &lt;span class="sr-only"&gt;(current)&lt;/span&gt;&lt;/a&gt;&lt;/li&gt;
        &lt;li&gt;&lt;a href="#"&gt;Link&lt;/a&gt;&lt;/li&gt;
        &lt;li class="dropdown"&gt;
        
          &lt;a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" 
                                aria-expanded="false"&gt;Dropdown &lt;span class="caret"&gt;&lt;/span&gt;&lt;/a&gt;
                                
          &lt;ul class="dropdown-menu"&gt;
            &lt;li&gt;&lt;a href="#"&gtAction&lt;/a&gt;&lt;/li&gt;
            &lt;li&gt;&lt;a href="#">Another action&lt;/a&gt;&lt;/li>
            &lt;li&gt;&lt;a href="#">Something else here&lt;/a></li>
            &lt;li role="separator" class="divider"&gt;&lt;/li>
            &lt;li&gt;&lt;a href="#">Separated link&lt;/a&gt;&lt;/li>
            &lt;li role="separator" class="divider"&gt;&lt;/li>
           &lt;li><a href="#">One more separated link&lt;/a&gt;&lt;/li>
          &lt;/ul>
        &lt;/li>
      &lt;/ul>
      &lt;form class="navbar-form navbar-left">
        &lt;div class="form-group">
          &lt;input type="text" class="form-control" placeholder="Search">
        &lt;/div>
        &lt;button type="submit" class="btn btn-default">Submit&lt;/button>
      &lt;/form>
      &lt;ul class="nav navbar-nav navbar-right">
        &lt;li><a href="#">Link</a>&lt;/li>
        &lt;li class="dropdown">
          &lt;a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Dropdown <span class="caret"></span></a>
          &lt;ul class="dropdown-menu">
            &lt;li><a href="#">Action</a>&lt;/li>
            &lt;li><a href="#">Another action&lt;/a></li>
            &lt;li><a href="#">Something else here&lt;/a></li>
            &lt;li role="separator" class="divider">&lt;/li>
            &lt;li><a href="#">Separated link</a>&lt;/li>
          &lt;/ul>
        &lt;/li>
      &lt;/ul>
    &lt;/div><!-- /.navbar-collapse -->
  &lt;/div><!-- /.container-fluid -->
&lt;/nav>
</pre>
