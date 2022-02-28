---
template: blog-post
title: "Everything You Need to Know About CSS Custom Properties, Fluid
  Typography and :Where() And :Is() Pseudo Classes "
slug: /article3
date: 2022-02-27 18:38
description: Everything You Need to Know About CSS Custom Properties, Fluid
  Typography and :Where() And :Is() Pseudo Classes
featuredImage: /assets/thisisengineering-raeng-8hgmg03spf4-unsplash.jpg
---
# CSS Custom Properties

![custom](/assets/kobu-agency-iparhaxetrk-unsplash.jpg "custom")

<!--StartFragment-->

CSS Custom Properties (also called CSS variables) allow us to define names for certain values of the properties. This way, that name can be used as if it were a variable. The big advantage is that changing the value of these "variables" automatically changes them everywhere in the CSS document where that name has been used. 

## Defining Custom Properties 

To define a custom property we will put two hyphens -- in front of the name we want to use. To define the custom property for the entire HTML document, we'll include it in the :root pseudo-element. Example:

`:root { `

`   --main-color: black; /* Custom value */ `

`   --font: "Arial"; `

`} `

## Using Custom Properties

To use a custom property, its name must be inserted into the `var()` expression: 

`.class { `

`   background-color: var(--main-color); `

`   font-family: var(--font); `

`} `

<!--EndFragment-->

# Fluid Typography 

![fluid](/assets/christopher-farrugia-80tmagtp3yi-unsplash.jpg "fluid")

<!--StartFragment-->

Nowadays, we see that websites are fluid and/or dynamic, which means that the content of the page adapts to the size of the window where the website is being visited. Therefore, fluency and dynamics are very important factors in the development of a website. 

What we know and must keep in mind is that the user must be offered a quality website with a good design. One important aspect is fluid typography, CSS allows us to create fluid typography that contributes to the overall fluency of our site/s. Fluid typography means that our font adapts to the size of the window. We can argue that we already had the control over that font aspect with “Font-size” in which we can give the font a percentage of size and that it is proportioned in the page, however, there are times when this property is not required or useful, as it sometimes misses the designer's intent. 

That is why there are now other units that we can add to the typography of our website, which will help us to: 

1. Not have to classify the sizes of the fonts depending on the size of the device where the website is consulted. 

2. Adjust the text directly to the size of the viewport or the window as such. 

The “Font-size” will continue to be used, the only thing we will change is the units of measure with which our font will be scaled. There is good browser support, as shown: 

Some of these units are `“vh”, “vw” ,”vmin”,”vmax”`. 

In addition to the aforementioned, CSS offers us a function that is determined by a trend between the dispersion of text sizes on a website, which helps us to make the value to which the size is scaled a little more precise, this function is `calc()`, which is also well supported by the browser. 

<!--EndFragment-->

# The :where() and :is() Pseudo Classes 

![classes](/assets/valery-sysoev-p9okl4yw3c8-unsplash.jpg "classes")

<!--StartFragment-->

CSS keeps evolving - will it ever stop? -, and some of its latest features can end certain debates, such as if CSS is considered a [coding language](https://css-tricks.com/is-css-a-programming-language/). Two of these features are the functional pseudo-class selectors `:is()` and `:where()`. These are features that can have a significant impact on the way you write CSS. 

In this section we'll look at some examples of `:is()` and `:where()`, and how they can improve and simplify your style sheets. 

But first, we need to know some definitions…. 

## What is a CSS pseudo-class? 

"A CSS pseudo-class is a keyword added to a selector that specifies a special state of the selected elements." An example is the pseudo-class “:hover” which you can use to change the color of a button when the user's pointer passes over it. 

## What Is a CSS selector? 

A CSS selector is the first part of a CSS rule. You use a selector to tell the browser which HTML elements should be selected for the CSS property values within the rule to apply to them. 

## What is Specificity in CSS? 

Specificity is the means by which browsers decide which CSS property values are most relevant to an element. It is based on matching rules that are made up of different types of CSS selectors. 

## The :is() And :where() Selectors 

`:is()` and `:where()` are functional pseudo-class selectors that function as dynamic function calls at runtime. This functionality, which improves readability, allows you to write CSS, grouping elements in the middle, at the beginning or at the end of a selector. 

Regarding grouping, whatever `:is()` does, `:where()` can also do, anywhere in the selector, by nesting or stacking. 

## What Is the Difference Between :is() And :where()? 

`:is()` and `:where()` diverge at the level of specificity. The following are some of the differences: 

* `:where()` has no specificity 
* `:where()` 'squashes' all specificity in the selector list passed as functional parameters 
* `:is()` takes the specificity of its most specific selector 

### Examples

If you want to know which parts of your code could benefit from `:is()` or `:where()`, you should look for selectors with multiple commas and selector repetition. Here are some examples: 

`h1 > span, h2 > span, h3 > span, h4 > span, h5 > span, h6 > span { font-weight: initial; } `

could you write as 

`:is(h1,h2,h3,h4,h5,h6) > span { font-weight: initial; } `

or 

`:where(h1,h2,h3,h4,h5,h6) > span { font-weight: initial; }`

As you can see, readability improves quite a bit. 

As you have seen, the `:is()` and `:where()` pseudo-selectors allow you to have a feature that helps you group, have smaller style sheets, and remove commas from your code. 

<!--EndFragment-->