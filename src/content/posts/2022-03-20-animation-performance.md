---
template: blog-post
title: A Glance at CSS Animations & Performance
slug: /cssanimations
date: 2022-03-20 19:41
description: css animations and performance
featuredImage: /assets/shubham-dhage-pacwvlrnzj8-unsplash.jpg
---
<!--StartFragment-->

CSS animations allow you to do simple animations without any JavaScript at all. JavaScript can be used to control CSS animation and enhance it with a bit of code. 

## CSS Transitions 

The idea of CSS transitions is simple. We describe a property and how its changes should be animated. When the property changes, the browser paints the animation. 

That is: all we need is to change the property, and the smooth transition will be done by the browser. 

For example, the CSS below animates background-color changes for 3 seconds: 

`.animated { `

`   transition-property: background-color; `

`   transition-duration: 3s; `

`} `

Now, if an element has the .animated class, any background-color change is animated for 3 seconds. 

Click the button below to animate the background: 

<figure>
<iframe height="300" style="width: 100%;" scrolling="no" title="Button Color Changing Animation" src="https://codepen.io/andloe/embed/rNLvBqE?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/andloe/pen/rNLvBqE">
  Button Color Changing Animation</a> by Andloe (<a href="https://codepen.io/andloe">@andloe</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>
</figure>

There are 4 properties to describe CSS transitions: 

transition property 

transition duration 

transition timing function 

transition-delay 

Transition allows you to declare them together in order: property duration timing-function delay, and also to animate multiple properties at once. 

For example, this button animates both color and font-size: 

<figure>
<iframe height="300" style="width: 100%;" scrolling="no" title="Button Animation Font Size and Color" src="https://codepen.io/andloe/embed/LYeZWKP?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/andloe/pen/LYeZWKP">
  Button Animation Font Size and Color</a> by Andloe (<a href="https://codepen.io/andloe">@andloe</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>
</figure> 

## Performance 

Most CSS properties can be animated, because most contain numeric values. For example width, color, font-size are all numbers. When we animate them, the browser gradually changes these values gram by gram, creating a smooth effect. 

However, not all animations will look as smooth as you'd like, because different CSS properties require more or less resources to change. 

In more technical details, when there is a style change, the browser goes through 3 steps to render the new view: 

Layout: (diagram) recalculates the geometry and position of each element, then. 

Paint: (draws) recalculates how everything should look in its places, including background, colors, finally. 

Composite: (render) displays the final result in screen pixels, applying CSS transformations if they exist. 

During a CSS animation, this process is repeated for each frame. However CSS properties that never affect geometry or position, such as color, can skip the “Layout” step. If a color changes, the browser doesn't recalculate geometry, it goes to Paint → Composite. And there are a few properties that jump right into “Composite”. 

Calculations can take a while, especially on pages with many elements and complex layout. And lags can be noticeable on many devices, causing jitter: jerky, less-smooth animations. 

The animation of properties that skip the "Layout" step are faster. Much better if the “Paint” step is skipped as well. 

The transform property is a great option because: 

CSS transform affects the target element as a whole (rotate, flip, stretch, shift). 

CSS transform never affects neighboring elements. So the browsers apply transform “above” the already calculated “Layout” and “Paint”, in the “Composite” step. 

In other words, the browser calculates the layout in the Layout stage (sizes, positions); you draw it with colors, backgrounds, etc., in the “Paint” stage; and then apply transform to the elements that need it. 

Changes (animations) of the transform property never trigger the Layout and Paint steps. Furthermore, the browser delegates CSS transformations to the graphics accelerator (a special chip on the CPU or graphics card), making them very efficient. 

Fortunately, the transform property is very powerful. Using transform on an element, you can rotate it, flip it, stretch or compress it, offset it, and much more. So instead of the left/margin-left properties we can use `transform: translateX(...)`, or use `transform: scale` to increase its size, etc. 

The opacity property also doesn't trigger “Layout” (it also skips “Paint” in Mozilla's Gecko). We can use it for show/hide or fade/fade effects. 

Pairing transform with opacity can usually solve most of our needs by providing nice and smooth animations. 

## Limitations 

CSS animations allow you to animate, smoothly or in steps, changes to one or more CSS properties. 

They are good for most animation tasks. We can also use JavaScript for animations.  

There are some limitations of CSS animations compared to JavaScript animations: 

+ Simple things done simply. 

+ Fast and light on the CPU. 

\- JavaScript animations are flexible. They can implement any animation logic, such as an "explosion" of an element. 

\- Not just property changes. We can create new elements in JavaScript for animation purposes. 

In the examples in this article we animate `font-size`, `color`, etc. In real life projects it is preferable to use `transform: scale()` and transform: `translate()` to get better performance. And the `transitionend` event allows JavaScript to be executed after the animation, so it integrates nicely with your code. 

Most animations can be implemented using CSS. And the `transitionend` event allows JavaScript to be executed after the animation, so it integrates nicely with your code. 

<!--EndFragment-->