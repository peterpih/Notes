
<h2>For fillin fields</h2>
<pre>
    <b>check</b> <em>"Yes, I accept the Terms of Use"</em>
    <b>click_on</b> <em>"Register"</em>
</pre>
<pre>
    <b>fill_in</b> <em>&quot;user_email&quot;</em><b>, :with =&gt;</b> <em>&#39;asd@example.com&#39;</em>
</pre>
<pre>
    <b>fill_in_reg(</b>email: 'CASE@sensative.com', email_confirmation: 'CASE@sensative.com', password: ''<b>)</b>
    <b>expect(find_field(</b><em>'user_email'</em><b>).value).to eq</b> <em>'case@sensative.com'</em>
    <b>expect(find_field(</b><em>'user_email_confirmation'</em><b>).value).to eq</b> <em>'case@sensative.com'</em>   
</pre>
