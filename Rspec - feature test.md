<h2>Sitepoint Video Tutorial</h2>  

[Setting Up Automated Testing with RSpec](https://www.sitepoint.com/premium/screencasts/setting-up-automated-testing-with-rspec)  
[Managing Sample Data with Fixtures and Factories](https://www.sitepoint.com/premium/screencasts/managing-sample-data-with-fixtures-and-factories)   
[Testing Your Rails App Models with RSpec](https://www.sitepoint.com/premium/screencasts/testing-your-rails-app-models-with-rspec)   
[Testing Views, Routes, and Helpers for Problems in Your Rails App](https://www.sitepoint.com/premium/screencasts/testing-views-routes-and-helpers-for-problems-in-your-rails-app)   
[Ensure Functionality with RSpec Controller Testing](https://www.sitepoint.com/premium/screencasts/ensure-functionality-with-rspec-controller-testing)   
[Feature Tests with RSpec: Simulate User Behavior and Test Your Ruby App](https://www.sitepoint.com/premium/screencasts/feature-tests-with-rspec-simulate-user-behavior-and-test-your-ruby-app)

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
