---
title: Intro to CSS
nav_order: 11
---

# Intro to CSS

## What is CSS?

CSS stands for Cascading Style Sheet.
It describes how HTML elements are to be displayed on different screens and in print.
It works on top of the HTML and makes use of the tree-structure of the HTML documents.
The HTML elements inherit stylistic properties through CSS.
Helps us add colors, sizes, order, position, hiding, showing, animatin etc.

### How do we write CSS?

Here is a very basic CSS style:

```css
h1 {
    color: red;
}
```

### Explaining the structure

Explaining the structure of CSS styles:

```
selector {
    property: value;
}
```

- The **selector** points to the HTML element you want to style
- The declaration block (within the curly braces) contains one or more declarations separated by semicolons.
- Each declaration includes a CSS **property** name and a **value**, separated by a colon.
Find full list of CSS Properties [here](https://meiert.com/en/indices/css-properties/).
- `red` - this is one way of defining color in CSS. This is called a `named color`. [Here](https://css-tricks.com/snippets/css/named-colors-and-hex-equivalents/) is a full list of named colors that CSS understands. CSS also understands hex values like `#ff0000`, and rgb(255, 0, 0);
- A CSS declaration **always** ends with a semicolon.
- So in sumarry, it reads like: If this condition is true, then apply this/these style(s).

### Another example
```css
h1 {
    /*
     *  Note px is a unit of measurement in CSS.
     *  Other units will be covered later
     */
    font-size: 60px;
}
```

### Where to put your styles

- Inline
- Style tag
- CSS File

Show how they override one another with the h1 color style above. Inline has the highest preference.

### Parent, Children, Sibling, Ancestor, Descendant
- An element that directly contains other elements is a **parent** of the elements that it contains.
- An element that is directly contained within another element is a **child** of the element that contains it.
- Elements are **sibling elements** if they share the same parent element.
- An element that contains (at any level) other elements is an **ancestor** of the elements that it contains.
- An element that is contained (at any level) within another element is a **descendant** of the element that contains it.

More details [here](http://www.littlewebhut.com/css/info_element_relationships/)

#### Example

```html
    <div>
        <h1>Museums in Berlin</h1>
        <div>
            <p>I am a paragraph!</p>
        </div>
    </div>
```

```css
    div {
        color: blue
    }
```

The `p` will be colored blue.

## CSS at work

Here is the [Museum's page](./museums.html) example. Let's do some really basic styling.

Teacher's Note: Apply styles on live editor.

- `color: #FF9900;`. This is an hex value. Another way to set color is rgb.
- `text-align: center;` (can be center, right, justify)
- `font-family: Helvetica` (Explain a bit about [web-safe fonts](https://web.mit.edu/jmorzins/www/fonts.html)). Also explain listing backup fonts example below
- `font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;`
- `font-size: 16px;` (px, em, rem, %)
- `font-weight: bold;` (normal, bold)
- `font-style: italic;` (normal, italic)
- `font` - This is a CSS Shorthand property.
- `border-width: 3px;`
- `border-style: solid;`
- `border-color: pink;`
- `border: 3px solid pink;` This is a CSS Shorthand property.
- `background-color: #660000;`
- `background-image: url()`


## Comments
```
h1 {
    /* this is a comment */
    color: #0066CC;
}
```

## Some sources for colors

- [Coolors.co](https://coolors.co/)
- [Color-hex.com](https://www.color-hex.com/color-palettes/)
- [Colorsupplyyy.com](https://colorsupplyyy.com/)

**Learn more**:

- [W3Schools: CSS Syntax and Selectors](https://www.w3schools.com/css/css_syntax.asp)
- [W3Schools: CSS Colors](https://www.w3schools.com/css/css_colors.asp)
