[LET'S ENCRYPT WITH A RAILS APP ON HEROKU](https://collectiveidea.com/blog/archives/2016/01/12/lets-encrypt-with-a-rails-app-on-heroku)  step-by-step, partially below

<pre>
$ sudo certbot certonly --manual
Password:&lt;CR&gt;
Saving debug log to /var/log/letsencrypt/letsencrypt.log
Please enter in your domain name(s) (comma and/or space separated)  (Enter 'c'
to cancel):new.soonerbaptist.org
Obtaining a new certificate
Performing the following challenges:
http-01 challenge for new.soonerbaptist.org

-------------------------------------------------------------------------------
NOTE: The IP of this machine will be publicly logged as having requested this
certificate. If you're running certbot in manual mode on a machine that is not
your server, please ensure you're okay with that.

Are you OK with your IP being logged?
-------------------------------------------------------------------------------
(Y)es/(N)o: <b>Y</b>
</pre>


You can check the long key (below bold) displays correctly locally by using localhost:3000/.well-known/acme...
<pre>
-------------------------------------------------------------------------------
Make sure your web server displays the following content at
http://new.soonerbaptist.org/.well-known/acme-challenge/fRw-PpDIiA8y2TO8Nrh2VW4d4SsyUvZ7-Eos9RZl6EM before continuing:

<b>fRw-PpDIiA8y2TO8Nrh2VW4d4SsyUvZ7-Eos9RZl6EM.OGiwEUMi3VpdWBK0OmrLyxII_anDIarAxDpRIlePB54</b>

If you don't have HTTP server configured, you can run the following
command on the target server (as root):

mkdir -p /tmp/certbot/public_html/.well-known/acme-challenge
cd /tmp/certbot/public_html
printf "%s" fRw-PpDIiA8y2TO8Nrh2VW4d4SsyUvZ7-Eos9RZl6EM.OGiwEUMi3VpdWBK0OmrLyxII_anDIarAxDpRIlePB54 > .well-known/acme-challenge/fRw-PpDIiA8y2TO8Nrh2VW4d4SsyUvZ7-Eos9RZl6EM
# run only once per server:
$(command -v python2 || command -v python2.7 || command -v python2.6) -c \
"import BaseHTTPServer, SimpleHTTPServer; \
s = BaseHTTPServer.HTTPServer(('', 80), SimpleHTTPServer.SimpleHTTPRequestHandler); \
s.serve_forever()" 
-------------------------------------------------------------------------------
</pre>

<b>DO NOT hit return until you have deployed the long key to the heroku app</b>
<pre>
Press Enter to Continue
Waiting for verification...
Cleaning up challenges
Generating key (2048 bits): /etc/letsencrypt/keys/0000_key-certbot.pem
Creating CSR: /etc/letsencrypt/csr/0000_csr-certbot.pem

IMPORTANT NOTES:
 - Congratulations! Your certificate and chain have been saved at
   /etc/letsencrypt/live/new.soonerbaptist.org/fullchain.pem. Your
   cert will expire on 2017-06-17. To obtain a new or tweaked version
   of this certificate in the future, simply run certbot again. To
   non-interactively renew *all* of your certificates, run "certbot
   renew"
 - If you like Certbot, please consider supporting our work by:

   Donating to ISRG / Let's Encrypt:   https://letsencrypt.org/donate
   Donating to EFF:                    https://eff.org/donate-le
</pre>

[Multiple SSL Certificates in One Heroku Application](http://stackoverflow.com/questions/13448012/multiple-ssl-certificates-in-one-heroku-application/36474485#36474485)

[Let's Encrypt](https://letsencrypt.org) - open free ssl (something to look into)

[HOWTO setup SSL with Rails & Heroku](http://readysteadycode.com/howto-setup-ssl-with-rails-and-heroku)

In Rails:need to add
<pre>
config.force_all = true
</pre>
to config/environments/production.rb

and possibly change
<pre>
&lt;script src="http://code.jquery.com/jquery-2.1.0.js"&gt;&lt;/script&lt
to
&lt;script src="//code.jquery.com/jquery-2.1.0.js"&gt;&lt;/script&gt;
</pre>

to secure assets and not get "mixed" content warnings.

The external resource will then be requested with whichever 
protocol the page was requested with, i.e. either https or http. 
So it’ll work just fine with or without SSL.
