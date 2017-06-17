To show the html on a page use <b>puts page.body</b>
<pre>
 it 'Sitterform signature_checkbox needs to be checked', :sitterform do
    visit '/login'
    sign_in(@user_sitterform)
    visit '/'
    click_link('Sitter Registration Form')
    <b>puts page.body</b>
    choose('A firm believer')
    fill_in('Electronic Signature', :with => 'John Doe')
    click_button('Submit')
    expect(page).to have_content 'Signature checkbox needs to be checked'
  end
</pre>

<h2>Databasecleaner</h2>  

In <b>Gemfile</b>
<pre>
group :test do
  gem 'database_cleaner', '1.6.0'
end
</pre>

Setup Database cleaner support file (use :truncation)

<pre>
<em># spec/support/database_cleaner.rb</em>


RSpec.configure do |config|
 
  config.before(:suite) do
    DatabaseCleaner.clean_with(:truncation)
  end
 
  config.before(:each) do
    DatabaseCleaner.strategy = :transaction
  end
 
  config.before(:each, :js => true) do
    DatabaseCleaner.strategy = :truncation
  end
 
  config.before(:each) do
    DatabaseCleaner.start
  end
 
  config.after(:each) do
    DatabaseCleaner.clean
  end
 
end
</pre>
