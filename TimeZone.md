[Brilliant Blog On This](http://danilenko.org/2012/7/6/rails_timezones/)

http://api.rubyonrails.org/classes/ActiveSupport/TimeZone.html

Do not use system time since servers could be anywhere

<pre>
<b>Time.zone.now</b>

Time.now.in_time_zone
DateTime.now.in_time_zone
</pre>

####Show All Different Time Zones
<pre>
<b>rake time:zones:all</b>
</pre>
