# DOM Events

## What is the DOM?

When the browser loads a webpage, it takes all the front-facing HTML code (information that's intended for display on the page), and creates JavaScript objects that represent those blocks of code.

## Events

DOM Events allow us to trigger actions based on "events". An event can be anything from a click, to a form submission, to a keystroke, or maybe even the action of scrolling! [If you want to know ALL the events...](https://developer.mozilla.org/en-US/docs/Web/Events)

### Event Listeners

An event listener is a function that runs whenever an event is satisfied. For example, you may have an "On click" event that starts playing DMX's "Ruff Ryders Anthem" whenever the user clicks on a picture of a dog!

That might look something like this:

```
var dog = document.getElementById('dogPic')
var music = document.getElementById('ruffRyderAnthem')

function ruff () {
  music.play()
}

dog.addEventListener('click', ruff)
```

The important bit here is that last line, so let's break it down a bit:

First, "dog". We know that's going to be referencing the dog picture, because we handled that way up at the top.

Then we tell it to look for an event: in this case, a 'click'! But this could be almost anything.

The last part of the recipe is our function. In this case, it's "ruff". We wrote that just above, we're just telling it WHEN to execute. Remember, functions don't execute unless called!
