###Generating a Model

<em>User</em> is the name of the model, with attributes <em>first-name</em>, <em>last-name</em>, <em>email</em>, and <em>password</em>

$ <b>rails generate model</b> <em>User</em> <em>first-name</em><b>:string</b> <em>last_name</em><b>:string</b> <em>email</em><b>:string</b> <em>password</em><b>:string</b>
<pre>
      invoke  active_record
      create    db/migrate/20161106075623_create_users.rb
      create    app/models/user.rb
      invoke    test_unit
      create      test/models/user_test.rb
      create      test/fixtures/users.yml
</pre>


<pre>
<em># app/models/sentence.rb</em>

class Sentence < ActiveRecord::Base
end
</pre>

<pre>
<em># db/migrate/20151213121015_create_sentences.rb</em>

class CreateSentences < ActiveRecord::Migration
  def change
    create_table :sentences do |t|
      t.integer :order
      t.text :lesson
      t.text :text

      t.timestamps null: false
    end
  end
end
</pre>

<pre>
<em># test/fixtures/sentences.yml</em>

# Read about fixtures at http://api.rubyonrails.org/classes/ActiveRecord/FixtureSet.html

one:
  order: 1
  lesson: MyText
  text: MyText

two:
  order: 1
  lesson: MyText
  text: MyText
</pre>

<pre>
<em># test/models/sentence_test.rb</em>

require 'test_helper'

class SentenceTest < ActiveSupport::TestCase
  # test "the truth" do
  #   assert true
  # end
end
</pre>

####Create Database Migration Only
<pre>
<b>rails generate migration</b> <em>CreateDuplicates</em>
    invoke  active_record  
    <b>create</b>  db/migrate/20160520211611_create_duplicates.rb
</pre>

Use this is after manually creating
<pre>
<em># app/models/duplicate.rb</em>

<b>class</b> <em>Duplicates</em> <b>< ActiveRecord::Base</b>
<b>end</b>
</pre>
