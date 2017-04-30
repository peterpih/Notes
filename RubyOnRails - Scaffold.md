ActiveAdmin messes with <b>rails scaffold</b> so the generated controller uses InheretedResources   
to get back to using ApplicationController and create all the CRUD methods use
<pre>
$ <b>rails g scaffold</b> <em>Foobar</em> name:string <b>-c=scaffold_controller</b>
</pre>

To Generate:
<pre>
$ <b>rails generate scaffold</b> <em>model attribute:type</em>
$ <b>rails g scaffold</b> <em>model attribute:type</em>
</pre>

To Reverse:
<pre>
$ <b>rails destroy scaffold</b> <em>model attribute:type</em>
</pre>
