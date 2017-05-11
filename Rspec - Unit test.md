<pre>
validates :title, presence: true, length: {minimum:3, maximum:20}
</pre>
<pre>
it { <b>should have_many</b>(:known_deads) }  
it { <b>should have_many</b>(:users)<b>.through</b>(:known_deads) }  
it { <b>should belong_to</b>(:user) }  
it { <b>should allow_mass_assignment_of</b> :title }
it { <b>should validate_uniqueness_of</b> :name }
</pre>
