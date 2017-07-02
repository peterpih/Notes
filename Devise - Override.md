<h2>Creat your own version of the Registration Controller</h2>
<pre>
# app/controllers/registrations_controller.rb

<b>class RegistrationsController < Devise::RegistrationsController</b>
    def new
        super
    end

  def create
    # add custom create logic here
  end

  def update
    super
  end
end 
</pre>

<h2>In routes.rb</h2>
<pre>
 devise_for :users, :controllers =&gt; {:registrations =&gt; "registrations"}
</pre>

