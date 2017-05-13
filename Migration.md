[**Migration** (RailsGuide.org)](http://guides.rubyonrails.org/v3.2/migrations.html)

[Migration for change column (SO)](http://stackoverflow.com/questions/2799774/rails-migration-for-change-column)

To create a Migration
<pre>
<b>rails generate migration</b> <em>name-of-migration</em>  
<em>Rails will create a new migration file in db/migration</em>

example:
<b>rails generate migration</b> <em>duplicates</em>
</pre>

<h3><b>Renaming</b></h3>
<pre>
<b>rename_table</b>  <em>:old-table,  :new-table</em>   <em>( note _id_seq will automatically be renamed )</em>
<b>rename_column</b> <em>:table-name,  :old-column,  :new-column</em>
</pre>

<h3><b>Rollback</b> a Migration</h3>
<pre>
<b>rake db:rollback</b>
<b>rake db:rollback STEP=</b><em>3</em>         <em># rollback the last 3 migrations</em>
</pre>

<h3><b>Redo</b> a Migration (rollback and re-migrate in one step)</h3>
<pre>
<b>rake db:migrate:redo</b>  
<b>rake db:migrate:redo TIMES=</b><em>3</em>        <em># redo the last 3 migrations</em>
</pre>

<h3>Run A <b>Specific Migration</b></h3>
<pre>
<b>rake db:migrate:up VERSION=</b><em>20080906120000</em>
<b>rake db:migrate:down VERSION=</b><em>20080906120000</em>
</pre>

If you accidentally deleted the table manually, your migration needs to look like this
<pre>
class CreateRelationships < ActiveRecord::Migration
def <b>up</b>  <em>(instead of <b>change</b>)</em>
    create_table :relationships do |t|
      t.string :name
      t.string :typeof

      t.timestamps null: false
    end
  end
  def <b>down</b>
    <b>drop_table :relationships if ActiveRecord::Base.connection.table_exists? 'relationships'</b>
  end
end
</pre>
Then use
<pre>
$ rake db:migrate:<b>redo</b> VERSION=20170428203612
</pre>
since migrations already thinks the migration happened (status 'up') without the <b>.table_exists?</b> for the redo
it will first try to <b>drop_table</b>, but then it's already dropped (manually by you, this causes an error) 
then will do <b>create_table</b> and all should be good!
