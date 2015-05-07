
*******************************************
Google Maps: fast routes from a fixed point
*******************************************

Whenever I want to find the route to somewhere, say to Cherry Red's in Birmingham, I go to the address bar in Chrome and type ::

	to Cherry Red's <enter>

This brings up the route from my university:

	https://www.google.co.uk/maps/search/from:+university+of+birmingham+to:+Cherry%20Red's

To get this, open `chrome://settings/searchEngines <chrome://settings/searchEngines>`_ (you'll have to copy-paste that link), and fill in a new entry:

	:New engine: *Route to*
	:Keyword: ``to``
	:URL: ``https://www.google.co.uk/maps/search/from:+university+of+birmingham+to:+%s``

To use your own starting place, replace ``university+of+birmingham`` with something of your choice without any special characters; replace spaces by plusses.


.. image:: ../resources/rc3YLWl.gif
	:width: 400px