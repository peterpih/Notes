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
