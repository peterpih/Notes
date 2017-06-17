<h2>Use spinner partial to display</h2>
<pre>
&lt;%= render 'common/spinner' %&gt;
</pre>

<h2>Setup the spinner partial</h2>
$ <b>mkdir app/views/common</b>
<pre>
<em># common/_spinner.html.erb</em>

&lt;div id='spinner' class='row col-md-12 text-center spinner' style='display:none;'&gt;
  &lt;i class='fa fa-spinner fa-spin fa-2x'&gt; Processing...
&lt;/div&gt;
</pre>

<h2>Add js code</h2>  
Add these functions to other js code to **show** and **hide** spinner
<pre>
<em># assets/javascript/application.js</em>

var hide_spinner = function(){
  $('#spinner').hide;
}

var show_spinner = function(){
  $('#spinner').show;
}
</pre>

<h2>js for showing and hiding spinner</h2>
<pre>
$('#<em>id-for-ajax-request</em>).on('ajax:before', function(event, data, status){
  show_spinner();
});

$('#<em>id-for-ajax-request</em>).on('ajax:after', function(event, data, status){
  hide_spinner();
});
