# Devtools and You

## What are devtools? Why should I use them?

TODO

## How can I get to my devtools in the browser?

There are a few different ways to get to the devtools

* Keyboard shortcuts: `⌘ + OPTION + I` (Elements Tab) or `⌘ + OPTION + J` (Console Tab)
* Right click (CTRL + Click) and select "Inspect"
* From Chrome's menu located at the top right, select More Tools -> Developer Tools

## Elements Tab

The elements tab allows you to look at the DOM elements. This allows you to see all the HTML and you can click on any element to see the CSS styles. Take a look at the screenshot below of Google's homepage. Notice that the logo is highlighted both on the screen and in the elements tab. Below that, you can see the CSS styles being applied to the logo (`opacity: 1`) and the location it comes from (`doodles.css`).

![](https://res.cloudinary.com/briezh/image/upload/c_scale,w_780/v1583946640/Screen_Shot_2020-03-11_at_10.09.57_AM_oiagou.png)

### Finding CSS Errors

Continuing on with the Google logo on the Google homepage, let's dig into the CSS. You may have noticed a "Computed" tab next to the Styles tab. Here you can see the box model (that's the margin, padding, border, and content) and a list of all the styles being applied to the element. Let's take a look:

![](https://res.cloudinary.com/briezh/image/upload/c_scale,h_585/v1583947304/Screen_Shot_2020-03-11_at_10.21.09_AM_hrm9kv.png)

So, how might we locate and fix a CSS error? Let's pretend that we're Google developers for a second, and we've been told say, that the `font-size` is wrong. Perhaps the `font-size` should be `16px`, but in the above screenshot, we can see that it's actually only displaying as `13px`. We can click

![](https://res.cloudinary.com/briezh/image/upload/c_scale,w_717/v1583947563/Screen_Shot_2020-03-11_at_10.25.37_AM_ive3qu.png)

## Console Tab

TODO

### Finding JavaScript Error Messages

TODO
