#Rails Commands

<pre>
<b>rails g</b>enerate <b>model</b> <em>model_name              # use singular</em>
$ rails generate model User

<b>rails g</b>enerate <b>controller</b> <em>controller-name    # use plural</em>
$ rails generate controller Users

<b>rails generate migration</b> <em>migration_name</em>

<b>rails s</b>erver                                 <em># run the local server</em>

<b>rails new</b> <em>app_name                           # create a new app</em>
</pre>

###Generating a Model

<pre>
<b>rails generate model<b> <em>lesson order:integer lesson:text text:text</em>
</pre>
generates :
'''
	app/models/sentence.rb
	db/migrate/20151213121015_create_sentences.rb
	test/fixtures/sentences.yml
	test/models/sentence_test.rb
	
