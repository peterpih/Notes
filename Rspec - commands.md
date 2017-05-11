
<h2>For fillin fields</h2>
<pre>
    <b>fill_in</b> <em>\"user_email\"</em><b>, :with =></b> <em>\'asd@example.com\'</em>

    <b>fill_in_reg(</b>email: 'CASE@sensative.com', email_confirmation: 'CASE@sensative.com', password: ''<b>)</b>
    <b>expect(find_field(</b><em>'user_email'</em><b>).value).to eq</b> <em>'case@sensative.com'</em>
    <b>expect(find_field(</b><em>'user_email_confirmation'</em><b>).value).to eq</b> <em>'case@sensative.com'</em>   
</pre>
