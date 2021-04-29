# The Program for Today

## CSS units

[w3schools](https://www.w3schools.com/cssref/css_units.asp)
[MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units)


- [ ] `px` and `%`
- [ ] `em` vs [`rem`](https://www.sitepoint.com/understanding-and-using-rem-units-in-css/)
- [ ] `vh` and `vw`
- [ ] [font-size](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size)
- [ ] [use cases for the different units](https://kyleschaeffer.com/css-font-size-em-vs-px-vs-pt-vs-percent#:~:text=%E2%80%9CEms%E2%80%9D%20(em)%3A%20The,5em%20would%20equal%206pt%2C%20etc.)

## Debugging with dev tools

- [ ] Debugging our CSS
- [ ] Quick intro to the DOM tree
- [ ] Modifying values
- [ ] https://developers.google.com/web/tools/chrome-devtools/css https://developers.google.com/web/tools/chrome-devtools/css/reference

## Using Images

- [ ] Introducing the [`<img>` tag](https://www.w3schools.com/html/html_images.asp)
- [ ] Importance of the `alt` attribute
- [ ] Absolute and Relative links
- [x] Framing our image with `border`
- [ ] Controlling corners with `border-radius`
- [ ] `width` and [`object-fit` property](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit) to control the aspect-ratio
- [ ] Image link by wrapping `<img>` with `<a>`
- [ ] using float (strictly with image and text)
- [ ] Quick intro to Gimp for image manipulation
  https://www.gimp.org/


# Repositories

* [CSS Units](https://github.com/DCIForks/float-image)
* [Using `em`](https://github.com/DCIForks/css-em)
* [Percent](https://github.com/DCIForks/percent)
---
* [Image Basics](https://github.com/DCIForks/image-basics)
* [Float Image](https://github.com/DCIForks/float-image)

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
