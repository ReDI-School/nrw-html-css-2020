---
title: CSS Specificity
nav_order: 13
---

# CSS Specificity

Specificity is a great tool to manage the power of CSS but can be complicated. As we will see, not all selectors are
equal in "power":

- If there are two or more rules that apply to an element, the most specific selector is used
- If the two rules have equal specificity, then the latest rule is applied

Let's check this example. Which one is more important?

```
li {
    color:green;
}
li.special {
    color:red;
}
```

**What about now?**

```
li#special {
    color:green;
}
li.special {
    color:red;
}
```

**How does it works**

- Specificity determines, which CSS rule is applied by the browsers
- Specificity is usually the reason why your CSS-rules don’t apply to some elements, although you think they should
- Every selector has its place in the specificity hierarchy
- If two selectors apply to the same element, the one with higher specificity wins.
- There are four distinct categories which define the specificity level of a given selector: inline styles, IDs,
classes, attributes, and elements
- When selectors have an equal specificity value, the latest rule is the one that counts
- When selectors have an unequal specificity value, the more specific rule is the one that counts
- Rules with more specific selectors have a greater specificity
- The last rule defined overrides any previous, conflicting rules
- The embedded style sheet has a greater specificity than other rules
- ID selectors have a higher specificity than attribute selectors
- You should always try to use IDs to increase the specificity
- A class selector beats any number of element selectors
- The universal selector and inherited selectors have a specificity of 0, 0, 0, 0

**Let's take a look at how the numbers are actually calculated:**

![Specificity](specificity.png)

- If the element has inline styling, that automatically1 wins (1,0,0,0 points)
- For each ID value, apply 0,1,0,0 points
- For each class value (or pseudo-class or attribute selector), apply 0,0,1,0 points
- For each element reference, apply 0,0,0,1 point

You can generally read the values as if they were just a number, like 1,0,0,0 is "1000", and so clearly wins over a
specificity of 0,1,0,0 or "100". The commas are there to remind us that this isn't really a "base 10" system, in that
you could technically have a specificity value of like 0,1,13,4 - and that "13" doesn't spill over like a base 10 system
would.

**Let's see some very good examples**

- [CSS Specificity Wars](https://stuffandnonsense.co.uk/archives/css_specificity_wars.html)
- [CSS Bento Box](https://flukeout.github.io/)

# Pseudo-classes and pseudo-elements

## What are Pseudo-classes?

A pseudo-class is used to define a special state of an element. For example, it can be used to:

- Style an element when a user mouses over it
- Style visited and unvisited links differently
- Style an element when it gets focus

### Syntax

```css
selector:pseudo-class {
    property: value;
}
```

### A common example: Anchor Pseudo-classes

- Unvisited: a:link
- Visited: a:visited
- Mouse Over: a:hover
- Selected: a:active

### A few CSS Pseudo Classes

| Selector | Example | Description |
| --- | --- | --- |
| [:active](https://www.w3schools.com/cssref/sel_active.asp) | a:active | Selects the active link |
| [:checked](https://www.w3schools.com/cssref/sel_checked.asp) | input:checked | Selects every checked `<input>` element |
| [:enabled](https://www.w3schools.com/cssref/sel_enabled.asp) | input:enabled | Selects every enabled `<input>` element |
| [:disabled](https://www.w3schools.com/cssref/sel_disabled.asp) | input:disabled | Selects every disabled `<input>` element |
| [:focus](https://www.w3schools.com/cssref/sel_focus.asp) | input:focus | Selects the `<input>` element that has focus |
| [:hover](https://www.w3schools.com/cssref/sel_hover.asp) | a:hover | Selects links on mouse over |
| [:in-range](https://www.w3schools.com/cssref/sel_in-range.asp) | input:in-range | Selects `<input>` elements with a value within a specified range |
| [:invalid](https://www.w3schools.com/cssref/sel_invalid.asp) | input:invalid | Selects all `<input>` elements with an invalid value |
| [:first-child](https://www.w3schools.com/cssref/sel_firstchild.asp) | p:first-child | Selects every `<p>` elements that is the first child of its parent |
| [:last-child](https://www.w3schools.com/cssref/sel_last-child.asp) | p:last-child | Selects every `<p>` elements that is the last child of its parent |


## What are Pseudo-Elements?

A CSS pseudo-element is used to style specified parts of an element. For example, it can be used to:

- Style the first letter, or line, of an element
- Insert content before, or after, the content of an element

Notice the double colon notation - **::first-line** versus **:first-line**

The double colon replaced the single-colon notation for pseudo-elements in CSS3. This was an attempt from W3C to distinguish between pseudo-classes and pseudo-elements. The single-colon syntax was used for both pseudo-classes and pseudo-elements in CSS2 and CSS1.

### The ::after Pseudo-element

The **::after** pseudo-element can be used to insert some content after the content of an element. The **::before** pseudo-element insert the content before the element. Obviously.

## Learn more

- [W3Schools: Pseudo-classes](https://www.w3schools.com/css/css_pseudo_classes.asp)
- [W3Schools: Pseudo-elements ](https://www.w3schools.com/css/css_pseudo_elements.asp)
- [CSS-Tricks: A Whole Bunch of Amazing Stuff Pseudo Elements Can Do](https://css-tricks.com/pseudo-element-roundup/)
- [CSS-Tricks: Glyphs](https://css-tricks.com/snippets/html/glyphs/)
- [W3Schools: CSS Specificity](https://www.w3schools.com/css/css_specificity.asp)
- [CSS Tricks: Specifics on CSS Specificity](https://css-tricks.com/specifics-on-css-specificity/)
- [Smashing Magazine: CSS Specificity Things You Should Know](https://www.smashingmagazine.com/2007/07/css-specificity-things-you-should-know/)

