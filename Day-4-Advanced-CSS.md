# 🎨 Day 4 - Advanced CSS (Web Development)

> **Course:** MERN Stack Learning Journey  
> **Topic:** Advanced CSS — Units, Display, Flexbox, Grid, Position, Transitions, Transforms & Animations  
> **Date:** 15/03/2026

---

## 📐 Units in CSS

| Type | Absolute Units | Relative Units |
|------|---------------|----------------|
| | `px` | `%` |
| | `pt` | `em` |
| | `pc` | `rem` |
| | `cm` | `ch` |
| | `mm` | `vh` |
| | `in` | `vw` + many more |

### Percentage (%)
Often used to define a size **relative to an element's parent object**.

```css
width: 33.33%;        /* relative to parent */
margin-left: 50%;     /* relative to the parent size */
```

---

## 🔤 Units — em

Relative to the **font size of the parent**, in the case of typographical properties like `font-size`, and font size of the element itself in the case of other properties like `width`.

```css
/* font-size = 10px → 1em = 10px */
/* font-size = 3em = 30px */
/* padding = 1em = 30px */
```

> **Drawback of Em:** If we want the padding to change according to the font size, we use `em` unit.

```css
button {
  font-size: 50px;
  border-radius: 15px;
  border: 5px solid green;
  padding-left: 1em;
  padding-right: 1em;
}
```

---

## 🔤 Units — rem (Root Em)

| Unit | Relative to |
|------|-------------|
| `rem` | font size of the **root element** |

---

## 🎨 Alpha Channel

Sets the **opacity for a color**. Ranges from `0` to `1` (0 = hidden).

```css
rgba(255, 255, 255, 0.3)
/*               ↑ alpha */
```

---

## 👁️ Opacity

Sets the **opacity for the element**. Ranges from `0` to `1` (0 = hidden).

```css
opacity: 0.5;
```

---

## 🖥️ Display Property — Block vs Inline vs Inline-block

### BLOCK:
1. Always start on a **new line**
2. Take up as much **horizontal space** as possible
3. Will **respect width and height** CSS properties
4. **Horizontal and vertical margins** both work

### INLINE:
1. Do **not** start on a new line
2. Only use as much horizontal space as **required by content**
3. Do **not accept width and height** CSS properties
4. **Margins work horizontally** but not vertically
5. **Padding works on all sides** but top and bottom may overlap other elements

### `display: inline-block`:
Behave like a **block element** and it keeps the styling.

### `display: none`:
If we want to **hide any block**, we use `none` there.

> **Note on Span:** When we set elements in the span, border, height, width are not implemented. Padding implemented only to left and right. Margin also implemented only to left and right. But if we apply same elements on `div` then the result will be different — means it will apply to all elements.

---

## 📍 Position Property

The position CSS property sets how an element is positioned in a document.  
The `top`, `right`, `bottom`, and `left` properties determine the final location of positioned elements.

- `static`
- `relative`
- `absolute`
- `fixed`

### 1. Static:
The `top`, `right`, `bottom`, `left`, and `z-index` properties have **no effect**. This is the **default value**.

### 2. Relative:
The offset is relative to **itself** based on the values of `top`, `right`, `bottom`, and `left`.

### 3. Absolute:
The element is **removed from the normal document flow** and no space is created for the element in the page layout.  
It is positioned relative to its **closest positioned ancestor** if any; otherwise it is placed relative to the **initial containing block**.

### 4. Fixed:
The element is **removed from the normal document flow** and no space is created for the element in the page layout.  
It is positioned relative to the **initial containing block established by the viewport**.

> `sticky` — also a position we can set.

---

## 📦 Flexbox → [Responsive]

**Flexible box layout** — It is an **one-dimensional** layout method for arranging items in rows or columns.

```
flex container → direction = row
     |
  main axis ————————————
     |
  cross axis
```

### Flex Model:
```css
.container {
  display: flex;
}
```

By default, display flex direction is in the form of **row** only.

```css
flex-direction: column;   /* horizontal → vertical */
flex-direction: row;      /* in row form i.e vertical */
```

### Flexbox Direction:
It sets how flex items are placed in the flex container — along which **axis** and **direction**.

```css
flex-box-direction: row;             /* L → R (main axis) */
flex-box-direction: row-reverse;     /* R → L */
flex-box-direction: column;          /* top to bottom */
flex-box-direction: column-reverse;  /* bottom to top */
```

---

## ↔️ Justify Content

Tells how the browser **distributes space between and around content items** along the **main axis**.

```css
justify-content: flex-start;
justify-content: flex-end;
justify-content: center;
justify-content: space-between;
justify-content: space-around;
justify-content: space-evenly;
```

---

## ↕️ Align Items

Distributes our items along the **cross axis**.

```css
justify-content: flex-start;
justify-content: flex-end;
justify-content: center;
justify-content: baseline;
/* (2RT — content same line पर आलायेगा) */
```

---

## 📦 Align Content

Sets the distribution of space **between and around content items** along a flexbox's **cross axis**.

```css
align-content: flex-start;
align-content: flex-end;
align-content: center;
align-content: space-between;
align-content: space-around;
align-content: evenly;
align-content: baseline;
```

---

## 🔀 Flex Wrap

Sets whether flex items are forced onto one line or can **wrap onto multiple lines**.

```css
flex-wrap: nowrap;
flex-wrap: wrap;
flex-wrap: wrap-reverse;
/* ↓ cross axis ke along wrap ho jate hai items */
```

---

## 🎯 Align Self (property for individual)

Aligns an item along the **cross axis**.

```css
align-self: flex-start;
align-self: flex-end;
align-self: center;
align-self: baseline;
```

---

## 📏 Flex Sizing

### Flex Basis:
Sets the **initial main size** of a flex item.

```css
flex-basis: 100px;
```

### Flex Grow:
Specifies how much of the flex container's **remaining space** should be assigned to the flex item's main size.

```css
flex-grow: 1;
```

### Flex Shrink:
Sets the **flex shrink factor** of a flex item.

```css
flex-shrink: 1;
```

### Flex Shorthand:

```css
/* flex-grow | flex-shrink | flex-basis */
flex: 2 2 100px;

/* flex-grow | flex-basis */
flex: 2 100px;

/* flex-grow (unitless) */
flex: 2;
```

---

## 🏗️ CSS Grid

Setting a container's display to `grid` will make all children **grid items**.

```css
.container {
  display: grid;
}
```

### Grid Model:
- **Grid lines** → `#`
- **Grid cell** = box `##`
- **Grid Track** = distance between two lines `---`

```
L1  L2  L3  L4
|   |   |   |
|   |   |   |  ← row lines
|   |   |   |
```

> If you want to check grid lines, you can **inspect it**.

---

## 📋 Grid Template

They define the **lines & track sizing**.

### grid-template-rows:
```css
grid-template-rows: t1(100px) t2(100px) t3(100px);
/* No of lines is always > than track */
/* We can use 'auto' also */
```

### grid-template-columns:
```css
grid-template-columns: 100px 100px 100px;
```

> We did not prefer `auto` so we directly give our values.

### Grid Template — Repeat:
`repeat` is used to **divide all available spaces**.

```css
grid-template-rows: repeat(count, 1fr);
grid-template-columns: repeat(count, 1fr);

grid-template-rows: repeat(2, 1fr);
grid-template-rows: 1fr 1fr;
```

---

## 🕳️ Grid Gaps

They define the **gaps between the lines**.

```css
row-gap: ;
column-gap: ;

/* Shorthand */
grid-gap: rowgap columngap;
```

---

## 📍 Grid Columns

Defines an item's **starting & ending position inside the column**.

```css
grid-column-start: line_number;
grid-column-end: line_number;

/* Shorthand */
grid-column: start_col / end_col;
grid-column: start_col / span no.;
/* 1 / span 3 */
```

After starting box — how many boxes that you want after starting line is called **span no**.  
`1 / span 2`

---

## 📍 Grid Rows

Defines an item's **starting & ending position inside the row**.

```css
grid-row-start: line_number;
grid-row-end: line_number;

/* Shorthand */
grid-row: start_row / end_row;
grid-row: start_row / span number;
```

---

## 🎛️ Common Grid Properties

| Property | Applies to | Direction |
|----------|-----------|-----------|
| `justify-items` | container | Horizontal |
| `justify-self` | item | Horizontal |
| `align-items` | container | Vertical |
| `align-self` | item | Vertical |
| `place-items` | for individual items | — |
| `place-self` | for individual items | — |

---

## 🎬 Animations in CSS

To **animate CSS elements**.

```css
@keyframe myName {
  from { font-size: 20px; }
  to   { font-size: 40px; }
}
```

```
State A ————————→ State B
 20px              40px
```

### Animation Properties:
```css
animation-name
animation-duration
animation-timing-function
animation-delay
animation-iteration-count
animation-direction
```

### Shorthand:
```css
animation: widthAnimate 3s ease-in 0s infinite normal;
```

---

## 🔄 CSS Transition

Transition enables you to **define the transition between two states** of an element.

```
[state 1] ——transition——→ [state 2]
```

```css
div {
  transition: 1s;
}

div:hover {
  border-radius: 50%;
}
```

### Transition Duration:
```css
/* transition: property name | duration | timing function | delay */
transition: margin-top 2s ease-in-out 0.2s;
```

### Centering a div:
```css
/* for eg: */
margin: 0 auto;
```

---

## 🔧 CSS Transform

This property lets you **rotate, scale, skew, or translate** an element.

### (i) Rotate:
```css
transform: rotate(45deg);
```

### (ii) Scale:
```css
transform: scale(0.5);
transform: scale(1.5);
```

### (iii) Translate (movement in 2D plane only):
```css
transform: translate(50px, 50px);
transform: translateX(10px);
transform: translateY(10px);
```

### (iv) Skew:
```css
transform: skew(30deg);
```

### Combined:
```css
transform: rotate(30deg) translateX(150px);
```

---

## 🌑 Box Shadow

Adds **shadow effects** around an element's frame.

```css
/* x-offset | y-offset | blur radius | color */
box-shadow: 2px 2px 10px green;
```

---

## 🖼️ Background Image

Lets you set an **image as a background**.

```css
background-img: url("  ");
background-size: contain / cover / auto;
/* mostly we use 'cover' — it is the best way to set the background image */
```

---

## 🃏 Card Hover Effect

*(Practice project using transitions and transforms)*

---

*Day 4 Complete! ✅ Flexbox, Grid, Position, Transitions & Animations mastered! 🚀*
