# js-popunder

**js-popunder** is a pure javascript function that creates pop-under windows

UPDATE (May 27, 2013): Now supports Chrome 27!

Usage
-----
Popunders are popup windows that open behind the currently active browser window.
The latest version of this script opens popunders on document.onclick.

Options
-------
- "sUrl": The url to open
- "sConfig": paramaters object (optional)

Available Parameters
-------
- "name": The name of the popunder window (defaults to a random number)
- "width": The width of the popunder (defaults to opener's width)
- "height": The height of the popunder (defaults to opener's height)
- "top": Popunder position from top (defaults to 0)
- "left": Popunder position from left (defaults to 0)
- "wait": Interval/wait time between popunders (in seconds, defaults to 3600 = 1 hour)
- "cap": Max daily popunders per domain (capping, defaults to 2)
- "cookie": Cookie name to be used (defaults to "__.popunder")

Compatibility
-------
- Google Chrome 10-27
- Mozilla Firefox 3-21
- Microsoft Internet Explorer 6-10
- Apple Safari 6

Known Issues
-------
- Safari also opens an empty tab

Examples
-------
This example opens google.com in full screen using default settings:

	jsPopunder('http://www.google.com');


This example opens google.com in a 500x500 window

	jsPopunder('http://www.google.com', {
		name: 'googleWindow', 
		width: 500, 
		height: 500
	});

Full example:

	jsPopunder('http://www.google.com', {
		name: 'googleWindow', 
		width: 1025, 
		height: 640, 
		top: 0, 
		left: 0, 
		wait: 1800, 
		cap: 10, 
		cookie: 'googPop'
	});

Enjoy!