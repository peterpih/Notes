###Create
<pre>
class CreateProducts < ActiveRecord::Migration[5.0]
  def change
    create_table :products do |t|
      t.string :name
      t.text :description
 
      t.timestamps
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

###Change
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
