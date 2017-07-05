<h2>Create a controller</h2>
<pre>
<em># email_controller.rb</em>

class EmailController < ApplicationController

  def send_an_email
    MyMailer.send_an_email(to: @user)
  end
end
</pre>

<h2>Create mailer</h2>

$ <b>rails generate mailer MyMailer</b>

<h2>Create email forms</h2>
<pre>
# views/my_mailer/send_an_email.html.erb

</pre>
