[**Migration** (RailsGuide.org)](http://guides.rubyonrails.org/v3.2/migrations.html)

[Migration for change column (SO)](http://stackoverflow.com/questions/2799774/rails-migration-for-change-column)

<h2>Always run rake db:migrate</h2>

<h2>To create a Migration</h2>

$ <b>rails generate migration</b> <em>UsefulMigrationName</em>  
$ <b>rails g migration</b> <em>UsefulMigrationName</em>   

Rails will create a new migration file in db/migrate
<pre>
class UsefulMigrationName &lt; ActiveRecord::Migration[5.0]
  def change
    ...
  end
end
</pre>

<h2>Changeing A Column</h2>
<pre>
<b>rename_table</b>  <em>:old-table,  :new-table</em>   <em>( note _id_seq will automatically be renamed )</em>   
<b>rename_column</b> <em>:table-name,  :old-column,  :new-column</em>   
<b>remove_column</b> <em>:table-name,  :old-column</em>   
<b>change_column</b> <em>:table-name,  :old-column, :integer</em>   
</pre>

###Setting a Default Value
<pre>
change_column :table-name, :column-name, :column-type, :default => 0
</pre>

###Rollback a Migration

$ <b>rake db:rollback</b>   
$ <b>rake db:rollback STEP=</b><em>3</em>         <em># rollback the last 3 migrations</em>

###Delete A Migration (do after 'rake db:rollback')   
$ <b>rails destroy migration</b> <em>UsefulMigrationName</em>   

###Redo a Migration (rollback and re-migrate in one step)

$ b>rake db:migrate:redo</b>    
$ <b>rake db:migrate:redo TIMES=</b><em>3</em>        <em># redo the last 3 migrations</em>  

###Run A Specific Migration

$ <b>rake db:migrate:up VERSION=</b><em>20080906120000</em>    
$ <b>rake db:migrate:down VERSION=</b><em>20080906120000</em>

-----------------------------------------------------------------------------------------------------
###Set Default Column Value

$ rails g migration AddUploadToUser upload:boolean

then need to edit the migration file and add default value
<pre>
# db/migrate/YYYYMMDDHHMMSS_add_upload_to_user.rb

class AddUploadToUser &lt; ActiveRecord::Migration[5.0]
  def change
    add_column :users, :upload, :boolean, <b>:default => false</b>
  end
end

</pre>

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
