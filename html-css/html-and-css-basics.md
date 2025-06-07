# HTML and CSS Fundamentals

This file documents essential HTML and CSS theory and syntax covered during your coursework. It includes structure, formatting, styling, lists, tables, layouts, and responsive design concepts.

---

##  HTML (HyperText Markup Language)

### What Is HTML?

- Standard markup language for creating web pages
- Describes the logical structure and content
- Uses tags to format and label elements like headings, paragraphs, links, images, etc.

### HTML Document Structure

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <h1>Main Heading</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

---

## Common HTML Tags

- Headings: `<h1>` to `<h6>`
- Paragraph: `<p>`
- Line break: `<br>`
- Horizontal rule: `<hr>`
- Text formatting:
  - Bold: `<b>` or `<strong>`
  - Italics: `<i>` or `<em>`
  - Underline: `<u>`
  - Superscript: `<sup>`, Subscript: `<sub>`

---

## Hyperlinks and Images

### Links

```html
<a href="https://www.google.com">Visit Google</a>
<a href="mailto:you@example.com">Send Email</a>
```

### Images

```html
<img src="image.jpg" alt="Description" height="100" width="100">
```

### Image as Link

```html
<a href="page.html">
  <img src="icon.png" />
</a>
```

---

## Lists

### Unordered List

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

### Ordered List

```html
<ol type="A" start="2">
  <li>Second Item</li>
  <li>Third Item</li>
</ol>
```

---

## Tables

```html
<table border="1" width="50%">
  <caption>Student Info</caption>
  <thead>
    <tr><th>Name</th><th>Age</th></tr>
  </thead>
  <tbody>
    <tr><td>Alice</td><td>20</td></tr>
  </tbody>
</table>
```

- Rowspan and Colspan are used to span cells across multiple rows or columns.

---

## CSS (Cascading Style Sheets)

### CSS Syntax

```css
selector {
  property: value;
}
```

Example:

```css
p {
  color: red;
  background-color: yellow;
}
```

---

## Applying CSS

1. **Inline**  
   Inside HTML tag:  
   `<p style="color:red;">Text</p>`

2. **Embedded**  
   Inside `<style>` in `<head>`:

```html
<style>
  h1 { color: blue; }
</style>
```

3. **External**  
   Linked CSS file:

```html
<link rel="stylesheet" href="style.css">
```

---

## CSS Selectors

- Tag: `p`, `div`
- Class: `.class-name`
- ID: `#id-name`
- Grouping: `h1, h2, p { ... }`
- Contextual: `ul li`, `a:hover`, `li em`

---

## Box Model: Margin, Padding, Border

- `margin`: space outside the element
- `padding`: space inside the element
- Units: `px`, `%`, `em`

```css
div {
  margin: 20px;
  padding: 10px;
  border: 1px solid black;
}
```

---

## Layout and Positioning

### Display Types

- `block`, `inline`, `inline-block`, `none`
- Example:

```css
div {
  display: inline-block;
  width: 100px;
}
```

### Positioning

```css
position: static | relative | absolute | fixed;
z-index: 1;
```

---

## Div, Span, and Semantic Tags

- `<div>`: Block container
- `<span>`: Inline container
- Semantic tags:
  - `<header>`, `<nav>`, `<section>`, `<footer>`

---

## Responsive Layout with Flexbox

```css
section {
  display: flex;
  flex-direction: row | column;
}
```

```css
div {
  margin: auto;
  width: 100px;
}
```

---

## CSS Class vs ID

| Feature | Class | ID |
|--------|-------|----|
| Symbol | `.`   | `#` |
| Reuse  | Yes   | No (unique) |
| HTML   | `class="blue"` | `id="header"` |
| CSS    | `.blue {}`     | `#header {}` |

---

