---
title: CSS Selectors
nav_order: 12
---
# First, a review of last class
- In particular, the `CSS at work` section.

# CSS Selectors

The three most used CSS Selectors are the Element, the ID and the Class.

## The element selector selects elements based on the element name

```
h1 {
    color: #990000;
    border-bottom: #990000;
}
```

## The ID Selector uses the id attribute of an HTML element to select a specific element

- In HTML, you identify an element with an ID this way: `<h1 id="title">`
- In CSS, you refer to that ID using the hashtag: `#title`
- **Important rule**: there should be only one ID per page **with the same name**. There could be many IDs, but all of
them should have different names

```
<h1 id="title">Welcome to ReDI School</h1>

#title {
    color: #ffffff;
    border-bottom: #59ADC5;
}
```

## The class selector selects elements with a specific class attribute

- In HTML, you add a class to an element this way: `<ul class="nobullets">`
- In CSS, you refer to that class using a dot: `.nobullets`
- There is no limit to the number of classes per HTML file so you can have as many as you want but...if you find
yourself adding too many on one page, there's probably an easier way to do it :)

```
<ul class="nobullets">

.nobullets {
    list-style-type:none;
}
```

## Prefer classes over IDs where possible

```html
    <h1 class="bigger">Welcome to ReDI School</h1>
```

```css
    h1 {
        font-family: sans-serif;
    }

    .bigger {
        font-size:125%;
        color: #ffffff;
        border-bottom: #59ADC5;
    }
```

## IDs and Classes best practices

- ID selectors win over class selectors. So try to always use a class first.
- If you want to apply a style for all element type (e.g every `ul` on the page), you don't need to apply a class to every UL, you can, you should use the element selector `ul`.
- Take advantage of the tree structure of an HTML document: put styles on the parent in cases where those styles can be passed to the children. For example, apply the text styling to `body`, so you don't have to add it to `p`, `li` or any other element.

## !important

Explain !important. And also why it is discouraged.

## Relational selectors & Combinators

- Descendant selector
```css
    ul li {
        ...
    }
```

- Child selector
```css
    ol > li {
        ...
    }
```

## Pseudo-classes
:hover

## Nested selectors

Selectors can be nested to give you more precise control.

```
<div id="header">
    <a href="#home">Home</a>
</div>

#header a {
    color: #0066CC;
}
```

**Learn more**:

- [W3Schools: CSS Syntax and Selectors](https://www.w3schools.com/css/css_syntax.asp)
- [W3Schools: CSS Box Model](https://www.w3schools.com/css/css_boxmodel.asp)
