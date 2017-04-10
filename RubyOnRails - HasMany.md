https://agilewarrior.wordpress.com/2014/03/13/rails-has_many-example/

[Has Many Through Forms Rails](https://learn.co/lessons/has-many-through-forms-rails)

[Setting Up A Has Many / Has One Nested Association With Formtastic And Cocoon In Rails 4.2](http://www.binarywebpark.com/setting-up-a-has-many-has-one-nested-association-with-formtastic-and-cocoon-in-rails-4-2/)

White Listing params in Controller   
<pre>
  <em>model-name<b>_attributes</b></em> hash is used

  def survey_params
    params.require(:survey).permit(:name, <b>questions_attributes</b>:[<b>:id</b>, :content, :survey_id, <b>:_destroy</b>])
  end  
  
  <b>:id</b> - stops duplicating entries  
  <b>:_destroy</b> - allows deleting, it is a <em>hidden param</em>
</pre>
