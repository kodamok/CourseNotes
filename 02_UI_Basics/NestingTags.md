# Nesting Elements

Every element in HTML is defined by a *tag* such as `<body>`, `<div>` or `<img>`. A tag consists of an opening *less than* symbol `<`, a type name, and a closing *greater than* `>` symbol.

## Opening and closing tags
Some elements require both opening `<...>` and closing `</...>` tags. A closing tag is identified by the *slash* character before the type name, like this: `<html> ... </html>`

Here are two examples: `<p>some text</p> ` or `<a href="path/to/file.html">Link Text</a>`.

### Balancing tags
Opening and closing tags need to be *balanced*. This means that every opening tag for a particular type must be matched by a closing tag for the same type later in the document.

### Nesting elements
Elements with closing tags can contain *nested* elements inside them. In the following example, there is:

* A `<div>` element nested inside the `<body>` element
* `<h1>`, `<figure>` and `<p>` elements nested inside the `<div>`
* `<img />` and `<figcaption>` elements nested inside the `<figure>` element

```html
<html>
  <body>
    <div>
      <h1>Header</h1>
      <figure>
        <img src="my_image.png" alt="description of image" />
        <figcaption>Caption for image</figcaption>
      </figure>
      <p>Lorem ipsum ...</p>
    </div>
  </body>
</html>
```

### Family metaphor
We use a family metaphor to describe the relationship between elements.
* Elements that are nested inside other elements are called *children*. In the example above, the `<div>` is a direct *child* of the `<body>`.
* The element they are nested in is their *parent*. The `<body>` is the parent of the `<div>`.
* One parent can have several children. The children of a given parent are *siblings*, in relation to each other. The `<h1>`, `<figure>` and `<p>` elements are all siblings.
* In a deeply nested structure, you can refer to all the children and their children's children as *descendants*. The `<div>`, `<h1>`, `<figure>`, `<p>`, `<img />` and `<figcaption>` elements are all descendants of the `<body> ` element.
* The parent and parent's parent (and so on, all the way up to the enclosing `<html>` element) are called *ascendants* or *ancestors*. The `<img>` element has four ancestors: `<figure>`, `<div>`, `<body>`, and `<html>`.

### Auto closing tags cannot nest other elements
Certain other elements, like `<img />`, `<br />` and `<meta />`, consist of a single tag. The technical term is [`void element`](https://html.spec.whatwg.org/multipage/syntax.html#void-elements), but you will see them referred to more often as *auto closing* elements. These elements, by definition, cannot contain any other elements.

The space and slash `/`  before the closing `>` symbol are optional. These are all valid tags that will create a *horizontal rule* (line):
* `<hr>`
* `<hr/>`
* `<hr />`

Using the final slash will help to remind you that this tag is auto closing.

### Block and Inline display
Elements can be divided into two display types:
* `block`-level elements are containers which, by default, are displayed like vertical building blocks. They take up the full width of their parent. An element that follows a `block` element will start on a new line. The elements `<header>`, `<main>`,`<div>`, `<p>` and  `<footer>`, for example, are all displayed by default as `block` elements.
* `inline` elements are containers whose contents extends horizontally and wraps to the next line wherever there is not enough space to continue horizontally. Their width is determined by their content, or limited by the width of their parent. The elements `<a>`, `<img>` and  `<span>`, for example, are all displayed by default as `inline` elements.

Here is a [list of elements](https://www.w3schools.com/html/html_blocks.asp), showing which are block-level elements and which are inline.

## Nesting rules

Here are some rules about how elements are nested.

1. **Void elements cannot nest any children**
2. **Elements cannot overlap**

    Here is an extract of HTML that will show some "*italic and **bold italic*** text":

    `some <em>italic and <strong>bold italic</strong></em> text`

    Note that both styles (italic and bold) end at the same point, but the `<strong>` (bold) element is closed first. The following HTML code would be invalid...

    > some &lt;em&gt;italic and &lt;strong&gt;bold italic&lt;/em&gt;&lt;/strong&gt; text

    ... because the two elements' start and end tags overlap.

3. **Inline elements cannot contain block elements**

   It makes no sense to place a `<p>`  paragraph (which starts on a new line) inside a `<span>` (which wraps automatically to the next line), for instance.

4. **Block elements of type text cannot be nested**
   
   If you need to include a list (`<ul>`, `<ol>` or `<dl>`) in a text section, do not nest these inside a paragraph (`<p>`)

5. Block elements can nest inline elements
6. Inline elements can nest other inline elements
7. Container block elements can contain other block elements
8. You can nest one list as part of an item (`<li>`) inside another list.

    ```html
    <ul>
      <li>Fruit
        <ul>
          <li>Bananas</li>
          <li>Apples</li>
          <li>Pears</li>
        </ul>
      </li>
      <li>Vegetables</li>
      <li>Meat</li>
    </ul>
    ```

    <ul>
      <li>Fruit
        <ul>
          <li>Bananas</li>
          <li>Apples</li>
          <li>Pears</li>
        </ul>
      </li>
      <li>Vegetables</li>
      <li>Meat</li>
    </ul>
