# Create a Single Page Site with Menubar

[Find your repositories here](https://classroom.github.com/a/RfgHLozF)

1. Open VSCode
2. Open the Terminal pane
3. Use `cd` to navigate to the directory where you save your experiments
4. Make a directory for your new project, and `cd` into it (Ask Emad about `mkcd`)
5. Use the command `code -r .` to open the current folder in the current window (`-r` = reuse, `.` = this folder)
6. `touch index.html`
7. Press the Up arrow to show the previous command
8. Use `Ctrl-A` to move the cursor to the beginning of the line
9. Use `Ctrl-Delete` (Entf) to delete the word to the right of the cursor
10. Type `code` then press Enter
11. Type `!` then press Enter, to create the boilerplate for an HTML page
12. Press the Tab key twice to select the word "Document" in the `<title>` tag, and replace it with a better title
---
13. Press Tab again to place the cursor inside the `<body>` tag
14. Add a `<h1>` tag
15. Add a `<nav>` tag
16. Add three `<a>` tags inside the `<nav>` tag, and give each a different `href` using the `#` (id) symbol
17. Create a `<main>` tag
18. Create three `<div>` tags inside the `<main>` tag, each with an `id` that corresponds to one of the `href`s in the links in the `<nav>` tag
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Better Title</title>
  </head>
  <body>
    <h1>Better Title</h1>

    <nav>
      <a href="#first">First Step</a>
      <a href="#second">Second Step</a>
      <a href="#third">Third Step</a>
    </nav>

    <main>
      <div id="first">
        <h2>First Step</h2>
      </div>
      <div id="second">
        <h2>Second Step</h2>
      </div>
      <div id="third">
        <h2>Third Step</h2>
      </div>
    </main>
  </body>
</html>
```
19. Start the Live Server to see the result in a browser
    * Click on Go Live in the blue status bar at the bottom of the VS Code window
    * Press Fn-F1, then type Live Open, and press Enter
---
20. Press Ctrl-` to activate the Terminal pane
21. Type `mkdir css;touch css/style.css`
22. Add a `<link>` element to the `<head>` and add `css/style.css` as the value for `href`.
23. Open the `style.css` document in the VS Code editor pane.
24. Give a good `background-color` to each of the elements `body` and `nav`
25. Set the `text-align` of the `nav` element to `center`
```css
body {
  background-color: #fec;
}

nav {
  background-color: #dcb;
  text-align: center;
}
```
---

26. Give some style to the `<a>` tags: `border` with the style `outset`, and  `width`
```css
a {
  border: 0.2em #cba outset;
  width: 30%;
}
```
27. Note that the width of the `a` elements does not change.
28. Add `display: inline-block`

```css
a {
  border: 0.2em #cba outset;
  width: 30%;
  display: inline-block;
}
```
29. Add a new rule with the `:hover` pseudo-class, to change the `border-color`, `border-style` and `background-color`
```css
a:hover {
  border-color: #a98;
  border-style: inset;
  background-color: #ba9;
}
```
30. In the browser window, test what happens when you hover over a link.
31. Remove the default blue color and underline from the `a` elements:
```css
a {
  border: 0.2em #cba outset;
  width: 30%;
  display: inline-block;

  text-decoration: none;
  color: #000;
}
```
32. Add a rule with the `:visited` pseudo-class:
```css
a:visited {
  background-color: #987;
  color: #fff;
}
```
33. Click on a link and observe what happens. Roll the mouse on and off, and see what happens then. Look at what happens to the address in the browser's address bar.

**Note that, for privacy reasons, the number of properties that can be set for the [`:visited` pseudo-class](https://developer.mozilla.org/en-US/docs/Web/CSS/:visited) is very limited.**

---
34. To reset the `visited` status of a link to `false`:
    * Press Ctrl-H to open your browser history
    * For each link to your new web page:
      * Select the `⋮` contextual menu
      * Select Remove From History
---
1.  Now for the magic. Add two new rules:
```css
div {
  display: none;
}

:target {
  display: block;
}
```
36. The first rule hides all the `<div>` elements inside the `<main>` tag. The second *shows only the `<div>` element whose `id` is the same as the `#` chunk in the address bar*.
37. Click on each `<a>` link in turn, to see the effect
---
**But what happens if you remove the #chunk from the address bar? All the `<div>` elements disappear.**
38. Change the last two rules to include a second selector each:
```css
div,
:target ~ :last-child {
  display: none;
}

:target,
div:last-child {
  display: block;
}
```
39. The last rule says: "show the element with the same `id` as the *fragment* in the address bar, and the div that is last element in its parent group."
40. The second-last rule says: "hide all divs, and the sibling of the element with the same `id` as the fragment in the address, if it is the last div in its parent group."
41. The selector `:target ~ :last-child` has a higher *specificity* than `div:last-child`, so it takes precedence, even if it occurs earlier. The `:target` selector indicates an `id`, which the `div:last-child` element is lacking.
---
42. Change the order of the `<div>` elements, so that the first element is shown by default. The order of the other elements does not, in fact, matter, since only one element will be shown at a time:
```css
<main>
  <div id="second">
    <h2>Second Step</h2>
  </div>
  <div id="third">
    <h2>Third Step</h2>
  </div>
  <div id="first">
    <h2>First Step</h2>
  </div>
</main>
```
## Exercise:
* Imagine how this technique could be useful in your own personal project.
* Edit the content and the links to make it relevant
* Adapt the CSS to suit your tastes

## What You've Seen:
* The `<nav>` element
* The `<main>` element
* The `<div>` element
* [Semantic markup](https://www.google.com/search?q=semantic+markup&oq=semanti&aqs=chrome.0.69i59j0l2j69i57j0l2j69i60l2.1704j1j7&sourceid=chrome&ie=UTF-8)
* The [`display` property](https://developer.mozilla.org/en-US/docs/Web/CSS/display) (values include `block`, `inline-block`, `none`...)
---
* The use of an `id` as an `href` target
* How the address in the address bar updates to show the `href` as a [*fragment*](https://en.wikipedia.org/wiki/URI_fragment)
* You've already seen how the page will scroll to show the `id` referenced by the fragment, if necessary.

---
* The existence of ["pseudo-classes"](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes):
  * :hover
  * :visited
  * :target
  * :last-child
* The order of rules is important (`:hover` before `:visited`)
* Altering the appearance of a link
* The [*specificity*](https://github.com/DigitalCareerInstitute/web-dev-v3-slides/blob/master/B_UI-Basics/02_Content/CSS%20Specificity%2C%20Inheritance%20and%20the%20Cascade.pdf) of selectors is important, so an earlier rule with a more specific selector can take precedence over a later one
---
* The [`~` sibling combinator](https://developer.mozilla.org/en-US/docs/Web/CSS/General_sibling_combinator)
* Multiple selectors
* Multiple elements in a selector
* [Additional selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors)
* [More combinators](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Combinators)
---
* Shortcuts when working in the Terminal


## Bonus 1

Prevent user from selecting link text; prevent the text from being draggable.
* Add two rules to the `a` selector:
```css
a {
  /* ... */

  user-select: none;
  -webkit-user-drag: none;
}
```

## Bonus 2

Keep the menu buttons visible at all times.
* Add two instruction to the rules for the `nav` selector:

```css
nav {
  background-color: #dcb;
  text-align: center;

  position: sticky;
  top: 0;
}
```
* Add a new rule to prevent the `<h2>` tag from being hidden when you click a link:
  ```
  :target > h2 {
    padding-top: 2em;
  }
  ```

## Bonus 3

[Creating `alias`es for the Terminal](https://github.com/FbW-E04-1/CourseNotes/blob/main/99_Productivity/bash/alias.md)
