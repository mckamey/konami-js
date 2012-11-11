[The Konami Code for JavaScript](http://github.com/mckamey/konami-js/)
==============================

Konami-js is a tiny JavaScript implementation of the [Konami Code](http://en.wikipedia.org/wiki/Konami_Code), but also monitors *any* arbitrary keyboard sequence.

&#8593; &#8593; &#8595; &#8595; &#8592; &#8594; &#8592; &#8594; B A

Konami.code(&hellip;) creates an event handler which you attach to any element you would like:

	$(document).on('keyup',
	
		Konami.code(function() {
			alert('Congratulations, 30 lives!');
		})
	
	);

Alternatively, you can specify [a different keyCode sequence](http://en.wikipedia.org/wiki/Alphabet_song) to monitor with Konami.sequence(&hellip;):

	$(document).on('keyup',
	
		Konami.sequence(
			65, 66, 67, 68, 69, 70, 71,
			72, 73, 74, 75, 76, 77, 78, 79, 80,
			81, 82, 83,
			84, 85, 86,
			87, 88, 89, 90,
			function() {
				alert('Now I know my ABCs.\r'+
					   Next time won't you sing with me?');
			})
	
	);


[Try it out!](http://mckamey.github.com/konami-js/)
-----------

Copyright &copy; 2012, [Stephen M. McKamey](http://mck.me)
