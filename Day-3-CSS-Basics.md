# 🎨 Day 3 - CSS Basics (Web Development)
> **Topic:** CSS — Cascading Style Sheets  

---

## 📌 What is CSS?

**CSS** stands for **Cascading Style Sheets**.  
It is a language that is used to **describe the style of a document**.

---

## 🧱 Basic Format of CSS

```css
selector {
  property: value;
}
```

```css
h1 {
  color: red;
}
```

- **Selector** → targets the HTML element
- **Property** → what you want to style
- **Value** → how you want to style it

---

## 🖌️ How to Include Styles?

### 1. Inline Styles
Writing style directly inline on each element.

```html
<h1 style="color: red;">Apna College</h1>
```

### 2. Using `<style>` Tag
Style is added using the `<style>` element in the same document.

```html
<style>
  h1 {
    color: red;
  }
</style>
```

### 3. External Stylesheet
Writing CSS in a **separate document** and linking it with the HTML file.

```html
<head>
  <link rel="stylesheet" href="style.css">
</head>
```

> `rel` = relation, `href` = path to the CSS file  
> 🎨 Color palette resource: **colors.co**

---

## 🎯 CSS Selectors

### Element Selector
Selects **all elements of the same type**.

```css
h1 {
  property: value;
}

/* Multiple elements */
h1, h3 {
  color: #b92b27;
}
```

### Universal Selector
Selects **all elements** on the page.

```css
* {
  property: value;
}
```

### ID Selector
Selects an element based on the **value of its `id` attribute**.

```css
#myId {
  property: value;
}
```

### Class Selector
Selects an element based on their **class attribute**.

```css
.myClass {
  property: value;
}
```

---

## 🔗 CSS Combinators

### Descendant Selector
Selects **all paragraphs inside divs**.

```css
div p {
  property: value;
}
```

### Adjacent Sibling Combinator
Selects heading 3 that comes **immediately after** any paragraph.

```css
p + h3 {
  property: value;
}
```

### Child Combinator
Selects all buttons which are **direct children** of spans.

```css
span > button {
  property: value;
}
```

> ⚠️ **Disadvantage of Child Combinator:** It does not go into multiple levels — it goes up to only one level. But as **descendant selector**, it goes up to multiple levels.  
> *(Improve attribute selector learning)*

---

## 🎭 Pseudo Class

A keyword added to a selector that **specifies a special state** of the selected element(s).

```css
:hover
:active
:checked     /* radio button */
:nth-of-type(2n)   /* every second element — colour changed */
```

### Example:
```css
.myClass:hover {
  color: blue;
}
```

---

## ✨ Pseudo Element

A keyword added to a selector that lets you **style a specific part** of that selected element(s).

```css
::first-letter
::first-line
::selection
```

### Example:
```css
h1::first-letter {
  color: green;
}

p::first-line {
  color: black;
}

p::selection {
  background-color: lemon;
}
```

---

## 🌊 CSS — Cascading Style Sheets

### What is Cascade in CSS?
This CSS cascade algorithm's job is to **select CSS declarations** in order to determine the **correct values for CSS properties**.

```css
h2 {
  background-color: yellow;
}
h2 {
  background-color: blue;  /* final colour — blue will be applied */
}
```

---

## ⚖️ Selector Specificity

Specificity is an algorithm that **calculates the weight** that is applied to a given CSS declaration.

| Selector | Weight |
|----------|--------|
| Inline style | Highest |
| `id` | 1 |
| `class`, attribute, pseudo class | 0 |
| element & pseudo-element | 1 |

**Priority order:**  `id > class > element`

### Specificity Score:

| | id | class, attribute & pseudo class | element & pseudo-element |
|--|----|---------------------------------|--------------------------|
| Score | 0 | 0 | 1 |

> **Which is greater than the above one → highest priority will be given to that.**

### Note Points:
1. `id > class > element`
2. More selectors > less selectors ↑ CSS
3. If specificity is same → **Cascading** applies

### Inline Specificity:
Inline styles are **more specific than id**.

```
Inline style > id > class > element
```

---

## ❗ `!important`

To show the **most specific thing** in document that I will never want to change — we use `!important`.

```css
h2 {
  background-color: blue !important;
}
```

---

## 🏗️ Inheritance in CSS

Properties are **inherited from parents to children** likewise.

```html
<div>
  <p></p>
  <ul>
    <li></li>
  </ul>
  <p></p>
</div>
```

> In this example, the properties of `div` are inherited by `paragraph`, `ul`, and `li`.

### Non-inherited properties:
`width`, `height`, `border` — these are **NOT inherited**.

---

## 📦 Box Model in CSS

Every element in CSS is a box with:

- **Height**
- **Width**
- **Margin**
- **Border**
- **Padding**

```
┌─────────────────────────────┐  ← Margin
│  ┌───────────────────────┐  │  ← Border
│  │  ┌─────────────────┐  │  │  ← Padding
│  │  │    Content      │  │  │
│  │  └─────────────────┘  │  │
│  └───────────────────────┘  │
└─────────────────────────────┘
```

---

## 📏 Height & Width

### 1. Height:
By default, it sets the **content area height** of the element.

```css
div {
  height: 100px;
}
```

### 2. Width:
By default, it sets the **content area width** of the element.

```css
div {
  width: 300px;
}
```

---

## 🔲 Border

Used to **set an element's border**.

```css
/* Individual properties */
border-width
border-style
border-color

/* Shorthand: width | style | color */
div {
  border: 2px solid blue;
}
```

### Border Sides:
To control an **individual side** of the box:

```css
border-left
border-right
border-top
border-bottom
```

### Border Radius:
Used to **round the corners** of an element's outer border edge.

```css
div {
  border-radius: 15px;
}

div {
  border-radius: 50%;  /* complete circle — set equal height & width */
}
```

> If we want a **complete circle**, put height and width of the same pixel.

---

## 📐 Padding

Sets spacing **inside** the border (between content and border).

```css
padding-left
padding-right
padding-top
padding-bottom
```

### Padding Shorthand:

| # | Sides | Example |
|---|-------|---------|
| 1 | All 4 sides | `padding: 50px` |
| 2 | Top & Bottom \| Left & Right | `padding: 1px 2px` |
| 3 | Top \| Left & Right \| Bottom | `padding: 1px 2px 3px` |
| 4 | Clockwise: Top \| Right \| Bottom \| Left | `padding: 1px 2px 3px 4px` |

---

## 📏 Margin

Sets spacing **outside** the border.

```
[content] ←——margin——→ [content]
```

```css
margin-left
margin-right
margin-top
margin-bottom
```

### Margin Shorthand:

| # | Sides | Example |
|---|-------|---------|
| 1 | All 4 sides | `margin: 50px` |
| 2 | Top & Bottom \| Left & Right | `margin: 1px 2px` |
| 3 | Top \| Left & Right \| Bottom | `margin: 1px 2px 3px` |
| 4 | Clockwise: Top \| Right \| Bottom \| Left | `margin: 1px 2px 3px 4px` |

> We can also **unset/set the default margin**.

---

## 🖥️ Display Property

Sets whether an element is treated as a **block or inline element** and the **layout used for its children**.

```css
display: inline;
display: block;
```

### Example:
```css
h2 {
  display: inline;
}

span {
  display: block;
}
```

*Day 3 Complete! ✅ 
