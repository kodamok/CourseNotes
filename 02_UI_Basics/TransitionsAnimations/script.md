

Today, we're going to look at a couple of ways to create interactions without actually using any JavaScript.

In particular, we'll be looking at CSS **Transitions** and **Animations**, and we'll also look at a CSS property called _clip-path_.
I'll show you how to make a simple game. Because we aren't using any JavaScript, we'll be using the `:hover` pseudo-class to trigger an action, rather than a click.

[Game](https://dciforks.github.io/UIB-interaction-bullseye/)


## clip-path

Let's start by looking at `clip-path`. I'll create a web page with a square image. I want to centre the image on the page. How can I do that?

First I'll set the `width` of the image to `100vmin`, so that it will fit neatly into the available space

Then I'll remove the border from the body, and set it's height to fill the page: `100vh`

I'll use `display: grid; place-content: center;`, and now the image will fill the centre of my page, regardless of the page dimensions.

OK so far? There's nothing here that is new or unexpected?

### circle()
Now, I'll add a `clip-path` property to the image. This takes a value that defines a path. Everything outside the path will not be displayed. The simplest value is `circle()`

This will create a circle whose diameter is just the right size so that it just reaches the edge of the element that it is applied to. I'll distort the image so that you will see that the circle adjusts to fit.

`width: 90vw; height: 90vh;`

By default, this circle is centred on the element. I can make that explicit by using `at 50% 50%`.

### at <centerX centerY>
If I change the position of the centre, the diameter will adjust so that, once again, the circle just touches the nearest edge.

### border and padding
Let me give the image a thick yellow border...

`border: 20px solid yellow`

... and you can see that the clipping is applied to the border, too.

If I change the `box-sizing` ... the result is the same.

And for `padding`, too. `padding: 20px`.

The area that is clipped is the area inside the `border-box`.

### radius
I can also give a radius for the circle. I can use any units: `px`, `em`, `rem`, `vw`, `vh`, `vmin`, `vmax` ... or `%`. If I use `%` then the question is "Percentage of what? Width? Height?" The answer is "A proportion of the diagonal". The precise answer is "The diagonal divided by the square root of 2", but if maths is not your favourite subject, then you can use `50%` on a square image to get the same effect as you saw with just plain `circle`. If the image is not square, then the result is different. Whatever shape the element is `70.7%` (or the square root of 1 over 2) to create a circle that contains the whole image.

Here: I set it to `70%` and you can see that the corners are just clipped, regardless of the shape of the image. At `70.7%`, the clipping is (almost) gone.



### radius and centre

You can set both radius and centre, and in this case the circle may go beyond the borders, and you'll get the border as a straight edge, because the circular area outside the border of the element will be ignored.

Let me place the centre in the corner and use a radius of `100%`:

`clip-path: circle(100% at 0 0);`

This create a quarter circle which includes the two corners nearest to the centre. To include the entire image, I'll need to use `141.4%`, to stretch across the whole diagonal.

`clip-path: circle(140% at 0 0);`

### out-of-range values

You can set the centre of the circle outside the area of the element, but then you must provide a radius big enough for the circle to reach into the area.

`clip-path: circle(70% at 150% -10%);`

If you set the radius to a negative value, the property is invalid and won't be applied.

### Summary of circle
So to resume what I have showed you so far:
1. I can clip an image with `clip-path: circle()`.
2. I can set the centre of the circle.
3. I can set the radius of the circle.
4. I've used `%` units, because they are relative to the size of the element, but you can use any units.
5. If I dont' set a centre, the centre of the element is used by default.
6. If I don't give a radius, the browser will create a circle that just touches the nearest edge
7. If you set both the centre and the radius, then the circle may go beyond the borders of the element, where it is ignored.
8. You can place the centre outside the area of the element
9. You can't use negative values for radius
10. The element takes up the same space on the page. It's just that parts of it are not shown.

Who has a question about what you have seen so far?

### Other element types
What about text? I'll create some "Lorem ipsum", set its width so that it is square-ish, and apply a circle clip-path.

What about containers? I can apply a circular `clip-path` to the `body` itself.

## Other shapes

Now, `circle` is not the only shape of path you can create. I'll show you a basic `ellipse`.

### ellipse
Like `circle`, by default an ellipse is centred on the element, and its dimensions are chosen to just touch every edge.

If you set the centre — `clip-path: ellipse(at 36% 48%)` — then again, the dimensions of the ellipse will adjust. If you explicitly set the radius, then your ellipse might extend beyond the borders of the element, just like with the circle.

Note that an ellipse has two radii: horizontal and vertical. You can't create an ellipse at an angle... or you can, but it requires some trickery using rotations and a background image on an `:after` pseudo element, so I'm not going to cover it here.
[How to Rotate Clip Path without rotating image?](https://stackoverflow.com/a/51010685/1927589)

To sum up:
* `ellipse()` is like `circle()`, except that it has both a horizontal and a vertical radius.

### inset

To create a rectangular `crop-path`, you can use the `inset()` value. This works like `margin`, `border` and `padding`. If you give one value, it is applied to all sides. If you give two, they are applied top-and-bottom and left-and-right. Three, and top and bottom are applied separately. Four, and you can set the inset on all sides.


### polygon and path
There are two more basic `clip-path` types: `polygon` and `path`. I'm not going to show you `path` because not all browsers support it yet. In those browser, you can use `path` to connect both straight and curved lines to create a complex outline. The `polygon` path type only allows straight lines, and so its syntax is simpler. You create a series of points, and the browser draws straight lines between the points.

But before I show you that, I want to show you a little magic.

## Interactions

I'll remove the paragraph, the padding and the borders, and I'll create a circle around the lion's left eye...

```css
img {
  width: 100vmin;
  clip-path: circle(5% at 55% 39%);
}
```

... and I'll add a rule for when you hover over the element:

```css
img:hover {
  clip-path: circle(at 55% 39%);
}
```
What do you expect to happen when I move my mouse over the image?

1. The `:hover` only takes effect over the visible part of the image
2. The circle widens until it touches the nearest edge.
3. When I drag the mouse off the wider circle, the `:hover` is no longer active.

How can I show the entire picture?

I can set the radius to a value big enough for the circle to contain the whole image. Through trial and error, I discovered that `80%` is enough, but let me use 100% for simplicity, so that you can still see that the `clip-path` is a circle.


```css
img:hover {
  clip-path: circle(80% at 55% 39%);
}
```

# Transitions

Now for the magic. Here's a new CSS property: `transition`. I'll add it to the rule for the `img` element:

```css
img {
  width: 100vmin;
  clip-path: circle(5% at 55% 39%);
  transition: 1s;
}
```
The value that I have given it is 1 second.

Now, when I hover, the browser sees that value for the `clip-path` changes, and it _interpolates_ all the intervening values,progressively over 1 second. When I move the mouse off the image, once again, the browser takes 1 second to transition between the two values.

## transition on :hover

If I move the `transition` property to the `:hover` rule, the transition is only applied during the hover. When I stop hovering,, the `clip-path` jumps back in one step.

## All animatable properties

Here, I showed you a change in the value of the property `clip-path` but there are many properties that can be _animated_.
[Animatable CSS properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties)

Let me show you with `opacity`.

Indeed, there are only a few which cannot be altered gradually from one value to another. For example: `display` cannot transition from `block` to `inline` or to `none`. There are no intermediate steps. The change will be immediate.

Another property, that we can test here, is `background`. Let me change the `img` element to a `div` with a background-image:

```css
div {
  width: 100vmin;
  height: 100vmin;
  clip-path: circle(5% at 55% 39%);
  background:
    url(../img/lion.jpg) center / contain no-repeat;
  transition: 1s
}


div:hover {
  clip-path: circle(82% at 55% 39%);
  background:
    url(../img/horse.jpg) center / contain no-repeat;
}
```

**Comment out `<img>` in HTML and add `<div>`**

As you can see, the background image jumps to the new value immediately. If you want to cross-fade from one image to another, you will need to use a different technique.

## Semi-animatable properties

Others like `visibility`, which can take the simple values `visible` or `hidden` _can sort of_ animate, in that the switch occurs at the _end_ of the transition.

Let me revert to using an image, I'll show you how `visibility` is applied at the end of the transition:

```css
img {
  width: 100vmin;
  clip-path: circle(5% at 55% 39%);
  transition: 1s
}


img:hover {
  clip-path: circle(82% at 55% 39%);
  /* opacity: 0.2; */
  visibility: hidden;
}
```

**Uncomment `<img>` in HTML and remove `<div>`**

### Sub-summary

The moral is that, if a transition is not working the way that you expect, you might need to check if the property that you are changing is _animatable_.

##

So far, you've seen that you can set a duration for a transition, and all the transitions for all animatable properties take this same duration. Before we look at more properties and values associated with `clip-path` and `transition`s, there's an exercise that you can do to practise what you've seen so far.

In this exercise, you'll use `clip-path` to create a circular `div` in a layer above some dummy text. When you hover over the `div`, it will expand into an ellipse with the same dimensions as the `p` element, it will change color and its opacity will decrease.

You'll be using a `transition` property to make the transition gradual. The shape will expand more slowly than it contracts when you stop hovering.

So:
1. Position the `div` over the `p`aragraph
2. Create a `clip-path` where the horizontal and vertical radii are the same
3. Create a rule for `div:hover` with:
  * A different `clip-path`
  * A different `color `
  * A different `opacity`
  * Set a transition time for the `:hover` state
  * Set a different transition time for "un:hovering"

Is there anything in what I've shown you so far that you want me to review before you begin?

---

# Live Code solution

## Named transition times

So far, all the transitions have taken the same amount of time. But you can give different durations for different properties. On `div:hover`, when the shape is expanding, let me provide different durations:

```css
div:hover {
  /* ... */
  transition: clip-path 1s, background-color 5s;
}
```
The `clip-path` will take 1 second as before, but the `background-color` will take longer to change. And what about `opacity`? How long will its transition last?

0s

If property names are given, then any unnamed property will change immediately.

## delay

Suppose I set `opacity` to change over 5s too... now it's not clear whether its the `color` that is changing or the `opacity` because they are both happening at once.

I can add a second time value, to represent a delay...

`  transition: clip-path 1s, background-color 5s, opacity 5s 5s;`

... but now the value for the `transition` property is getting complicated. There's an alternative syntax that allows you to define different properties on different lines, like a table:

```css
div:hover{
  /* ... */
  transition-property: clip-path, background-color, opacity;
  transition-duration: 1s,        5s,               5s;
  transition-delay:    0ms,       0ms,              5s;
}
```

And there's one more property that you can use: `transition-timing-function`

* linear
* ease (default)
* ease-in
* ease-out
* ease-in-out
* cubic-bezier(p1, p2, p3, p4)

* steps

Linear will move at a constant rate. Ease (and ease-in-out) start slowly get faster, and slow down towards the end. Ease-in starts slowly and gets faster. Ease-out starts fast and gets slower. And cubic-bezier allows you to customize the easing in and out.

Steps gives a number of discrete steps, all at the same speed. We'll play with that in a little while.

# Animation

Actually, to understand the transition-timing-function, let me jump ahead a little and introduce animations. Animations are basically transitions that can repeat, or go forwards and backwards, a given number of times or forever. In other words: transitions that you can play one after the other, like beads on a string.

A simple example would be a bouncing ball.

I'll create a new HTML page with two divs: a ball and the ground that it can bounce on. I'll put the ball in front of the ground.

```html
div.ground
div.ball
```

For the CSS, I want to make the ball round. Can anyone remind me how to do that?

```css
div.ball {
  width: 10vmin;
  height: 10vmin;
  clip-path: circle();
  background-color: red;
}
```

The ground I can make rectangular and black and fix it to the bottom of the page:

```css
div.ground{
  width: 100vw;
  height: 10vh;
  position: fixed;
  bottom: 0;
  background-color: black;
}
```
Is there anything new here? Are there any questions about that?

## @keyframes

Now I want to make the ball bounce. I do this by giving the `div.ball` an animation name. I'll call it "bounce".

The animation is not stored in the rule for `div.ball`. An animation is created as a separate `@keyframes`

Now I creating an `@keyframes` at-rule. This means that different elements can use the same animation, using different settings.

Just like `@media` queries, these have curly brackets that enclose other rules. In this case, the "selectors" are not element types or classes but times. For now, we will use `0%` for the start of the movement and `100%` for the end of the movement. We don't use an actual duration time in seconds or milliseconds; we'll give that information in the rule for the ball `div` in a moment.

At time `0%`, I want the ball to be at the top of my page. At time `100%`, I want it to be at the bottom. I need to change the `top` property. I'll cheat a bit for now, to simplify the explanation


```css
@keyframes bounce {
  0% {
    top: 0
  }

  100% {
    top: 90vh;
  }
}
```

At the end of the movement, the top of the ball will be at the same height as the top of the ground, but that looks quite natural.

So now, I'll make it "bounce":

```css
div.ball{
  /* ... */
  animation-name: bounce;
  animation-duration: 1s;
  animation-iteration-count: 10;
}
```
It doesn't look very natural, because the default `-timing-function` is `ease`, which makes it start slowly (which is fine), speed up and end slowly (which is not fine). Also, it keeps playing from the top down. It reaches the bottom and then it pops back to the top immediately.

If I change the `animation-timing-function` to `ease-in`, it looks more like something falling...

` animation-timing-function: ease-in;`

... and there is another property `animation-direction` that lets me play the animation backwards and forwards:

`  animation-direction: alternate;`

`animation-direction` also takes other values, such as `normal`, `reverse`, `alternate-reverse`, and you can look them up on MDN when you need to use them.

---

So that makes it look more like a ball bouncing. If I set the `animation-iteration-count` to `infinite`, it will go on forever.

My point here was to show you the different kinds of `-timing-functions`, so let me try them, one by one:

* linear      — like a puck in a game of pong, moving at a constant speed
* ease        — (default) starts getting faster, ends getting slower
* ease-out    — starts fast, ends lower
* ease-in-out — like something oscillating on a spring, or a pendulum
* ease-in     — accelerating like something falling
* steps(N)    — a linear, step-wise motion, with a given number of steps

Steps holds the element in each position for 1/Nth of the time, which means that it may not reach the end, because that would require one more step that it doesn't have time for. It has a second parameter `jump-term` which you can use to tweak this. If you need to use `steps()` you can check out the different values for yourself. Here, I'll simply use `jump-none` to force it to take that extra step, so that you know that it can do it.

Now let's go back to `ease-in`, so that the bounce looks like a bounce.

## Animating multiple properties.

Just like with transitions, you can animate more than one property at once. Let me add an asterisk to the ball `div`, and `text-align: center;`, so that you can see it at the top.

Now I can get my `bounce` animation to use `transform: rotate()` to spin the ball as it is falling.

You've already seen `transform: translateX()`, when I showed you how to convert a checkbox into a sliding switch. Here, I'm going to make the ball rotate one complete rotation as it falls.

What units do we use to measure rotation?

Degrees or `deg`

So I'll set the `rotation()` to `0deg` at `0%` and `360deg` at `100%`. Neat, but not too natural. When the ball alternates its direction, it spins in the opposite direction too.

## Multiple animations

But that's ok. Instead of animating multiple properties with the same @keyframe animation rule, I can create multiple @keyframe animations, using a similar table-like layout to the one I showed you for transitions:


```css

div.ball {
  /* ... */
  animation-name:            bounce,    spin;
  animation-duration:        1s;
  animation-iteration-count: infinite;
  animation-timing-function: ease-in,   linear;
  animation-direction:       alternate, normal;
}


@keyframes spin {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
  }
}
```

I can give one value to certain properties, so that both @keyframe animations use the same value, or I can give a different one to each. The rotation animation will have a `-direction` of `normal` so that it keeps turning the same way. a `-timing-function` of `linear` so that it turns at a constant speed.

And I can make it rotate faster or slower by changing the `animation-duration`.

## move

And now that it is turning, let me make it move.

```css
div.ball {
  /* ... */
  animation-name:            bounce,    spin,   move;
  animation-duration:        1s,        0.5s,   5s;
  animation-iteration-count: infinite;
  animation-timing-function: ease-in,   linear, linear;
  animation-direction:       alternate, normal;
}

@keyframes move {
  0% {
    left: 0
  }
  100% {
    left: 90vw;
  }
}
```
I've cheated again a bit here: I've animated the `left` of the ball using `90vw`, but the ball is `10vmin` in diameter, so it might not quite reach the right side of the page. In the version that I've posted in the ClassBook repository, I've used `calc()` to get the exact value.

I've given the ball 5 seconds to cross the page, though it takes 2 seconds to bounce (down and then up), so it takes 2 ¹/₂ bounces to cross the page.

All three animations will continue forever, at different speeds. The spin and move animations are linear, moving at the same speed at all times.

But the `animation-direction` line only has two items. Which value is applied to the `move` animation? Let's test. Let me set the third item to `normal`...

And it starts over from the beginning after 5 seconds. So obviously, when there is no 3rd item, it is `alternate` that is applied.

In fact, if the browser gets to the end of the items, but it still needs another value, it will start reading the values again from the beginning of the list. So `alternate` is applied again for the third animation.

## Summary

So let's go through that again.

1. There are different `-timing-functions` for both transitions and animations.
  * Linear
  * Various accelerations
  * and Steps
2. For transitions, the property name is `transition-timing-function`
3. For animations, the property name is `animation-timing-function`
4. Animations are defined by `@keyframe` at-rules
5. Each `@keyframe` at-rule as a name. You can choose whatever names you want.
6. Within an `@keyframe` block, there are two or more keyframe definitions.
7. The "selectors" for the keyframe rules are percentages of time. (We've just looked at `0%` and `100%` so far, but you can add more intermediate points.)
8. You can modify more than one property at a time in any given keyframe definition.
9. You can add more than one animation to an element
10. You can give each animation different property values for
  * duration
  * direction
  * iteration-count
  * and other properties that I haven't shown you yet
10. If a list of values is shorter than the list of animations, then the browser will start reading the list again from the beginning.

Have you had time to take notes about all this, or is there something I need to go through again more slowly?

# Exercise

Time for an exercise to check whether my explanations have been clear.

Here's a square that rotates around an other square, changing its `background-color` as it goes. There are four different properties that are changing:
* top
* left
* background-color
* rotation

I've changed all these properties in the demonstration that I have just made, so you've seen them at work. There is one new idea: there are four distinct periods — _different keyframes_ — in the animation: down, right, up, left. Can you guess how the timing of the keyframes is organized?

25%, 50%, 75% and 100%

But you'll find that already laid out for you in the exercise. All you have to do is define the changes between each keyframe.

---

# Summary

This morning, I showed you three related topics:

* `clip-path` (which you can animate)
* transitions (a one-way tweening between two values of a given property)
* animations (where you define keyframes to chain a series of transitions, and repeat them, if you want)

I'll go through each of the points you've seen, and if anything is unclear, please stop me, and I'll find another way to explain it.

## clip-path

For clip-path, you saw how to:
* create circles and ellipses
* with specific centres and radiuses
* You saw that the default values place the circle or the ellipse nicely inside the element that it is applied to
* I used `%` units, in order to place the circles and ellipses with respect to the current element, but you can use other units as required.
* I applied the `clip-path` to an image, a `<p>` element and to the `<body>`, so you know that it can work with any container.
* I also demonstrated `inset`, to remove the edges of an element.

And I promised to show you `polygon` clip-paths, which we will see in a moment.

## transition

Then I showed you how you can set a different clip-path on `:hover`, and how you can apply a transition, so that the change happens gradually over time.

* You saw how some properties (like `display` and `background-image`) cannot be animated, so they happen immediately.
* You saw how others (like `visibility`) have no intermediate steps, so they are applied all at once at the end of the transition.
* You saw how you can use the same transition values on several properties at once...
* ... and how you can set the values differently for different properties.

## animation

Then I showed you how to use animations keyframes to simulate a bouncing ball.
* Animations are defined by `@keyframe` at-rules
* Inside an @keyframe rule, you define separate keyframes at percentage time points
* The browser will perform a smooth transition for each of the properties that change between two keyframes
* I didn't show it to you, but for each element to which you apply an animation, you can set different values, so that you create variations on the same animation. You'll find an animation with two different balls in the ClassBook repository.

# Two more things

There are two more things I want to show you: `clip-path: polygon()` and the `steps()` `-timing-function`.

## polygon

Let's go back to the project with the Lion that I showed you this morning. I created a `clip-path` that showed just the lion's eye. When you hover over the eye, the entire image is revealed. To hide the entire image, I had to move my cursor off the image entirely.

I'm now going to show you how to make a `clip-path` with a hole in it, and I'll apply that to a `div` just in front of the lion image, with the hole around the eye. When the cursor moves off the eye, it will moves out of the hole, onto the `div` itself.

Let's start by showing the entire lion image.

`  /* clip-path: circle(5% at 55% 39%); */`

And I'll create a `div` in the HTML file.

`    <div class="lion"></div>`

For simplicity, I'll positon both the `img` and the `div` with absolute, at the top left...

```html
img {
  position: absolute;
  top: 0;
  left: 0;
  <!-- ... -->
}

div {
  position:absolute;
  top: 0;
  left: 0;
  width: 100vmin;
  height: 100vmin;
  background-color: red;
  opacity: 0.5;
}
```
... and I'll place the `div` directly on top of the lion.

Now I'll create a polygon clip-path.

Remember that the eye of the lion is centred at 55% 39%, and its radius is 5%. I can create a square that fits neatly around the circle if I start 5% to the left and 5% above the centre, and make corners that are 5% to the right and 5% below. I create each corner as a horizontal % from the left and a vertical percentage from the top.

```css
div {
  /* ... */

  clip-path: polygon(
    50% 34%,
    60% 34%,
    60% 44%,
    50% 44%
  )
}
  ```
Do you see how, after the third point of my polygon, I have a triangle, and after the fourth I have square.

I've created 4 points, and the polygon automatically closes the last side.

But this is not a hole. I want a hole. So I'm going to make my polygon reach out from this square to the edge. I don't stop at 50% from the left, I go all the way to the left: `0%` or `0`...

```css
div {
  /* ... */
  clip-path: polygon(
    50% 34%,
    60% 34%,
    60% 44%,
    0% 44%,
    0 100%,
    100% 100%,
    100% 0,
    0 0,
    0 43%,
    50% 43%
  )
}
```
... and now I create more points, one at each corner. Notice how, when the line from the last point I created crosses another line, I get a sort of pretzel, or bow-tie effect. Only the area within the lines is included.

So as I continue, my original red square turns inside out, as it were, and becomes a transparent hole.

And back to where I created the first point on the left edge. Or almost, so that you can see the join.

Let me close it completely (`43% => 44%`).

And I'll apply the `clip-path: circle()` to the lion image again.

Now when I move the mouse over the circle, with the square hole around it, the `clip-path` expands nicely, and when I move the mouse out of the square hole, over onto the red `div`, my mouse is no longer `:hover`ing on the lion image; it's `:hover`ing on the red `div`, so the lion`s big `clip-path` collapses again.

I can remove the `background-color` for the `div`, but it continues to block the `:hover` from the lion image.

# Exercise

You'll find the code I've just shown you in the CourseBook repository, in a folder with today's date.

And you'll find an exercise that allows you to practise for yourself:
* Creating a polygon `clip-path` with a hole in it
* Detecting a `:hover` on a clipped image
* Transitioning to show the whole image
* Making the mouse stop hovering over the clipped image if it moves outside the hole in `<div>` that is its next adjacent sibling.
* In a word: creating the game I showed you at the beginning.

## steps()

But before you do that exercise, there's just one more little thing that I'd like to show you: using `steps()` in an animation to imitate a typewriter.

This is what it will look like.

[Demo]

Basically, there is text in a `<p>`aragraph element, and its width is initially set to 0. A set of keyframes in a  `@keyframe` at-rule widens the paragraph one letter at a time, using the `steps()` `-timing-function`. Then there is a pause, and then the animation continues back to its starting point.

You'll also notice that there is a blinking insertion point. That is a separate animation.

Starting with my standard boilerplate HTML, I create two paragraphs:

```html
    <p class="screenplay">Screenplay: Tom Stoppard</p>
    <p class="music">Music: Tom Jones</p>
```

In the CSS, I'll make the text look good. I'll use a monospace font, so that all the letters are exactly the same width. You are used to `em` units for measuring the size of text, based on its height. There is also a much less common `ch` unit, which measures the space required for the "0” (zero) character. In a monospace font, all characters are exactly `1ch` wide.

```css
body {
  background-color: black;
  font-size: 6vw;
  color: green;
  font-family:'Courier New', Courier, monospace
}
```

I want the text to appear all in a single line, even when the width of the `p`aragraph is small. There's a property called `white-space` that I can set to `nowrap`, so there will be no line breaks. If I set the width of the `p` to `1ch` and give it a dark-but-not-black background-color, then I can show you from the Elements Inspector what will happen when the width of the `p` changes:

```css
p {
  white-space: nowrap;
  width: 1ch;

  background-color: #333;
}
```

But I don't want to see any characters outside the current width:

`  overflow: hidden`

How many letters in the first line? At full width: `24ch`

I'll create an animation which changes the width from 0 to `24ch`...

```css
@keyframes typewriter {
  0% {
    width: 0;
  }

  100% {
    width: 24ch;
  }
}
```

... and I'll set the animation for the first `p` to use this animation in 24 steps...

```css
p.screenplay {
  animation: typewriter 6s steps(24);
}
```

Notice that when it gets to the end, it goes back to beginning.

Let me make it take only half the time to reach full width, and then pause there:

```css
@keyframes typewriter {
  0% {
    width: 0;
  }

  50% {
    width: 24ch;
  }

  100% {
    width: 24ch;
  }
}
```

And let me force it to go back to the beginning after the pause:

```css
@keyframes typewriter {
  0% {
    width: 0;
  }

  50% {
    width: 24ch;
  }

  90% {
    width: 24ch;
  }

  100% {
    width: 0;
  }
}
```

I'll set its initial width to 0, so that it remains "empty" when the animation is over.

What about the "music" animation. There are only 16 characters to type, so I don't want the `p` element to get so wide. What if I use a CSS custom property?

```css
p.screenplay {
  --width: 24ch;
  animation: typewriter 6s steps(24);
}

p.music {
  --width: 16ch;
  animation: typewriter 4s steps(16) 6s;
}


@keyframes typewriter {
  0% {
    width: 0;
  }

  50% {
    width: var(--width);
  }

  90% {
    width: var(--width);
  }

  100% {
    width: 0;
  }
}
```

And I don't want the music animation to take so long. Four seconds should be enough.

And I want the screenplay animation to finish before the music animation starts, so I can add a delay to the music animation: 6s.

Ad n
