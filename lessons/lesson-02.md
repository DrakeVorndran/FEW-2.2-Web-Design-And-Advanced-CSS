# FEW 2.2 - Advanced CSS - Animation

Making things move.

## Why you should know this

Engagment is important. Things that move are much more interesting. Adding motion adds another dimention to your content. All of your favorite apps probably have little bits of animation. 

## Learning Objectives (5 min)

1. Describe easing
1. Use CSS transition and keyframes to make things move
1. Control and define the time and easing for elements that move

## Initial Exercise

Animation is everywhere on the computer. Even your code editor has some animation. 

Explore some CSS animations

1. https://codepen.io/FabioG/full/QjLreK
2. https://codepen.io/dsenneff/pen/2d338b0adf97472ebc5d473cf1fa910b
3. https://codepen.io/donovanh/full/pvMeeB
4. https://codepen.io/yoannhel/full/sJpDj
5. https://codepen.io/Manoz/full/pydxK
6. https://codepen.io/Venerons/full/BvHbK
7. https://codepen.io/MarioDesigns/full/woJgeo
8. https://codepen.io/u1tralord/full/pvXwza
9. https://codepen.io/Zaku/full/YjRqzB
10. https://codepen.io/pcameron/pen/rVmera
11. https://codepen.io/valhead/full/rfump
12. https://codepen.io/stefcharle/full/Gydvbx
13. https://codepen.io/nathantaylor/full/PJGqdE
14. https://codepen.io/oliviale/full/jxPgKv
15. https://codepen.io/antho-fsy/pen/wJqWKj

What is happening in these animations? Don't worry about the technical details just _identify what is moving_ and _how is it moving_.

## Making things move

There are a couple ways to make things move with CSS. 

- `transition`
- `@keyframe`

In a nutshell `transition` causes chnages to CSS properties to chnage over time rather than instantly, `@keyframe` defines changes that are mapped out over time. 

### Transition

```CSS
.a {
  width: 100px;
  height: 100px;
  background-color: #f00;
  /* Sets the time to apply changes to this element */
  transition: 400ms;
  /* s = secs ms = milliseconds  */
}

.a:hover {
  /* These changes occur over the transition time */
  transform: scale(1.25) rotate(12deg);
}
```

The base rule declares a transition of 400 milliseconds. The hover rule changes the scale and rotation. Rather than happening immediately the change takes 400 milliseconds.

https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions

### Keyframes

To create keyframe animations define some keyframes. A key frame describes the values for CSS properties at a point in time. 

Give animation a name, `scaleAndRotate` in the example below. 

Define the value for properties along the length of the animation. Here `transform: scale(0.5) rotate(0)` happens at the beginning `0%`, `background-color: blue` happens at the half way point `50%`, and `transform: scale(1.0) rotate(23deg)` happens at the end of the animation `100%`.
```CSS
@keyframes scaleAndRotate {
  0% {transform: scale(0.5) rotate(0);}
  50% {background-color: blue}
  100% {transform: scale(1.0) rotate(23deg)}
}
```

The code above defines the animation. Below the animation is applied to an element. 

The `animation` property applies an animation to an element. The line: `animation: scaleAndRotate 5s infinite` sets the animation to `scaleAndRotate` (matches the name above), sets the length of the animation 5 secs (`5s`), and repeat infinitely (`infinite`).

```CSS
div {
  width: 100px;
  height: 100px;
  background: red;
  position :relative;
  animation: scaleAndRotate 5s infinite;
}
```

The animation property is the shorthand property for: 

- animation-delay
- animation-duration
- animation-fill-mode
- animation-iteration-count
- animation-name
- animation-play-state
- animation-timing-function

The code above could be broken into three lines: 

```CSS
animation-name: scaleAndRotate;
animation-duration: 5s;
animation-iteration-count: infinite;
```

## Easing 

Easing describes the change in rate of motion. When things speed up, think a car starting from a stop sign, we say they are easing in. When things slow down, think a car slowing as it reaches a stop sign, we say they are easing out. 

Everythin in the real world eases in or eases out. You should always apply easing. This will give your motion character and make it more realistic and interesting to watch. 

Play around with: https://developer.mozilla.org/en-US/docs/Web/CSS/animation-timing-function

## Making things move with CSS

Pair up with someone you haven't paired with in class before and take a look at these tutorials. The idea is to find some things you can incorporate into your logo/icon. 

- https://css-tricks.com/almanac/properties/a/animation/
- https://thoughtbot.com/blog/css-animation-for-beginners

## Animate your CSS Logo

Add some motion to your logo/icon from class 1. Keep the motion simple. 

It's easiest to use `transition` for interactive animations on hover or click and keyframes for a cycling animations or complex animations.

## Wrap Up

- Continue working on your current tutorial
- Complete reading
- Complete challenges

## Additional Resources

1. https://css-tricks.com/almanac/properties/a/animation/
1. https://www.mockplus.com/blog/post/css-animation-examples
1. https://uicookies.com/css-animation-examples/
1. https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions
1. https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations

## Minute-by-Minute [OPTIONAL]

| **Elapsed** | **Time**  | **Activity**              |
| ----------- | --------- | ------------------------- |
| 0:00        | 0:05      | Objectives                |
| 0:05        | 0:15      | Overview                  |
| 0:20        | 0:45      | In Class Activity I       |
| 1:05        | 0:10      | BREAK                     |
| 1:15        | 0:45      | In Class Activity II      |
| TOTAL       | 2:00      |                           |
