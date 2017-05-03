For single Choose One

models/sitterform.rb
<pre>
class Sitterform < ActiveRecord::Base
  belongs_to :belief_type
  attr_accessible :belief_type_id
end
</pre>

models/belief_type.rb  
<pre>
class BeliefType < ActiveRecord::Base
  has_many :sitterforms
  attr_accessible :name
end
</pre>

Accessible by  
<pre>
sitterform.belief_type.name
</pre>
