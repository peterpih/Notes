<h2>Create a controller</h2>

<pre>
<em># email_controller.rb</em>

  class EmailController < ApplicationController

    def send_an_email
      MyMailer.<b>send_an_email</b>(to: @user)
      flash[:notice] = 'Successfully emailed.'
      redirect_to root_path
    end
  end
</pre>

<h2>Create mailer</h2>

$ <b>rails generate mailer MyMailer</b>

<pre>
<em># mailer/my_mailer.rb</em>

  class MyMailer &lt; ApplicationMailer
    default from: "<em>no_reply@gmail.com</em>"

    def <b>send_an_email</b>(user)
      @user = user
      mail(to: @user.email, subject: 'Sample Email')
    end
  end
</pre>

<h2>Create email forms</h2>

<pre>
# views/my_mailer/<b>send_an_email</b>.html.erb

</pre>

<h2>To send email in development</h2>

<em>Need to use <b>gmail</b> in development</em>

<pre>
<em># config/initializers/<b>mail.rb</b></em>

if Rails.env.development?
  ActionMailer::Base.raise_delivery_errors = true
  ActionMailer::Base.perform_deliveries = true
  ActionMailer::Base.delivery_method = :smtp
  ActionMailer::Base.smtp_settings = {
    :address              =&gt; "smtp.gmail.com",
    :port                 =&gt; 587,
    :domain               =&gt; '<b>gmail.com</b>',
    :user_name            =&gt; ENV['EMAIL_USERNAME'],
    :password             =&gt; ENV['EMAIL_PASSWORD'],
    :authentication       =&gt; "plain",
    :enable_starttls_auto =&gt; true
  }
end
  </pre>
  
  <h2>To send email in production</h2>
  
  <em>Need to use <b>SendGrid</b> on Heroku </em>
  
  <pre>
  <em># config/initializers/<b>mail.rb</b></em>
  
if Rails.env.production?
  ActionMailer::Base.raise_delivery_errors = true
  ActionMailer::Base.perform_deliveries = true
  ActionMailer::Base.delivery_method = :smtp
  ActionMailer::Base.smtp_settings = {
    :user_name =&gt; ENV['SENDGRID_USERNAME'],
    :password =&gt; ENV['SENDGRID_PASSWORD'],
    :domain =&gt; 'heroku.com',
    :address =&gt; '<b>smtp.sendgrid.net</b>',
    :port =&gt; 587,
    :authentication =&gt; :plain,
    :enable_starttls_auto =&gt; true
  }
  </pre>
