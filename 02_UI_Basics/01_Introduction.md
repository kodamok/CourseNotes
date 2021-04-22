# Mastering Git

- [GitHub teaches GitHub](https://github.com/FbW-E04-1/learn-github)
- [Interactive tutorial](https://learngitbranching.js.org/)
- [Tutorial on Branches](https://www.tutorialspoint.com/git/git_managing_branches.htm)

# UI Basics

## [HTML and CSS Pre-Test](https://forms.gle/vqcHfKTiWBoWWLRN8)

## [Install Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

## [Install Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)

- Launch VS Code
- Press Ctrl-Shift-P to open the Command Palette (View > Command Palette)
- Enter `ext install ritwickdey.LiveServer` in the text field
- Press Enter

## Test Live Server

- Open a new window: Ctrl-Shift-N
- Create a new folder for your project and open it: Ctrl-K Ctrl-0
- `touch index.html && code index.html`
- Type

```html
Hello World!
```

- Press Ctrl-Shift-P to open the Command Palette (View > Command Palette)
- Type `live open`
- Press Enter
- Google Chrome should open to show your web page

## Use the Developer Tools to inspect the page

- Open [Chrome Developer Tools](https://developer.chrome.com/docs/devtools/open/): Ctrl-Shift-I
- Notice that the browser has added tags:

```html
<html>
  <head></head>
  <body>
    Hello World!
  </body>
</html>
```

- Click on the &lt;body&gt; tag
- Click on the Styles pane in the Inspector
- Click on the `element.style {}` entry
- Add

```css
element.style {
  color: red;
  background: #fcc;
  font-size: 5px;
}
```

- Test with a font-size of `5vw`, `5vh`, `5em`
- Use the up and down arrow keys
- Press Ctrl or Shift or Alt while pressing the arrow keys
- Add

```css
border: 1px solid black;
margin: 0;
```

- Toggle buttons on and off
- Add `border-style:` and select a value
- Copy the rule
- Reload the page

## CSS

- Edit your index.html file

```html
<html>
  <head>
    <style>
      body {
        color: red;
        background: #fcc;
        font-size: 5px;
        border: 1px solid black;
        margin: 0;
        border-style: dotted;
      }
    </style>
  </head>

  <body>
    Hello World!
  </body>
</html>
```

- Save
- Notice that Live Server has injected a script

## Minimal code for an HTML page

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Text for Browser Tab</title>
    <link rel="stylesheet" href="style.css" />
    <script src="script.js"></script>
  </head>

  <body>
    Page content goes here
  </body>
</html>
```

- Create separate folders and files for css, js and img

## Tags

- html
- head
- body

### [Head Tags](https://www.w3schools.com/tags/tag_head.asp)

- <span style="color:red">title</span>
- [meta](https://www.w3schools.com/tags/tag_meta.asp)
- link
  - For CSS
  - _empty element_
- script
  - For JavaScript
  - Can contain link or code

### Common Body Tags

- &lt;h1&gt;&lt;/h1&gt;
- &lt;p&gt;&lt;/p&gt;
- &lt;div&gt;&lt;/div&gt;
- &lt;img /&gt;
- &lt;a&gt;&lt;/a&gt;
- &lt;span&gt;&lt;/span&gt;
- &lt;ul&gt;&lt;/ul&gt;
- &lt;ol&gt;&lt;/ol&gt;
- &lt;li&gt;&lt;/li&gt;
- &lt;!-- _comment_ --&gt;

### Attributes

- class
- id
- style

### CSS selectors and rules

## Topics

1. Content
1. Box Model
1. Flow
1. UI/UX
1. Data
1. Responsive Design
1. Layout
1. Interactions
1. Framework
1. Publishing
1. Assessment
1. Project

## Tools

- [Emmet](https://code.visualstudio.com/docs/editor/emmet)
- [CodePen](https://codepen.io/)

## Slides

- [Boilerplate](Boilerplate.pdf)
- [CSS](CSS%20Specificity%2C%20Inheritance%20and%20the%20Cascade.pdf)
- [Box Model](canva-intro-content-boxes.pdf)
- [Accessibility](What%20is%20web%20accessibility_.pdf)

## Resources

- [Learn HTML](https://www.internetingishard.com/html-and-css/basic-web-pages/)
- [Learn CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps)
- [meta](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta)
- [Video: What happens when you load a webpage?](https://youtu.be/OE8EvaOPkZ4?t=16)
