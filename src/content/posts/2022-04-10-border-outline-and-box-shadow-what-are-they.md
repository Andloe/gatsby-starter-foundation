---
template: blog-post
title: "Border, Outline and Box-Shadow, What Are They? "
slug: border
date: 2022-04-10 19:03
description: border
featuredImage: /assets/steven-ramon-odbodeqvf2q-unsplash.jpg
---
<!--StartFragment-->

In this article we'll discuss three important CSS methods that everyone should know. First we'll start with border, then outline, and finalize with box-shadow. The objective of this article is to find out what each of this terms are, what are they for, and how could we use it. 

# Border Property

The border property is one of the "shorthand properties" defined by CSS and used to shorthand set the value of one or more individual properties. In this case, it is one of the most complete shorthand properties, since it allows you to set up to 12 properties simultaneously. 

The border property is used to set the same thickness, style and/or width of all the borders of an element. Unlike the margin and padding properties, with the border property it is not possible to specify different values for each of the four borders. 

As it is one of the most flexible properties in CSS, its definition seems complicated, especially when it comes to the allowed values "any or all of the following values and in any order". 

The most common use of border is to simultaneously set the thickness, style, and color of an element's border: 

![](/assets/screenshot-2022-04-10-192947.png "ex1")

The following example shows three different ways to set the same border to an element: 

/\* Using the "border" shorthand property \*/ 

`div { `

`  border: 1px solid #C00; `

`} `

/\* Using the shorthand properties of each border \*/ 

`div { `

`  border-top: 1px solid #C00; `

`  border-right: 1px solid #C00; `

`  border-bottom: 1px solid #C00; `

`  border-left: 1px solid #C00; `

`} `

/\* Using the simple properties of each edge \*/ 

`div { `

`  border-top-width: 1px; `

`  border-top-style: solid; `

`  border-top-color: #C00; `

`  border-right-width: 1px; `

`  border-right-style: solid; `

`  border-right-color: #C00; `

`  border-bottom-width: 1px; `

`  border-bottom-style: solid; `

`  border-bottom-color: #C00; `

`  border-left-width: 1px; `

`  border-left-style: solid; `

`  border-left-color: #C00; `

`} `

At best, the border property is equivalent to 12 simple properties. Also, as with all shorthand type properties related to borders, the order in which the values are indicated does not matter: 

`div { border: 1px solid #C00; } `

`div { border: solid 1px #C00; } `

`div { border: #C00 1px solid; } `

`div { border: #C00 solid 1px; } `

# Outline Property

The outline property is one of a number of CSS-defined "shorthand properties" that are used to shorthand the value of one or more individual properties. In this case, it is used to set the same thickness, style, and/or width for all profiles of an element. 

Although it is true that it has many similarities with the border property, in reality they differ in some very important aspects: 

Outlines do not take up space, while normal borders do. 

Outlines can have non-rectangular shapes. 

From a design point of view, the first feature is the most important. Outlines are always drawn "above the element", so they do not modify the position or the total size of the elements. 

The following example shows two boxes; the first shows a very thick border and the second shows an outline of the same width: 

![](/assets/screenshot-2022-04-10-193626.png "ex2")

The outline of the second box is drawn just outside its edge. Although visually it doesn't look like it, the outline and the edge are not in the same plane. In this way, the profile is not taken into account to calculate the total width of an element and does not influence the rest of the nearby elements. 

The outline property does not require the three properties that define the style of the outlines to be indicated. If no property is specified, its value is obtained using the default value of that property. 

In the following example, only the style of the outline is indicated, so the browser automatically assigns the medium value to its thickness and the color is chosen so that it has the maximum contrast with the background of the page: 

![](/assets/screenshot-2022-04-10-193818.png "ex3")

The following example ignores the outline thickness, so the browser automatically sets it to medium: 

![](/assets/screenshot-2022-04-10-193912.png "ex4")

 

The thickness of the profile can be set in any of several ways to indicate a measurement in CSS. The color can also be set in any of the different ways of indicating a color in CSS, with the particularity of the invert value that selects the color that has the most contrast with the background color. Finally, the outline style is set to the same values as those used in the border-style property. 

# Box-Shadow

The CSS3 box-shadow property is used to cast one or more shadows on an element. Pretty much any element can get a shadow using this property. 

Box-shadow allows you to easily implement multiple shadows (outer or inner) on elements by specifying color, size, blur, and offset values. 

The syntax would be something like this: 

`.shade { `

`box-shadow: 5px 5px 5px 1px #ccc; `

`} `

1. The first value corresponds to the horizontal displacement of the shadow. A positive number means the shadow will be to the right of the box, a negative value will make the shadow appear to the left of the box. 
2. This is the vertical offset of the shadow. As before, a negative value means the shadow will be above the box while a positive value means the shadow will be below the box. 
3. The third parameter corresponds to the blur radius and is optional. If the value is 0, the shadow will be very strong. The higher the number, the blurrier it will be. 
4. The propagation radius (also optional). Positive values increase the size of the shadow, negative values decrease the size. The default value is 0. 
5. This last attribute simply corresponds to the color of the shadow. 

Other shadow examples… 

## Inner Shadow: 

`.innerShadow { `

`box-shadow: inset 0 0 10px #000000; `

`} `

## One side only: 

This is my favorite. Using a negative spread radius, we can "squeeze" the shadow and direct it onto only one side of the box. 

`.singleside { `

`box-shadow: 0 8px 6px -6px black; `

`} `

That's the basics to know for now. 

There are thousands of ways to experiment with these shadows and the other two methods we just discussed. 

<!--EndFragment-->