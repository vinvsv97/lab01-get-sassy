# Let's Get SASS-y

Writing CSS kinda sucks. Many times when writing it, you copy paste code a lot, and there isn't a great way to throw stuff into variables to be reused. An awesome library called [SASS](http://sass-lang.com/) fixes all of it!

## Installing

1. For this lab, we will be using macOS to install SASS
  > If you are using a windows machine, just use a lab machine for this lab since we don't want to wrestle with `gem` and Ruby installations during the lab
2. Follow the [installation instructions ](http://sass-lang.com/install)
3. Confirm that you have `sass` installed with `sass -v`
3. Make sure that you have [`live-server`](https://www.npmjs.com/package/live-server)

## What and Why?

Like said above, writing CSS sucks since its _*way*_ too tedious for its own good. Being able to have variables, import variables, mixins, and whatnot is super helpful. Sass also supports nesting your SCSS code so that its easier to read & encapsulate what and where the styles are being applied.

## Getting Started

1. Begin the live server using `live-server --port=4000`
2. Begin the sass watcher using `sass --watch sass:css`
2. Open the `index.html` and `sass/styles.css` files!
3. Make a change to `h1` to give it the color of `red` to confirm that the styles are compiling & that the live-server is getting the changes.

## Part 1: Variables and Math

1. Using a nesting structure, select all the `ul` and `ol` elements within the `.container` class and give them the color `red`.
2. Now, at the top of the file, declare a variable `$red`, and assign it the color `red`.
3. Now, go back to where you styled the `ul` adn `ol` elements. Change that `red` to `$red`.
4. Now, change the value of the `$red` variable to `blue`, and see the change take place! :eyes:

Continue making variables & doing nesting selection with these steps:

1. Make the `ul` font family be `sans-serif` and the `ol` font family be `monospace`.
2. Make the background color of paragraphs in the the first container have blue color. In the second container, have those paragraphs be the color orange.
3. Make the width of `container` elements have a width of 100% minus 40 pixels.
> :bulb: Use the `calc` helper! (google it :wink:)
4. Set the background color of the containers to be pink.

## Getting Sassier

Let's get a little more advanced!

Have quite a few color variables at the top that, if you had other SCSS files, you'd want to use there? Make a new `sass/colors.scss` that defines those color variables and import them into your `styles.scss`!

Check out how to use [`mixins`](http://sass-lang.com/guide) and utilize one called `sideMargin` to set both the left and right margins of the container class. Since the class lacks 40 pixels from the total width, try setting containers to *auto* -matically center in the page. Try playing with the container width and different values and different values passed into `sideMargin`.

## Challenge

Finish early? Figure out how to compile all of your compiled CSS code into a single `styles.css` file.
