# DAY 1

## *Intro*
- [ ] *History of HTML*
- [ ] *HTML document and the browser*
- [ ] *Defining the user*

## Code Editor

- [x] Setting up VSCode
- [x] File directories
- [x] Extensions (live server, prettier)
- [ ] Keyboard shortcuts
- [ ] [Introducing emmet](https://emmet.io/)

## Examining the boilerplate

- [x] `<!DOCTYPE html>`
- [x] meta tags
- [x] Character set
- [x] `<html>` is the root element
- [x] `<head>`, `<body>`, `<title>`

## Up and Running

- [x] Anatomy of an element (opening tag, content, closing tag)
- [x] `<h1>` - [ ] `<h6>`, `<p>`
- [x] Running our file locally and globally
- [x] Commenting with `<!-- [comment] -->`
- [x] The importance of clean, indented code

---

# DAY 2

## Introducing Style

- [ ] *History of Cascading Style Sheets*
- [x] Writing CSS inline, internally and externally
- [x] Anatomy of a declaration (selector, declaration, property, value)
- [x] The `<link>` tag
- [x] Commenting with `\*[comment]*\` (Ctrl-/ or Strg-Shift-7)

## Separation of Concerns - content and presentation

- [x] [HTML is for content, CSS is for presentation](https://en.wikipedia.org/wiki/Separation_of_content_and_presentation)

## Lists: Indentation and Family

- [x] `<ol>`, `<ul>`, `<li>`
- [ ] [Changing presentation with `list-style-type`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-type) ([Try It Yourself](https://www.w3schools.com/cssref/tryit.asp?filename=trycss_list-style-type_ex))
- [ ] [Descendent combinator](https://developer.mozilla.org/en-US/docs/Web/CSS/Descendant_combinator) ([More combinators](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Combinators))
- [ ] [Understanding nesting, parent - child relationship](../../main/02_UI_Basics/NestingTags.md)

## Classes and IDs

- [x] Targeting a unique element with the `id` attribute
- [x] Targeting a group of elements with the `class` attribute

---

# DAY 3

## Hyperlinks

- [x] Anchoring with `<a>`
- [x] linking pages
- [x] ID linking
- [x] web links
- [ ] [Sending emails with `mailto:`](https://www.w3schools.com/tags/tag_address.asp)

## [Color in CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)

- [ ] [Using keywords, RGB, RGBA, hex](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value#syntax_2)
- [ ] [Transparency](https://www.w3schools.com/css/css_image_transparency.asp) and opacity
- [x] Combining multiple selectors with `,`
- [ ] [HSL, HSLA for self study](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value#hsl_colors)

## Pseudo Classes

- [ ] [Introducing state pseudo class](https://www.w3schools.com/css/css_pseudo_classes.asp) ([in depth presentation](https://www.smashingmagazine.com/2016/05/an-ultimate-guide-to-css-pseudo-classes-and-pseudo-elements/))
- [x] Coloring links with `:hover`, `:active` and `:visited`
- [ ] The importance of state in [UI/UX](https://givegoodux.com/use-5-principles-interaction-design-supercharge-ui-part-1-5/) - feedback and predictability
- [x] Using MDN to locate [additional selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors), [combinators](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Combinators), [elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) and rules ([Overview of CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_is_structured))

---
# DAY 4

## CSS units

- [x] `px` and `%`
- [ ] [`em` vs `rem`](https://www.digitalocean.com/community/tutorials/css-rem-vs-em-units)
- [ ] [`vh` and `vw`](https://www.hongkiat.com/blog/css-viewport-units-vw-vh-wmin-vmax/)
- [ ] [use cases for the different units](https://www.digitalocean.com/community/tutorials/css-css-units-explained) ([Video tutorial](https://www.youtube.com/watch?v=fi81bovqxXI))

## Debugging with dev tools

- [x] Debugging our CSS
- [ ] [Quick intro to the DOM tree](https://developer.chrome.com/docs/devtools/dom/)
- [x] Modifying values
- [ ] [View and Change CSS](https://developers.google.com/web/tools/chrome-devtools/css)
- [ ] [CSS features reference](https://developers.google.com/web/tools/chrome-devtools/css/reference)

---
# DAY 5

## Using Images

- [Repo to demonstrate different features of the `<img>` tag](https://github.com/DCIForks/image-basics) and [Preview](https://dciforks.github.io/image-basics/)
- [x] Introducing the `<img>` tag
- [x] Importance of the `alt` attribute
- [ ] [Absolute and Relative links](https://www.webstix.com/knowledgebase/general/relative-links-vs-absolute-links/)
- [x] Framing our image with `border`
- [x] Controlling corners with `border-radius`
- [ ] [`width` and `object-fit` to control the aspect-ratio](https://www.digitalocean.com/community/tutorials/css-cropping-images-object-fit)
- [ ] [Image link by wrapping `<img>` with `<a>`](https://www.tutorialspoint.com/How-to-use-an-image-as-a-link-in-HTML)
- [ ] [using float (strictly with image and text)](https://css-tricks.com/all-about-floats/)
* [Repo to demonstrate float](https://github.com/DCIForks/float-image) and [Preview](https://dciforks.github.io/float-image/)
- [ ] Quick intro to [Gimp](https://www.gimp.org/) for image manipulation


---
# DAY 6

## [*The importance of accessibility*](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/HTML)

- [ ] [*provide equal access and equal opportunity to people with disabilities*](https://www.levelaccess.com/accessibility-regulations/germany/)
- [ ] *Always use the [`title` attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/title) and the [`alt` attribute](https://moz.com/learn/seo/alt-text) for images ([alternatives to title](https://inclusive-components.design/tooltips-toggletips/))*
- [ ] [*What`s a screen reader?](https://www.smashingmagazine.com/2018/12/voiceover-screen-reader-web-apps/) ([Enabling Orca on Ubuntu](https://help.ubuntu.com/stable/ubuntu-help/a11y-screen-reader.html.en))*
- [ ] [*using the `aria-label` attribute*](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/WAI-ARIA_basics)
- [ ] *[Google Lighthouse](https://developers.google.com/web/tools/lighthouse)*
- [ ] [*What is Web Accessibility? - slide presentation*](What_is_web+accessibility.pdf")

## Understanding the cascade, specificity and inheritance

- [ ] [Conflicting rules](https://medium.com/web-for-you/css-conflict-resolution-rules-explained-9ab90de18aef)
- [ ] [!important and why not to use it](https://css-tricks.com/when-using-important-is-the-right-choice/)
- [ ] Specificity - [selecting by element, class, ID](https://www.w3schools.com/css/css_selectors.asp)
- [ ] [Inline always wins](https://css-tricks.com/specifics-on-css-specificity/)
- [ ] [Non-inheriting properties](https://dev.to/muyunyun/inherited-and-non-inherited-in-css-mi4) - `width` and `border`
- [x] Using dev tools to inspect the cascade
- [ ] [Controlling inheritance - `inherit`, `initial`, `unset`](https://www.digitalocean.com/community/tutorials/css-inherit-initial-unset) ([in depth](https://webdesign.tutsplus.com/tutorials/understanding-css-inheritance-inherit-initial-unset-and-revert-keywords--cms-34233))
- [ ] [Source order](https://wattenberger.com/blog/css-cascade)
- [x] [Specificity calculator](https://specificity.keegan.st/)

---
# DAY 7

## Introduction - Everything is a Box

- [x] Taking a look with dev tools
- [ ] Demonstration with `border: 1px solid red; !important` to show
  boxes on webpage, eg. google.com

## Containing Content
- [x] The default box: -the `<main>` tag](https://www.htmlquick.com/reference/tags/main.html)
- [ ] Shrink Wrapping our content:
  putting everything in a [`<main class="container">` element](https://www.pair.com/support/kb/understanding-bootstraps-grid-system/)
- [ ] [Changing width and centering: css `width` and `margin: auto`](https://css-tricks.com/almanac/properties/m/margin/#auto-and-centering)
- [ ] Limiting the [height](https://developer.mozilla.org/en-US/docs/Web/CSS/height): USE css [`height`](https://css-tricks.com/almanac/properties/h/height/) ONLY in specific situations, when the default `auto` value is not the best solution.
- [ ] Full height content with [the `vh` unit](https://wpshout.com/quick-guides/using-css3-vh-viewport-height-unit/)
- [ ] [The `vh` unit on mobile Safari and Chrome](https://medium.com/rbi-tech/safaris-100vh-problem-3412e6f13716)
- [ ] Control your flow: [the `overflow` property](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow)

## Block Level Semantics

- [x] A [block-level element](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements) always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can) ([w3schools](https://www.w3schools.com/css/css_display_visibility.asp))
- [ ] [`<section>`, `<article>` and `<aside>`](https://www.w3schools.com/html/html5_semantic_elements.asp)
- [ ] Top and bottom of segments - `<header>` and `<footer>`
- [x] `<div>` - a generic box for styling
- [x] Self study - using MDN to find more block elements
- [ ] [Block vs inline](https://stackoverflow.com/a/9189873)

---
# DAY 8

## Modeling Boxes

- [ ] [Setting box width with `box-sizing: border-box;`](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing) ([Try It Yourself](https://www.w3schools.com/css/tryit.asp?filename=trycss3_box-sizing_old))
- [x] Spacing out our boxes - `margin` is for outside, `padding` for inside
- [ ] Reset me softly - `* {margin: 0; padding:0; box-sizing: border-box;}`
- [ ] [The universal selector *](https://www.geeksforgeeks.org/what-is-the-use-of-asterisk-selector-in-css/)
- [ ] [Margins, paddings, width and height on inline elements](https://dciforks.github.io/inline-margin/)
- [ ] Changing boxes with css `display` and `inline`, `block` and `inline-block`

---
# DAY 9

## Background Images

- [x] [`background-image`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-image) is for decoration not content
- [ ] [`background-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-size), [`background-repeat`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-repeat), `[no-repeat`](https://www.w3schools.com/css/tryit.asp?filename=trycss_background-image_norepeat)
- [ ] [Setting multiple attributes with `background` shortcut](https://developer.mozilla.org/en-US/docs/Web/CSS/background)
- [ ] [Linear](https://www.w3schools.com/css/css3_gradients.asp) and [radial](https://developer.mozilla.org/en-US/docs/Web/CSS/radial-gradient()) gradients ([Gradient Generator](https://cssgradient.io/))

## Positioning

- [ ] [Understanding positioning](https://developer.mozilla.org/en-US/docs/Web/CSS/position) - `static`, `relative`, `absolute`, `fixed`, `sticky`
- [ ] Position offsets - `top`, `bottom`, `right`, `left`
* [Demo of the different values for the `position` property](https://dciforks.github.io/css-position/) ([Repo](https://github.com/DCIForks/css-position))

## Layering
- [ ] [Stacking order of static and positioned elements](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/Stacking_without_z-index)
- [ ] [Layering boxes with `z-index`](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index)
- [ ] [How z-index is applied to child elements](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context)

---
## UI Basic - Basic Test

---
# DAY 10

## Intro to UI/UX

- [ ] What is the user?
- [ ] What is an interface?
- [ ] What is a user interface?
- [ ] Intro To UXD - slide deck

## Inline Text Semantics
- [ ] Conveying importance with `<strong>`
- [ ] Emphasizing words with `<em>`
- [ ] Generic inlines with `<span>`
- [ ] Self learning: Finding more inline elements on MDN

## Font Family
- [ ] Different faces for different meanings:
  when to use - [ ] serif, sans-serif, monspace and cursive
- [i] Pre Installed System fonts: css `font-family: <font-name>`
- [ ] Providing fallbacks: font stack values for `font-family`
- [ ] Getting more fonts: Google fonts and css `@import` directive

---
# DAY 11

## Font Sizing:
- [x] Setting text size with `font-size`
- [ ] Relative to parent: `em` sizing and nesting
- [ ] Relative to root: `rem` sizing and the `:root` selector
- [ ] Setting the base size:
  `:root { font-size: 62.5% }` and decimal `rem`s (1.2rem = 12px)

## Direction and Alignment
- [ ] Writing text in RTL languages with `direction: rtl;`
- [x] Aligning text with `text-align`
- [ ] Centring text: comparison between `center` and `justify`

## Stylish Text
- [ ] Thicker text with css `font-weight`, choosing font weights on google fonts
- [ ] Italics with css `font-style`
- [ ] Underline and line-through with css `text-decoration`
- [ ] Changing case with css `text-transform`
- [ ] Adding shadow and stroking text with css `text-shadow`
- [ ] Text-styling with `:before` and `:after` pseudo-elements

---
# DAY 12

## Icon Fonts
- [ ] Conveying meaning without text: fontawesome
- [ ] Adding fontawesome to our websites: choosing the correct CSS links
- [ ] Sizing icons with Fontawsome sizing utility classes
- [ ] Self-study: Alternatives to Fontawesome - flaticon, thenounproject.com

---
# DAY 13

## Designing With Colors
- [ ] Creating color palettes
- [ ] Primary and accent colors
- [ ] Importance of lightness and saturation
- [ ] Color temperature: cooling down with blue, warming up with yellow / orange
- [ ] Importance of color choice regarding accessibility concerns

## Let The Light In
- [ ] using `box-shadow` to emulate a light source
- [ ] inset elements create a `well` component
- [ ] shadows to convey elevation
- [ ] 2 part shadows - using multiple instances of `box-shadow`

## Basic Principles of UI Design
- [ ] structure, simplicity, visibility, feedback, tolerance, reuse
  https://en.wikipedia.org/wiki/Principles_of_user_interface_design

---
# DAY 14

## Organizing Data in Tables
- [ ] Tables are only for tabular data, never for layout
- [ ] `<table>` and `display: table`
- [ ] `<tr>` and `<td>`
- [ ] `<thead>`, `<th scope=[...]>`, `<tbody> and <tfoot>`
- [ ] Spanning rows and columns - `<td rowspan=""..."">`, `<td colspan=""..."">`
- [ ] `<caption>` (optional)
- [ ] The `scope` attribute for improved accessibility
-
## Styling Tables
- [ ] Overriding borders with css `border-collapse`
- [ ] Zebra stripes with pseudo child selectors: `:nth-child() { ... }`
- [ ] Easy layout with `table-layout: fixed` and `:nth-child() { ... }`
- [ ] Additional info with `<caption>`
- [ ] Specifying `<caption>` placement with `caption-side`

---
# DAY 15

## Forms and Dynamic Data
- [ ] Searching - `<form>`, `<input>`
- [ ] Sending forms to a URL - the `action` attribute
- [ ] Importance of names: `<input name=[...]>` attribute,
  `<label for=[...]>`
- [ ] URL structure & anatomy
- [ ] HTTP verbs - `GET`, `POST` and the `method` attribute
- [ ] `<form>`, `<fieldset>`, `<legend>`

## The Wonderful World of Inputs
- [ ] Text inputs: `type=""email""`, `type=""password""`, `type=""search""`
- [ ] Default text - the `placeholder` attribute
- [ ] `<checkbox>` - the `value` and `checked` attributes
- [ ] Many choices - `type=""radio""`, `<select>`, `<option>`
- [ ] `<textarea>`
- [ ] Set up example with formspree.io
- [ ] `<input type="file">` and using MDN to find more inputs

## Validated, Sanitized and Secured
- [ ] Concept of client side form validation
- [ ] HTML form controls - `required`, `minlength` & `maxlength`,
  `min` & `max`, `type`, `pattern` attributes
- [ ] `:valid` and `:invalid` pseudoclasses
- [ ] Controlled parameters with `<datalist>` and `<optgroup>`

---
# DAY 16

## Styling our Form
- [ ] Using `:focus` pseudoclass and `outline`
- [ ] `::placeholder` for styling `placeholder` text
- [ ] Styling with attribute selectors
- [ ] `disabled` and `readonly` attributes
- [ ] Mobile Form Design : A UX Perspective - slide presentation

## Styling our Form 2 - Use Case
- [ ] Creating a CSS only toggle switch

---
# DAY 17

## Mobile First
- [ ] A brief history of web pre and post the smartphone revolution
- [ ] Targeting our users - mobile is the future (and present)
  https://gs.statcounter.com/platform-market-share/desktop-mobile-tablet
- [ ] Ensuring proper scale -
  `<meta name=""viewport"" content=""width=device-width, initial-scale=1"">`
- [ ] Mobile-First Design - slide presentation

## Media Queries
- [ ] Anatomy of a media query: `@media [media-type] ([media features]) { ... }`
- [ ] Default media type: `screen` is optional
- [ ] Common features: `(min-width: <size>)`
- [ ] Breakpoints: The ""standard"" bootstrap breakpoint values

## Responsivity
- [ ] The `vw` unit: DON`T USE for text (overrides user zoom capabilities)
- [ ] Making the root text respond to screen width
- [ ] Overriding headings: bigger headings for bigger screens
- [ ] Responsive text size classes
- [ ] `rem` and `em` in regards to responsivity
  http://ami.responsivedesign.is/

---
# DAY 18

## Planning Our Layout
- [ ] Translating design to code
- [ ] Pen and paper
- [ ] Figma
- [ ] Wireframing for multiple breakpoints
- [ ] Screen layout vs User flows

## Flexbox on parent elements
- [ ] Flexible boxes: `display: flex`, flex child & flex parent concept
- [ ] Aligning and justifying: `justify-content` and `align-items`
- [ ] Direction and wrapping: `flex-direction` and `flex-wrap`
- [ ] Small shorthand: `flex-flow`

---
# DAY 19

## Flexbox on child elements
- [ ] Growing and shrinking: `flex-grow` and `flex-shrink`
- [ ] Base sizing: `flex-basis` and the `flex` shorthand
- [ ] Reordering children: `order` and `align-self`
- [ ] The perfect center:
  centering in fixed height parents with `display: flex` and `margin: auto`
- [ ] Responsivity - media queries + flexbox

---
# DAY 20

## Flexbox use cases
- [ ] Cards
- [ ] Media queries and Flexbox
- [ ] Simple page with Flexbox nav and cards

---
# DAY 21

## CSS Grid on parent elements
- [ ] Making our grid container: `.container { display: grid }`
- [ ] Grid columns: css `grid-template-columns` and `fr` unit
- [ ] Setting max and min sizes: css `minmax([min], [max])`
- [ ] Spacing columns and rows - `gap`

---
# DAY 22

## CSS Grid on child elements
- [ ] Spanning over several columns:
  `grid-column: [start] / [end];`, `span` keyword
- [ ] Spanning over several rows: `grid-row: [start] / [end];`

---
# DAY 23

## Defining grid areas
- [ ] Template areas: setting the parent with keywords, css `grid-template-areas`
- [ ] Placing boxes in an area: css `grid-area`

---
# DAY 24

## Grid Use Cases
- [ ] Photo Gallery
- [ ] Blog Page

---
# DAY 25

## Fancy Shapes
- [ ] Creating shapes using the the `border` property -
  https://css-tricks.com/the-shapes-of-css/
- [ ] Cutting fancy shapes with `clip-path` - https://bennettfeely.com/clippy/
- [ ] Transforming shapes: `transform`, `rotate()`, `scale()`
- [ ] MDN transforms page for more advanced shapes

---
# DAY 26

## Built in Animations
- [ ] Transitioning property changes -
  css `transition: [prop] [duration] [timing]`
- [ ] Creating a nested navigation bar with `<nav>` and nested `<ul>`
- [ ] Showing dropdowns on `:hover` and `:focus`
- [ ] Best Design Practices: When and how much transition and animation

---
# DAY 27

## Custom Animations
- [ ] Creating custom animation scripts: `@keyframes [name] { ... }`
- [ ] Applying animations: `:hover` and `:focus`, css `animation`
- [ ] Controlling the script: `from`, `to` and `%` directives
- [ ] Changing the iteration and direction:
  `animation-iteration-count`, `animation-direction`
- [ ] Getting predefined animations: http://animista.net/

---
# DAY 28

## Animation use cases
  - Typewriter

---
# DAY 29

## Bootstrap
- [ ] Adding Bootstrap to our project (with CDNs) -
  JS dependencies and Bootstrap CSS, `<script src=""..."">`
- [ ] Content, Components, utilities - navigating the bootstrap documentation
- [ ] Using the Bootstrap grid system: grid classes and flex
- [ ] Smart copy pasting - read, understand, copy, modify
- [ ] Using Bootstrap components: Creating a page with close to 0 CSS

---
# DAY 30

## Sass Introduction
- [ ] What is a preprocessor: Quick definition of transpilation
- [ ] Installing SASS: `npm install -g sass`
- [ ] Creating input: `.scss` vs. `.sass`, nesting CSS rules
- [ ] Comparing the output: `sass [input file] [output file]`

## Build scripts: Using npm as a build tool
- [ ] DCI Project boilerplate I:
  https://github.com/DigitalCareerInstitute/dci-boilerplate-I
  Presenting the HTML/CSS Sass Bootstrap boilerplate (including dependencies)
- [ ] Installing dependencies: `npm install`
- [ ] Running for development: `npm start`
- [ ] Building for publication: `npm run build`
- [ ] Publishing online: `npm run deploy`

## Sass Variables: an introduction
- [ ] Variables concept: "A box to keep values in"
- [ ] Vanilla CSS Variables:
  Defining in `:root { --[name]: [value] }`,
  Using with `var(--[name], [fallback])`
- [ ] Sass variables: Defining with `$[name]: [value]`, Using with `$[name]`
- [ ] Sass maps: A collection of variables in one name
- [ ] Main use case for variables: Customizing bootstrap colors and options

---
# DAY 31

## Sass Mixins: Predefined reusable rulesets
- [ ] Defining mixins: `@mixin [name](){ ... }`
- [ ] Using mixins: `@include [name]()`
- [ ] Parameters and arguments:
  `@mixin [name]([parameters])`, `@include [name]([arguments])`
- [ ] Main use case for mixins: Using bootstrap breakpoint mixins

---
# DAY 32
## Learning More Sass: Various resources to learn sass and other preprocessors

---
# DAY 33

## Publishing with GitHub pages
## Publishing through the terminal with git:
- [ ] Creating and pushing our `gh-pages` branch
- [ ] Publishing flow: previewing changes on `master`, merging to `gh-pages`
## Automating the flow: `gh-pages` tool
- [ ] Installing `gh-pages`: `npm install -g gh-pages`
- [ ] Publishing through the terminal: running `gh-pages` in a repository

---
## UI Basic - Advanced Test

---
# DAYS 34 - 36
- [ ] Final portfolio project / presentations
