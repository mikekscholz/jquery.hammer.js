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

