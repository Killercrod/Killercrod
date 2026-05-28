** CSS
In this markdown we are going to talk about the basics of CSS and how to use it to style your webpages.

By the end of this guide you will be able to:
- Understand what CSS is used for
- Read the basic structure of a CSS file
- Practice the first things you should learn before moving on

This guide is for people who are new to CSS, or for people who want a simple refresher without too much technical language.

First, we need to understand when we use CSS. We use CSS when we want to make our webpage look better. HTML gives the structure, and CSS gives the style. It is a good idea to keep both parts separate so the project stays organized.

## Before You Start

You do not need to know everything before learning CSS. It is enough to:

- Know the basics of HTML
- Understand that CSS changes how things look
- Be comfortable with practice and repetition
- Not be afraid of mistakes, because they are part of learning

## Basic Structure

This is the basic structure of a CSS file. It is important to know why it is written like this.

```css
/* Hello World style */
body {
	background-color: white;
	color: black;
}

/* Comments */
/* Single-line or multi-line comment */
```

I will explain why it is written like this and why it is important to know this.

** body
This is the selector.
Why is it necessary? It tells CSS which HTML element you want to style.

** background-color and color
These are properties.
Why are they necessary? They tell CSS what part of the element should change.

** white and black
These are values.
Why are they necessary? They tell CSS which exact style to apply.

** Comments
Comments help you write notes inside your code.
Why are they useful? They make code easier to understand when you come back later.

## CSS in Simple Words

CSS is like the clothes and decoration of your webpage.

- HTML is the structure
- CSS is the style
- JavaScript is the behavior

That is the easiest way to think about it.

## How CSS Connects to HTML

Usually, CSS is connected to HTML with a link tag inside the head.

```html
<link rel="stylesheet" href="style.css">
```

Why this matters:

- It keeps the code organized
- It lets you reuse styles
- It is easier to maintain than putting everything in the HTML file

## Selectors

Selectors tell CSS what you want to style.

```css
/* Element selector */
p {
	color: blue;
}

/* Class selector */
.box {
	padding: 10px;
}

/* ID selector */
#title {
	font-size: 24px;
}
```

Simple way to remember them:

- Element selector targets all elements of that type
- Class selector can be used many times
- ID selector is usually for one specific element

## Variables, Properties, and Values in Simple Words

In CSS, properties are the things you want to change. Values are the exact style you want to apply.

For example:

- `color` is the property
- `blue` is the value

Think of it like this:

- Selector = what you want to style
- Property = what you want to change
- Value = how you want it to look

## Common Properties

```css
p {
	color: #333;
	background-color: #f5f5f5;
	font-size: 16px;
	font-family: Arial, sans-serif;
}
```

Some common things you will use a lot:

- color
- background-color
- font-size
- font-family
- margin
- padding
- border

## The Box Model

Every element in CSS can be seen like a box.

- Content is the inside text or image
- Padding is the space inside the box around the content
- Border is the line around the box
- Margin is the space outside the box

```css
.card {
	padding: 20px;
	border: 1px solid black;
	margin: 10px;
}
```

If you understand the box model, CSS becomes much easier.

## Typography

Typography is how your text looks.

```css
h1 {
	font-size: 32px;
	font-weight: bold;
}

p {
	line-height: 1.5;
	text-align: left;
}
```

Why this matters:

- It makes text easier to read
- It helps you create hierarchy
- It gives your page a cleaner look

## Colors and Backgrounds

```css
body {
	background-color: #ffffff;
	color: #222222;
}

.button {
	background-color: #0077ff;
	color: white;
}
```

If you want a simple way to remember it:

- color changes the text
- background-color changes the background

## Display and Layout Basics

Some elements behave differently on the page.

```css
.block {
	display: block;
}

.inline {
	display: inline;
}

.flex-container {
	display: flex;
}
```

Simple idea:

- Block elements take full width
- Inline elements stay inside the text flow
- Flex helps organize items more easily

## Flexbox

Flexbox is one of the easiest modern ways to place items on a page.

```css
.container {
	display: flex;
	justify-content: space-between;
	align-items: center;
}
```

Why people like Flexbox:

- It helps arrange items in rows or columns
- It makes alignment easier
- It is very useful for modern layouts

## Responsive Design

Responsive design means your webpage looks good on different screen sizes.

```css
@media (max-width: 768px) {
	.container {
		flex-direction: column;
	}
}
```

Why this is important:

- People use phones, tablets, and computers
- Your page should adapt to different screens
- A good layout should not break on mobile

## Pseudo-classes

Pseudo-classes let you style elements in special states.

```css
a:hover {
	color: red;
}

button:focus {
	outline: 2px solid blue;
}
```

Simple idea:

- hover means when the mouse is over it
- focus means when the element is selected

## Basic Exercises

1. Change the color of a heading.
Expected result: Your heading should show in a different color.

2. Add padding and margin to a box.
Expected result: The box should have more space inside and outside.

3. Style a button with a background color and text color.
Expected result: The button should look different from normal text.

4. Create a simple card and center its content.
Expected result: The card should look clean and organized.

5. Add a media query that changes the layout on small screens.
Expected result: Your layout should adapt when the screen gets smaller.

## Common Beginner Mistakes

- My CSS is not applying.
Check if the link tag points to the correct file.

- My selector does not work.
Check if you used the correct class name, ID, or element name.

- My styles look strange.
Check if there is another style overriding your rule.

- My page looks bad on mobile.
Check if you added responsive styles.

- My spacing does not work.
Check the difference between margin and padding.

## What to Learn Next

- CSS syntax basics (practice with small styles)
- Box model in more depth
- Flexbox and grid layouts
- Responsive design with media queries
- Colors, fonts, and spacing
- Styling full web pages

## Key Points to Remember

- HTML gives structure
- CSS gives style
- Selectors tell CSS what to change
- The box model is very important
- Flexbox helps with layout
- Responsive design matters a lot
- Practice is the best way to learn CSS

This guide covers the essential CSS concepts. Keep practicing and referring to the official CSS documentation for more detailed information.
