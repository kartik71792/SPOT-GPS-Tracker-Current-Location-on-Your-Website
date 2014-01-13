If you subscribe to the Track Progress service with SPOT, you can tell the GPS device to send your location to SPOT via satellite every 10 minutes, and then export those tracks at a later time.

They even have an API from which you can fetch JSON with all your current tracks! The unfortunate part, and the reason for this script, is that they only keep 30 days of GPS coordinates.

It’s not a problem if you export your data to Spot Adventures and create an “adventure” — that will live forever. But if you wish to present “my current location” on your personal web page, for example, you’re out of luck. It will only work as long as you’ve used the track progress functionality within the last 30 days.

I guess you need to cache the last used location yourself.

spotparse.pl
------------
This was the first attempt. It's ugly, and don't use it.
You probably want to have this script write out straight HTML rather than the javascript gunk I did (which is a hack because including iframes in the joomla version I use is broken). 

spotparse.py
------------
New hotness. Works very well.
Run this from cron every 15 minutes, and you’ll always have your last checked-in GPS coordinates! And a .json (and .xml) file that matches what SPOT has for you (they get overwritten each time, as long as the API didn't return an error).


