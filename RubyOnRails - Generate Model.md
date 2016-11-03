###Generating a Model

"<em>sentence</em>" is the name of the model, with attributes "<em>order</em>", "<em>lesson</em>", and "<em>text</em>"


<pre>
<b>rails generate model</b> <em>sentence</em> <em>order</em><b>:integer</b> <em>lesson</em><b>:text</b> <em>text</em><b>:text</b>
</pre>
generates the following files :
<pre>
<b>app/models/</b><em>sentence</em><b>.rb</b>
<b>db/migrate/</b><em>20151213121015_create_sentences</em><b>.rb</b>
<b>test/fixtures/</b><em>sentences</em><b>.yml</b>
<b>test/models/</b><em>sentence_test</em><b>.rb</b>
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
