###Do a migration

$ <b>rails g migration</b> <em>UsefulMigrationName</em>  
$ <b>rake db:migrate</b>

###Undo a migration

$ <b>rake db:rollback</b>  
$ <b>rails destroy migration</b> <em>UsefulMigrationName</em>

###Create A Table

$ <b>rails g migration</b> <em>UsefulMigrationName</em>  
 which creates
<pre>
# db/migrate/YYYYMMDDHHMMSS_useful_migration_name.rb

class UsefulMigrationName &lt; ActiveRecord::Migration
  def change
  end
end
</pre>

and then you can edit

<pre>
class UsefulMigrationName &lt; ActiveRecord::Migration[5.0]
  def change
    create_table :products do |t|
      t.string :name
      t.text :description
 
      t.timestamps
    end
  end
end
</pre>

###Delete A Table

$ <b>rails g migration</b> <em>UsefulMigrationName</em>  
 which creates
<pre>
# db/migrate/YYYYMMDDHHMMSS_useful_migration_name.rb

class UsefulMigrationName &lt; ActiveRecord::Migration
  def change
  end
end
</pre>

and then you can edit

<pre>
class UsefulMigrationName &lt; ActiveRecord::Migration
  def change
    <b>drop_table</b> <em>:table_name</em>
    end
  end
end
</pre>

###Datatypes (t.<em>datatype</em>)
<pre>
:binary
:boolean
:date
:datetime
:decimal
:float
:integer
:bigint
:primary_key
:references
:string
:text
:time
:timestamp
</pre>

###Change Column Name
To change column "<b>new</b>" to column "<b>status</b>" in table "<b>events</b>" and change its type to "<b>integer</b>"    
use the following rails command and <b>give it a name that will help you remember!</b>

$ <b>rails g migration</b> <em>ChangeColumnNameNewToStatus</em>
<pre>
Running via Spring preloader in process 6365
      invoke  active_record
      create    db/migrate/20161207022049_rename_column_new_to_status.rb
</pre>
it will generate the migration file
<pre>
# db/migrate/20161207022049_rename_column_new_to_status.rb

class RenameColumnNewToStatus &lt; ActiveRecord::Migration
  def change
  end
end
</pre>
which you then need to edit
<pre>
class RenameColumnNewToStatus &lt; ActiveRecord::Migration
  def change
    <b>rename_column :events, :new, :status</b>
    <b>change_column :events, :status, :integer</b>
  end
end
</pre>
<pre>
class ChangeProductsPrice < ActiveRecord::Migration[5.0]
  def up
    change_table :products do |t|
      t.change :price, :string
    end
  end
 
  def down
    change_table :products do |t|
      t.change :price, :integer
    end
  end
end
</pre>

$ rails generate migration add_email_to_users

add_column  
remove_column  

add_index  
