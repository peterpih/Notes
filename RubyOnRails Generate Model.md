###Generating a Model

<pre>
<b>rails generate model</b> <em>lesson</em> <em>order</em><b>:integer</b> <em>lesson</em><b>:text</b> <em>text</em><b>:text</b>
</pre>
generates the following files :
<pre>
app/models/sentence.rb
db/migrate/20151213121015_create_sentences.rb
test/fixtures/sentences.yml
test/models/sentence_test.rb
</pre>
####app/models/sentence.rb
<pre>
class Sentence < ActiveRecord::Base
end
</pre>
####db/migrate/20151213121015_create_sentences.rb
<pre>
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
####test/fixtures/sentences.yml
<pre>
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
####test/models/sentence_test.rb
<pre>
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
