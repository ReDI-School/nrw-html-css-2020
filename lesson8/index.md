---
title: Intro to CSS
nav_order: 10
---

# Intro to CSS

## What is CSS?

CSS stands for Cascading Style Sheet. It describes how HTML elements are to be displayed on different screens and in print. It works on top of the HTML and makes use of the tree-structure of the HTML documents. The HTML elements inherit stylistic properties through CSS.

### How do we write CSS?

Here's a sintax example of a CSS rule:

```
selector {
    property: value;
}
```

### How does it work?

- The selector points to the HTML element you want to style
- The declaration block contains one or more declarations separated by semicolons.
- Each declaration includes a CSS property name and a value, separated by a colon.
- A CSS declaration always ends with a semicolon, and declaration blocks are surrounded by curly braces.

```
h4 {
    color: #0066CC;
    font-style: italic;
}
```

<h4 style="color: #0066CC; font-style: italic;">This is how the h4 with #0066CC color and italic font style it looks.</h4>

## Let's see CSS at work

Here is the [Museum's page](./museums.html) example. Let's do some really basic styling.

## The box model

All HTML elements can be considered as boxes. In CSS, the term "box model" is used when talking about design and layout.

The CSS box model is essentially a box that wraps around every HTML element. It consists of margins, borders, padding, and the actual content.

- **Content**: The content of the box, where text and images appear
- **Padding**: Clears an area around the content. The padding is transparent
- **Border**: A border that goes around the padding and content
- **Margin**: Clears an area outside the border. The margin is transparent

### Box elements styles

Well...every element is a box, but let's focus on `<div>`, `<ul>`, `<ol>` and also the previous text elements.

- `width: 500px;` (px, em, rem, %)
- `height: 250px;` (px, em, rem)
- `border: 5px solid #CC0000;` (px, em, rem; solid, dotted, dashed; hex, name, rgb, rgba)
- `padding: 10px 20px 10px 20px;` (px, em, rem)
- `margin: 10px auto 30px auto;` (px, em, rem)

### Here is an example

```
div {
    background-color: #eeeeaa;
    padding: 16px 24px;
    margin: 32px auto;
    border: 3px solid #00cc00;
    width:50%;
}
p {
    text-align: center;
    font-size: 24px;
    font-weight: bold;
    font-style: italic;
    color: #990000;
}
```

### The Result:

<div style="background-color: #eeeeaa; padding: 16px 24px; margin: 32px auto; border: 3px solid #00cc00; width:50%;">
    <p style="text-align: center; font-size: 24px; font-weight: bold; font-style: italic; color: #990000;">Look at me, I
    know latin! Enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
Maecenas aliquet accumsan leo. Nulla quis diam. Nullam eget nisl. Praesent dapibus. Pellentesque ipsum. Mauris tincidunt
sem sed arcu. Etiam quis quam. Nullam at arcu a est sollicitudin euismod. Aenean fermentum  risus id tortor.</p>
</div>

