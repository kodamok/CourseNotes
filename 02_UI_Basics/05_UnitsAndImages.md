# The Program for Today

## [CSS units](https://dciforks.github.io/css-units/)

[w3schools](https://www.w3schools.com/cssref/css_units.asp)
[MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units)


- [x] `px` and `%` ([demo of %](https://dciforks.github.io/percent/))
- [x] `em` vs [`rem`](https://www.sitepoint.com/understanding-and-using-rem-units-in-css/)
- [x] `vh` and `vw`
- [x] [font-size](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size) ([demo](https://dciforks.github.io/css-em/))
- [ ] [use cases for the different units](https://kyleschaeffer.com/css-font-size-em-vs-px-vs-pt-vs-percent#:~:text=%E2%80%9CEms%E2%80%9D%20(em)%3A%20The,5em%20would%20equal%206pt%2C%20etc.)

## Debugging with dev tools

- [ ] Debugging our CSS
- [ ] Quick intro to the DOM tree
- [x] Modifying values
- [ ] https://developers.google.com/web/tools/chrome-devtools/css https://developers.google.com/web/tools/chrome-devtools/css/reference

## Using Images

- [x] Introducing the [`<img>` tag](https://www.w3schools.com/html/html_images.asp)
- [x] Importance of the `alt` attribute
- [x] Absolute and Relative links
- [x] Framing our image with `border`
- [x] Controlling corners with `border-radius`
- [ ] [`width`](https://www.smashingmagazine.com/2020/03/setting-height-width-images-important-again/) and [`object-fit` property](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit) to control the aspect-ratio
- [x] Image link by wrapping `<img>` with `<a>`
- [x] using float (strictly with image and text)
- [ ] Quick intro to Gimp for image manipulation
  https://www.gimp.org/


# Repositories

* [CSS Units](https://dciforks.github.io/css-units/) ([repo](https://github.com/DCIForks/css-units/))
* [Using `em`](https://dciforks.github.io/css-em/) ([repo](https://github.com/DCIForks/css-em))
* [Percent](https://dciforks.github.io/percent/) ([repo](https://github.com/DCIForks/percent))
---
* [Image Basics](https://dciforks.github.io/image-basics/) ([repo](https://github.com/DCIForks/image-basics))
* [Float Image](https://dciforks.github.io/float-image/) ([repo](https://github.com/DCIForks/float-image))
* [Side-by-side `div`s with `float`](https://dciforks.github.io/side-by-side/) ([repo](https://github.com/DCIForks/side-by-side))
* [Side-by-side `div`s with `inline-block`](https://dciforks.github.io/inline-block/) ([repo](https://github.com/DCIForks/inline-block))
Q
# Assignment
[Image Viewer Repository](https://classroom.github.com/a/ZbcBUSVS)

* Create a div with id "viewport"
* Inside it, create a div with the id "wrapper"
* Inside the `wrapper` div, add all the images from the `img` folder
* Add an `alt` attribute for each image
* In the `styles.css` file
  * Create a rule for the `#viewport` div, so that it shows its own scrollbar
  * Create a rule for the `#wrapper` div so that it is wide enough for all 9 images
  * Set a height for the `#wrapper` div, and a background color
  * Create a rule for the images, so that they scale to fit the height of the`#wrapper` div
  * Create a space between each image
  * Ensure that there is not a space after the last image

## Bonus

* Checkout the `final` branch and take a look at the `styles2.css` file. This uses CSS variables, so that you can tweak all the settings in one place.
