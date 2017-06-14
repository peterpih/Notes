Trying to align check box and label  


https://stackoverflow.com/questions/24109276/how-to-align-input-and-label-from-collection-check-boxes/24109846

https://stackoverflow.com/questions/24109276/how-to-align-input-and-label-from-collection-check-boxes/24109846

<h2>Standard checkbox</h2>
**type** makes _input_ a checkbox
**name** makes multiple checkboxes a _group_
<pre>
&lt;input <b>type='checkbox'</b> name="firstname" value="John"&gt;First name:&lt;/label&gt;
</pre>

<h2>Standard checkbox with selectable label</h2>  
the 'my' connects the two making the label selectable
<pre>
&lt;input type="checkbox" id='<b>my</b>' name="firstname" value="John"&gt;
&lt;label for='<b>my</b>'&gt;First name:&lt;/label&gt;
</pre>

this is from [SO: check_box_tag with label_tag click action](https://stackoverflow.com/questions/16095060/check-box-tag-with-label-tag-click-action)
<pre>
<%= label_tag "some_name", raw("#{check_box_tag('some_name')} Click label to check") %>
</pre>

this is from RailsCast [#17 HABTM Checkboxes (revised) ](http://railscasts.com/episodes/17-habtm-checkboxes-revised?autoplay=true)
<pre>
&lt;div style="background-color: yellow"&gt;
  &lt;%= hidden_field_tag 'meal[food_ids][]', nil %&gt;
  &lt;% Food.all.each do |food| %>
    &lt;%= check_box_tag 'meal[food_ids][]', food.id, @meal.food_ids.include?(food.id), id: dom_id(food)%&gt;
    &lt;%= food.name %&gt;&lt;br&gt;
  &lt;% end %&gt;
&lt;/div>
</pre>
