###Commands

This assumes the model for User has already been defined.
<pre>
>>User.new  
>>User.create(name:'Peter', password:'asdfghjkl')  
</pre>

###Database Manipulation
<pre>
User.find_by(name:'Peter')  
User.first  
User.all

User.save
User.create
User.update_attributes(hash)

User.reload

User.errors
User.errors.full_messages
</pre>
