<h2>Add to Gemfile</h2>

<pre>
<em># Gemfile</em>

gem 'will_paginate', '3.0.7'
gem 'bootstrap-will_paginate', '0.0.10'
</pre>

$ <b>bundle install --without production</b>

<h2>In articles_controller.rb file</h2>

<pre>
def index
  @articles = Article.paginate(page: params[:page], per_page: 5)
end
</pre>

<h2>In index.hml.erb</h2>

<pre>
  &lt;div align='center'&gt;
    &lt;%= will_paginate %&gt;
  &lt;/div&gt;

    &lt;%= render 'my_partial' %&gt;

  &lt;div align='center'&gt;
    &lt;%= will_paginate %&gt;
  &lt;/div&gt;
</pre>
