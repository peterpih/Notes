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

<h2>To send email in development</h2>
<pre>
<em># config/environments/development.rb</em>

  ActionMailer::Base.raise_delivery_errors = true
  ActionMailer::Base.perform_deliveries = true
  ActionMailer::Base.delivery_method = :smtp
  # SMTP settings for gmail
  ActionMailer::Base.smtp_settings = {
    :address              => "smtp.gmail.com",
    :port                 => 587,
    :domain               => 'gmail.com',
    :user_name            => ENV['EMAIL_USERNAME'],
    :password             => ENV['EMAIL_PASSWORD'],
    :authentication       => "plain",
    :enable_starttls_auto => true
  }
  </pre>
  
