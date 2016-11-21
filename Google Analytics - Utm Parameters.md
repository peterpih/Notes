##Click here for [Google URL Builder](https://ga-dev-tools.appspot.com/campaign-url-builder/)


an interesting blog: https://support.google.com/analytics/answer/1033863?hl=en

ALways include tags:
<pre>
<b>utm_campaign</b>:  The individual campaign name, slogan, promo code, etc. for a product.

<b>utm_medium</b>:    The advertising or marketing medium, for example: cpc, banner, email newsletter.

<b>utm_source</b>:    Identify the advertiser, site, publication, etc. that is sending traffic to your 
               property, for example: google, newsletter4, billboard.  
</pre>

optional tags
<pre>
<b>utm_term</b>:      Identify paid search keywords. If you're manually tagging paid keyword campaigns, 
               you should also use utm_term to specify the keyword.

<b>utm_content</b>:   Used to differentiate similar content, or links within the same ad. For example, 
               if you have two call-to-action links within the same email message, you can use 
               <b>utm_content</b> and set different values for each so you can tell which version is 
               more effective.
               
               You can use Campaign Content to indicate the specific ad, button, or link that was 
               clicked
</pre>

###Hierarchy
<pre>
utm_campaign - Recommended Books

utm_source - Email

utm_medium - (could be today's date)
