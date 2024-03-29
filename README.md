# Stitching Together the Three Pillars

## Learning Goals

- Identify the three essential pillars of front-end web programming
- Cause a change to given code so that DOM updating effect is seen
- Cause a change to given code so that server-side behavior is stubbed in
- Cause a change to given code so that event listening has an effect

## Introduction

Remember when we started this exploration of the "Simple Liker" application?
You might not have been sure that you would make it to this point, but you
have. Right now you should have the information needed to create a basic web
application!

Your goal is to implement "Simple Liker," from scratch.

You might be tempted to look back at previous code, but don't. Use your
knowledge and documentation from the internet (if needed), to build the
application.


Elements have a property `.classList` that will let you `.add()` and `.remove()`
class names. By just adding and removing class names your code has a clearer
separation of concerns:

* HTML defines the structure of the website (not appearance or functionality)
* JavaScript defines functionality of the website (not structure or styling)
* CSS defines the visualization and style of the website (not structure or functionality)

Keep all your styling rules entirely in `style.css`. Do not manipulate any `.style` properties.

* [MDN classList Documentation](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList)

Here's the specification:

* Add the `.hidden` class to the error modal in the HTML so it
  does not appear when the page first loads
* When a user clicks on an empty heart ("Recognizing events")
  * Invoke `mimicServerCall` to simulate making a server request
    * `mimicServerCall` randomly fails to simulate faulty network conditions
    * When the server returns a failure status
      * Respond to the error using a `.catch(() => {})` block after your
        `.then(() => {})` block.
      * Display the error modal by removing the `.hidden` class
      * Display the server error message in the modal
      * Use `setTimeout` to hide the modal after 5 seconds (add the `.hidden` class)
    * When the server returns a success status
      * Change the heart to a full heart
      * Add the `.activated-heart` class to make the heart appear red
* When a user clicks on a full heart
  * Change the heart back to an empty heart
  * Remove the `.activated-heart` class

Only manipulate the DOM once the server requests respond. Do not make the
heart full until you're inside a successful `.then` block.

## Conclusion
That's it! Congratulations. You're now a real-deal web programmer. You can use
HTML, CSS, and JavaScript to create living, breathing applications. Every web
application you see or have seen is built on these three pillars, which you're
now skilled with! Give yourself a well-deserved pat on the back!

[fetch]: https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch
