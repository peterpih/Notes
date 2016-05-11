[Brilliant Blog On this](http://danilenko.org/2012/7/6/rails_timezones/)

Do not use system time since servers could be anywhere

<pre>
<b>Time.zone.now</b>

Time.now.in_time_zone
DateTime.now.in_time_zone


</pre>
