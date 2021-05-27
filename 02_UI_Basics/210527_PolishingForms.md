# Review of forms

## Usability

* [Design Best Practices](FormDesign_BestPractices.pdf)

- [ ] Label around checkbox and radio button
   * Include space between button and label
   * Accessibility: still use `for` and `id`

- [ ] [Email validation](https://en.wikipedia.org/wiki/Email_address#Syntax)

- [ ] `autofocus` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)
   * [Demo](https://github.com/FbW-E04-1/ClassBook/tree/main/UIB/2021-05-27/autofocus)
- [ ] `disabled` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/disabled)
- [ ] `readonly` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/readonly)

### Pseudo-classes
- [ ] `:autofill` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:autofill)
   * [Styling autofilled elements](https://css-tricks.com/snippets/css/change-autocomplete-styles-webkit-browsers/)
- [ ] `:placeholder` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/::placeholder)
- [ ] `:focus` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus)
- [ ] *`outline`* [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/outline)
- [ ] [more...](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes#the_input_pseudo-classes)

## More Inputs
* [Form Inputs](Forms.pdf)

- [ ] `<input type="search">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/search)
   * `name="q"`
   * × to delete contents
   * May show previous search terms

- [ ] `<input type="checkbox">`
   * Multiple buttons in group with same `name`
   * [Demo](https://github.com/FbW-E04-1/ClassBook/tree/main/UIB/2021-05-27/checkbox-multiple)
   * Style as toggle switch
   * [Demo](https://github.com/FbW-E04-1/ClassBook/tree/main/UIB/2021-05-27/toggle-switch)

- [ ] `<input type="file">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/file)
   * `accept`
     * `audio/*`, `audio/mp3`
     * `video/*`
     * `image/*`
     * file type specifiers
   * `capture`: visitor can use microphone or camera
   * `multiple`
   * Need server-side treatment to store uploaded file
   * [Demo](https://github.com/FbW-E04-1/ClassBook/tree/main/UIB/2021-05-27/toggle-switch)

- [ ] `<input type="hidden">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/hidden)
   * Invisible to user
   * Example: id of database record being edited

- [ ] `<input type="image">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/image)
   * Provides `x`, `y` coordinates of click
- [ ] `<input type="password">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/password)
   * Set `type` to `text` to show content
   * [Demo](https://github.com/FbW-E04-1/ClassBook/tree/main/UIB/2021-05-27/show-password)
- [ ] `<input type="radio">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/radio)
   * Multiple buttons in group with same `name`
   * `checked`
   * Custom styling
   * [Demo](https://github.com/FbW-E04-1/ClassBook/tree/main/UIB/2021-05-27/styled-radio)
- [ ] `<input type="range">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/range)
- [ ] `<input type="reset">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/reset)

- [ ] `<input type="time">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/time)
- [ ] `<input type="url">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/url)
---
- [ ] `<textarea>` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea)
- [ ] `<select>` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select)
- [ ] `<optgroup>`[MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/optgroup)
- [ ] `datalist` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist) [CanIUse](https://caniuse.com/datalist)


## Styling Tricks

- [ ] `<fieldset>` [w3.org](https://www.w3.org/TR/2016/REC-html51-20161101/rendering.html#the-fieldset-and-legend-elements)
- [ ] `<legend>`
   *  `direction: rtl` must be set on parent `<fieldset>`

- [ ] [CSS-only toggle switch](https://dev.to/dcodeyt/creating-a-css-only-toggle-switch-5cg3)
- [ ] CSS custom properties [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties) [W3C](https://www.w3.org/TR/css-variables-1/#defining-variables)
- [ ] Custom styling radio buttons

## Resources

- [HTML Web Forms Tutorial](https://html.com/forms/)
- [How to Style Forms With CSS](https://blog.logrocket.com/how-to-style-forms-with-css-a-beginners-guide/)
- [Custom Styles for Form Inputs and Textareas](https://moderncss.dev/custom-css-styles-for-form-inputs-and-textareas/)


## Exercises

* [Transparent Login](https://classroom.github.com/a/DmimjUc5)
  ![Transparent Login](data_img/transparent_login.png)
* [Swagger](https://classroom.github.com/a/dELpsdSk)
  ![Validated Swagger](data_img/validated.png)
* [Swagger part 2 (validation)](https://classroom.github.com/a/RzdUmN-K)
