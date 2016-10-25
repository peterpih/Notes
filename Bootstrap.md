[Integrating Rails and Bootstrap, Part 1 - the Installation](https://launchschool.com/blog/integrating-rails-and-bootstrap-part-1)

[Bootstrap Grid Examples](http://getbootstrap.com/examples/grid/)

<pre>
%body
  .container.container-fluid
    .row
      #sidebar.col-xs-5
      .container.col-xs-7
        .row     <em>aligns the following columns</em>
          .dev.col-xs-6   <em>each .col-x-x indent must add to 12</em>
          .dev.col-xs-6
</pre>
