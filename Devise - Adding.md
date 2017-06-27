On Udemy: https://www.udemy.com/the-complete-ruby-on-rails-developer-course/learn/v4/t/lecture/3853646?start=0

The credit card form is added in the <b>Sign Up</b> window sicne the user ill pay to <b>register</b>

<h2>Add payment model</h2>
$ <b> rail g model Payment email:string token:string user_id:integer</b>   

The <b>token</b> is sent back and forth to Stripe, but is <b>not</b> stored in the database.

<h2>Add Payment to User</h2>
<pre>
class User &lt; ApplicationRecord
# Include default devise modules. Others available are:
# :confirmable, :lockable, :timeoutable and :omniauthable
devise :database_authenticatable, :registerable, :confirmable,
       :recoverable, :rememberable, :trackable, :validatable

  <b>has_one :payment</b>
  <b>accepts_nested_attributed_for :payment</b>
end
</pre>

<h2>Setup Payment model</h2>

<pre>
class Payment &lt; ApplicationRecord  
  attr_accessor :card_number, :card_cvv, :card_expires_month, :card_expires_year  
  belongs_to :user  

  def self.month_options  
    Dare.MONTHNAMES::.compact.each_with_index.map { | name, i| ["#{i+1} - #{name}", i+1 ]}  
  end  

  def self.year_options  
    (Date.today.year...(Date.today.year+10)).to_a  
  end  

  def process_payment
    customer = Strip::customer.create email: email, card: token

    Stripe::Charge.create customer: customer.id,
                          amount: 1000
                          description: 'Premium',
                          currency: 'usd'
end
</pre>
