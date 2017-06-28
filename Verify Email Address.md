Check out email-address gem: https://github.com/afair/email_address

Several steps to verify an email address
- verify MX record
- verify server has the actual email address

<h2>Verify MX record on command line</h2>

$ <b>nslookup -type=mx</b> <em>gmail.com</em>

<pre>
Server:		208.67.220.220
Address:	208.67.220.220#53

Non-authoritative answer:
gmail.com	mail exchanger = 5 gmail-smtp-in.l.google.com.
gmail.com	mail exchanger = 10 alt1.gmail-smtp-in.l.google.com.
gmail.com	mail exchanger = 30 alt3.gmail-smtp-in.l.google.com.
gmail.com	mail exchanger = 40 alt4.gmail-smtp-in.l.google.com.
gmail.com	mail exchanger = 20 alt2.gmail-smtp-in.l.google.com.

Authoritative answers can be found from:
</pre>
$ <b>nslookup -type=mx</b> <em>foreverfamilyfoundation.org</em>

<pre>
Server:		208.67.220.220
Address:	208.67.220.220#53

Non-authoritative answer:
foreverfamilyfoundation.org	mail exchanger = 1 aspmx.l.google.com.
foreverfamilyfoundation.org	mail exchanger = 10 aspmx2.googlemail.com.
foreverfamilyfoundation.org	mail exchanger = 10 aspmx3.googlemail.com.
foreverfamilyfoundation.org	mail exchanger = 5 alt1.aspmx.l.google.com.
foreverfamilyfoundation.org	mail exchanger = 5 alt2.aspmx.l.google.com.

Authoritative answers can be found from:
</pre>
