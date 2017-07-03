<h2>Generate files</h2>

$ <b> rails generate mailer example_mailer</b>
<pre>
      create  app/mailers/example_mailer.rb
      invoke  erb
      create    app/views/example_mailer
   identical    app/views/layouts/mailer.text.erb
   identical    app/views/layouts/mailer.html.erb
      invoke  test_unit
      create    test/mailers/example_mailer_test.rb
      create    test/mailers/previews/example_mailer_preview.rb
</pre>

<h2>Change the default return email address</h2>
<pre>
# app/mailers/example_mailer.rb

    class ExampleMailer < ActionMailer::Base
      default from: "from@example.com"

      <b>def sample_email(user)
        @user = user
        mail(to: @user.email, subject: 'Sample Email')
      end</b>
    end
</pre>
