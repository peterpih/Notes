From Udemy: https://www.udemy.com/the-complete-ruby-on-rails-developer-course/learn/v4/t/lecture/3853672?start=0

Add to
<pre>
# application.html.erb

    &lt;!-- For all other devices -->
    &lt;!-- Size should be 32 x 32 pixels -->
    &lt;%= favicon_link_tag 'favicon.ico', :rel => 'shortcut icon' %&gt;
    <b>&lt;%= javascript_include_tag "https://js.stripe.com/v2" %&gt;</b>
    &lt;%= javascript_include_tag "application" %&gt;
<pre>
