[Brilliant Blog On This](http://danilenko.org/2012/7/6/rails_timezones/)

http://api.rubyonrails.org/classes/ActiveSupport/TimeZone.html

[How to change how ActiveAdmin displays time](http://stackoverflow.com/questions/17845646/how-to-change-how-activeadmin-displays-time-every-time)

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
