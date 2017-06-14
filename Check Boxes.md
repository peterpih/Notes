Trying to aling check box and label  


https://stackoverflow.com/questions/24109276/how-to-align-input-and-label-from-collection-check-boxes/24109846

https://stackoverflow.com/questions/24109276/how-to-align-input-and-label-from-collection-check-boxes/24109846

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
