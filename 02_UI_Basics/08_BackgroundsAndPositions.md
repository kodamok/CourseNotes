# Recap

## Which of the following are `block` elements, and which are `inline` elements, by default?
 - [ ] `<a>`
 - [ ] `<article>`
 - [ ] `<aside>`
 - [ ] `<div>`
 - [ ] `<figcaption>`
 - [ ] `<figure>`
 - [ ] `<footer>`
 - [ ] `<h1>-<h6>`
 - [ ] `<header>`
 - [ ] `<hr>`
 - [ ] `<img>`
 - [ ] `<li>`
 - [ ] `<main>`
 - [ ] `<nav>`
 - [ ] `<ol>`
 - [ ] `<p>`
 - [ ] `<section>`
 - [ ] `<span>`
 - [ ] `<ul>`

<div style="background-color:white;">
<p style="color:black;font-weight:bold;">Answer: <span style="color:white;font-weight:normal">&lt;a&gt;, &lt;img&gt; and &lt;span&gt; are inline by default</span></p>
</div>

[HTML Block and Inline Elements](https://www.w3schools.com/html/html_blocks.asp)


## Display differences

* `block`
  * 100% width of parent by default
  * box shrinks to fit height of content by default
  * width and height attributes respected
  * line break after element

* `inline`
  * box shrinks to fit content both horizontally and vertically
  * width and height are ignored <em style="color:darkred;">even ignoring <code> box-sizing: border-box</code></em>
  * top and bottom margin are ignored
  * top and bottom padding overflow
  * no line break after element

* `inline-block`
  * box shrinks to fit content both horizontally and vertically
  * width and height attributes are respected
  * top and bottom margin and padding are ignored
  * no line break after element

[Demo](https://dciforks.github.io/inline-margin/) ([repo](https://github.com/DCIForks/inline-margin/tree/main))


## CSS Selectors and Combinators

* element-type
* .class
* #id
* :pseudo-class
* parent descendant
* parent > immediate-child
* element ~ younger-sibling

### Element types
(see above)

### `pseudo-class`es
* :hover
* :active
* :visited
* :last-child
* :target

[Further reading](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

## Exercises
* Stairway to Heaven
* Build a blog

---
---

# Backgrounds

## Images

- [ ] `background-image` is for decoration not content
- [ ] `background-size`
   * contain
   * cover
   * %
   * units
   * width (and height)
   * auto
- [ ] `background-repeat`
   * repeat
   * no-repeat
   * space
   * round
   * repeat-x
   * repeat-y
- [ ] Setting multiple attributes with `background` shortcut
   * `background: bg-color bg-image position/bg-size bg-repeat bg-origin bg-clip bg-attachment`
   *  `background:initial;`
   * `background:inherit;`


### Attributes:
- [ ] background-color ([w3schools](https://www.w3schools.com/css/css_background.asp), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color))
- [ ] background-image ([w3schools](https://www.w3schools.com/css/css_background_image.asp), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/background-image))
- [ ] background-position ([w3schools](https://www.w3schools.com/cssref/pr_background-position.asp), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position
))
- [ ] background-size ([w3schools](https://www.w3schools.com/cssref/css3_pr_background-size.asp), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/background-size))
- [ ] background-repeat ([w3schools](https://www.w3schools.com/css/css_background_repeat.asp), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/background-repeat))
- [ ] background-origin ([w3schools](https://www.w3schools.com/cssref/css3_pr_background-origin.asp), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/background-origin))
- [ ] background-clip ([w3schools](), [MDN]([clip](https://developer.mozilla.org/en-US/docs/Web/CSS/background-clip)))
- [ ] background-attachment ([w3schools](https://www.w3schools.com/css/css_background_attachment.asp), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/background-attachment))
<br><br>
- [ ] background-blend-mode ([w3schools](https://www.w3schools.com/cssref/pr_background-blend-mode.asp), [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/background-blend-mode))

## Multiple images
* Top image listed first, bottom image last
* Separate other attributes with commas

## Gradients
- [ ] [Linear](https://developer.mozilla.org/en-US/docs/Web/CSS/linear-gradient()) and [radial](https://developer.mozilla.org/en-US/docs/Web/CSS/radial-gradient()) gradients
* [Gradient Maker](https://cssgradient.io/)

---

# [Exercise](https://classroom.github.com/a/pxy7sGPt)
1. Create a new folder for your project
2. Add subfolders called `css` and  `img`
3. Create an `index.html` page with some (dummy) text in a `<main>` element
4. Find a [seamless pattern](https://pixabay.com/images/search/seamless%20pattern/) that you like, and download it into your `img/` folder
5. Use the repeating pattern to fill the background of your `<main>` element
6. Find an image with a transparent background (PNG, WEBP) and place it strategically in your background
7. Choose whether to make it scroll or fixed

# Install GIMP

```bash
sudo apt update
sudo apt install snapd
sudo snap install gimp
```


# Shadows
- [ ] Box shadow
- [ ] Text shadow


# Position
- [ ] Understanding positioning - static, relative, absolute, fixed, sticky
- [ ] Position offsets - top, bottom, right, left
- [ ] Layering boxes with z-index
