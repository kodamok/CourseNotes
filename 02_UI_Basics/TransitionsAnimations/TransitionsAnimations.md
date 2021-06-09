# Clip

Co-ordinate system



# Transitions

## Basic: `transition: 1s;`

- background-color
- transform

## Tricks

- To transition opacity, you need to transition between two colours with the same rgb and different a

## Can't animate

- Linear gradients


# Animations

* animation-name
  - none
  - ^(?!none$|initial$|inherit$|unset$)-{0,1}[A-Za-z]+[A-Za-z0-9_-]*
  - multiple names separated by commas
* animation-duration
  - Ns
  - Nms
  - default 0s
* animation-timing-function
  - ease
  - ease-in
  - ease-out
  - ease-in-out
  - linear
  - cubic-bezier
  - steps(n, `<jump term>`)
    - jump-start
    - jump-end
    - jump-both
  - step-start
  - step-end
* animation-delay
  - Ns
  - Nms
  - 0s
  - +N (waits N to start)
  - -N (starts immediately at position N)
* animation-iteration-count
  - 0
  - integer
  - floating point number
  - infinite
  - repetitions before animationend is triggered
* animation-direction
  - normal
  - reverse
  - alternate
  - alternate-reverse
* animation-fill-mode (applies to delays)
  - none
  - forward
  - backwards
  - both
* animation-play-state
  - paused
  - running

JS events
* animationstart
* animationiteration
* animationend
* animationcancel


@keyframe

from = 0%
to = 100%

shorthand:
iteration-count | direction | fill-mode | play-state | name
