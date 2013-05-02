http-status-echoer
==================

.htaccess file to return error to user based on url.

HTTP status codes copied from http://www.iana.org/assignments/http-status-codes/http-status-codes.xml with minor modifications
* Added 402 - I am a teapot
* Removed a couple that my Apache at url below did not like

example: stepanyakovlev.net/error/402

License: Feel free to do anything you want. What was name for that kind of license?

Generate your own!
==================
* copy paste table from iana url above
* cat codes | grep -v "Unassigned" | grep -v "-"  | awk '{print "RewriteRule ^(" $1 "$ - [R=" $1 ",L]"}' 
