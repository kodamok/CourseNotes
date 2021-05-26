# Review of forms

* [Forms Basics](Forms-Inputs.pdf)

## Validation
- [ ] `required` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/required)
- [ ] `minlength` & `maxlength` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/minlength)
- [ ] `pattern` = regular expression [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/pattern)
- [ ] `title` attribute to describe the pattern (tooltip) [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/title)

- [ ] [Email validation](https://en.wikipedia.org/wiki/Email_address#Syntax)

## Other attributes
- [ ] `autofocus` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)
- [ ] `disabled` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/disabled)
- [ ] `readonly` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/readonly)

### Pseudo-classes
- [ ] `:valid` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:valid)
- [ ] `:invalid` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid)
- [ ] `:required` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:required)
- [ ] `:autofill` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:autofill)
   * [Styling autofilled elements](https://css-tricks.com/snippets/css/change-autocomplete-styles-webkit-browsers/)
- [ ] `:checked` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:checked)
- [ ] `:disabled` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:disabled)
- [ ] `:placeholder` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/::placeholder)
- [ ] `:placeholder-shown` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:placeholder-shown)
- [ ] `:focus` [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus)
- [ ] *`outline`* [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/outline)
- [ ] [more...](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes#the_input_pseudo-classes)

## All the Inputs
* [Form Inputs](Forms.pdf)

- [ ] `<input type="search">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/search)
   * `name="q"`
   * × to delete contents
   * May show previous search terms

- [ ] `<input type="button">`
   * No label required
- [ ] `<input type="checkbox">`
   * Multiple buttons in group with same `name`
   * Style as toggle switch
- [ ] `<input type="color">`
   * Different in different browsers (Chrome, Firefox, Epiphany, ...)

- [ ] `<input type="date">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/date)
   * `YYYY-MM-DD` format for `value`, `min` and `max`
   * `step` starts from `min` date, if present
   * Use `pattern` for older browsers with text-only input
   * Show validation with `::after`

- [ ] `<input type="datetime-local">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/datetime-local)
   * Limited support

- [ ] `<input type="file">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/file)
   * `accept`
     * `audio/*`, `audio/mp3`
     * `video/*`
     * `image/*`
     * file type specifiers
   * `capture`: visitor can use microphone or camera
   * `multiple`
   * Need server-side treatment to store uploaded file
   * Cannot

- [ ] `<input type="hidden">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/hidden)
   * Invisible to user
   * Example: id of database record being edited

- [ ] `<input type="image">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/image)
   * Provides `x`, `y` coordinates of click
- [ ] `<input type="month">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/month)
- [ ] `<input type="number">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/number)
- [ ] `<input type="password">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/password)
   * Set `type` to `text` to show content
- [ ] `<input type="radio">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/radio)
   * Multiple buttons in group with same `name`
   * `checked`
   * Style as toggle switch
- [ ] `<input type="range">`
- [ ] `<input type="reset">`
- [ ] `<input type="submit">`
- [ ] `<input type="tel">`
- [ ] `<input type="text">` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/text)
- [ ] `<input type="time">`
- [ ] `<input type="url">`
- [ ] `<input type="week">`
---
- [ ] `<textarea>` [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea)

## Usability

* [Design Best Practices](FormDesign_BestPractices.pdf)

- [ ] Label around checkbox and radio button
   * Include space between button and label
   * Accessibility: still use `for` and `id`
- [ ] `<select>`
- [ ] `<optgroup>`
- [ ] `datalist`


## Styling Tricks

- [ ] `<fieldset>` [w3.org](https://www.w3.org/TR/2016/REC-html51-20161101/rendering.html#the-fieldset-and-legend-elements)
- [ ] `<legend>`
   *  `direction: rtl` must be set on parent `<fieldset>`

- [ ] [CSS-only toggle switch](https://dev.to/dcodeyt/creating-a-css-only-toggle-switch-5cg3)

- [ ] Custom styling radio buttons
