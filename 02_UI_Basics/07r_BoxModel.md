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

**Text, links and images all behave slightly differently**

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
