# Devtools and You

## What are devtools? Why should I use them?

Chrome or Firefox Developer Tools will be a crucial tool for you to be able to access error messages, see if files are being loaded, and see how CSS styles are being applied to your web page. Part of being a good developer is knowing how and where to find error messages which will make us more likely to be able to solve a problem. No one likes bugs in their code, but error messages exist to give us a little hint about what went wrong. For that reason - let's think of them as helpers!

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

So, how might we locate and fix a CSS error? Let's pretend that we're Google developers for a second, and we've been told say, that the `font-size` is wrong. Perhaps the `font-size` should be `16px`, but in the above screenshot, we can see that it's actually only displaying as `13px`. We need to determine where exactly that `13px` is coming from, at which point, it should be easy enough to go make a change. We can click on the style in question to see a little more detail, including the source file and location (line number) of that style.

![](https://res.cloudinary.com/briezh/image/upload/c_scale,w_717/v1583947563/Screen_Shot_2020-03-11_at_10.25.37_AM_ive3qu.png)

So, now that we know the offending CSS is located in the `local-ntp.css` file on line 65, we can go locate that file and make a change!

## Console Tab

TODO

## Network Tab

On this tab, you can see which files loaded and which didn't. This tab isn't automatically populated like the others, so you'll need to do a refresh in order for it to be updated.

Once you reload the page, you should see something like this:

![](https://res.cloudinary.com/briezh/image/upload/c_scale,h_457/v1583948683/Screen_Shot_2020-03-11_at_10.44.08_AM_lmxa0d.png)
### Finding JavaScript Error Messages

TODO
