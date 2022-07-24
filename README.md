jquery.hammer.js
==============

This jQuery plugin is just a small wrapper around the `Hammer()` class.
It also extends the `Manager.emit` method by triggering jQuery events.

Can be used with
````js
require('jquery-hammerjs');
````
Or
````js
import 'jquery-hammerjs';
````
And the Hammerjs library will be included automatically, you don't have to
manually import or require it in your code.
````js
$(element).hammer(options).bind("pan", myPanHandler);
````

The Hammer instance is stored at `$element.data("hammer")`.

Example for setting swipe options on an element
````js
$('#container').hammer()
	.data('hammer')
	.get('swipe')
	.set({
		direction: Hammer.DIRECTION_ALL,
		threshold: 200,
		velocity: 0.1
	});

$('#container').hammer()
	.on("swipedown", function (ev) {
		modalShow('#menu', '.settingsModal');
	})
	.on("swipeleft", function (ev) {
		loadKeys(layoutNames[layoutNext]);
	})
	.on("swiperight", function (ev) {
		loadKeys(layoutNames[layoutPrev]);
	});
````
