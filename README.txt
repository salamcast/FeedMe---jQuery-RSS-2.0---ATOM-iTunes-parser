@author Karl Holz <newaeon|a|mac|d|com>
@package feedMe

//#############################################################################################
 FeedMe - jQuery RSS 2.0 + ATOM/iTunes parser
 
feedMe is a basic RSS feed and Podcast parser with XML namespace support for your Javascript and jQuery web apps.
 
//#############################################################################################
 Reference for RSS 2.0
 
 http://www.rssboard.org/rss-2-0

 Reference for iTunes Podcasting 

 http://www.apple.com/itunes/podcasts/specs.html
 http://www.podcast411.com/howto_1.html
 
 Reference for ATOM
 
 http://tools.ietf.org/html/rfc4287
 


This class returns
- a normal Javascript object
- a JSON string
- a Base64 encoded JSON string

example:

$('link[type="application/rss+xml"]').each(function() {
 var link = $(this).attr('href');
 // for base64 encoded JSON string: feedMe(link,'base');
 // for JSON encoded string:        feedMe(link,'json');
 // for normal javascript object you only need an RSS url link
 var f = feedMe(link);
 /**  Do something with the object  */
});


The test.html has an example of printing the returned javascript object with prettyprint
- http://james.padolsey.com/javascript/prettyprint-for-javascript/

The base64 string can be decoded with the class in base64.js

- Base64.decode(<Base64 string>);

The JSON string can be turned into a javascript object with JSON.js

- JSON.parse(<JSON string>);