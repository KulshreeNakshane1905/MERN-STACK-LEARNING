# 🌐 Day 2 - HTML Tables & Forms (Web Development)

> **Course:** MERN Stack Learning Journey  
> **Topic:** HTML (Level 2 & 3) — Tables, Forms & Input Elements  
> **Date:** 15/01/2025

---

## 📌 Further Understanding in HTML — HTML 5

### HTML Standard:
It is a document that tells the browser **how HTML should work**.

---

## 📊 HTML 3 — Tables & Forms

### Tables in HTML:
Used to **represent real-life table data**.

Tables have:
- **Rows** → `<tr>` — used to represent rows
- **Columns** → `<td>` — used to display data / `<th>` — used to display header

### Basic Table Structure:

```html
<table>
  <caption>Table Caption</caption>
  <tr>
    <th>header 1</th>
    <th>header 2</th>
  </tr>
  <tr>
    <td>data 1</td>
    <td>data 2</td>
  </tr>
</table>
```

---

## 🏛️ Semantics in Tables

| Tag | Purpose |
|-----|---------|
| `<thead>` | To wrap table header |
| `<tbody>` | To wrap table body |
| `<tfoot>` | To wrap table footer |

---

## 🔗 Colspan & Rowspan Attribute

Used to create cells which **spans over multiple rows or columns**.

```html
<td rowspan="2"></td>       <!-- spans 2 rows -->
<td colspan="2">Average</td> <!-- spans 2 columns -->
```

### Practice Question — Create a table with merged cells:

```html
<body>
  <table border="black">
    <caption>A test table with merged cells</caption>
    <tr>
      <td rowspan="2"></td>
      <td colspan="2">Average</td>
    </tr>
    <tr>
      <th>average</th>
      <th>Redeyes</th>
    </tr>
    <tr>
      <td>Height</td>
      <td>Weight</td>
    </tr>
    <tr>
      <td>Males</td>
      <td>1.9</td>
      <td>0.003</td>
      <td>40</td>
    </tr>
    <tr>
      <td>Females</td>
      <td>2.0</td>
      <td>0004</td>
      <td>50</td>
    </tr>
  </table>
</body>
```

---

## 📝 Forms in HTML

```html
<form>
  form content
</form>
```

### Action Attribute in Forms:
Action attribute is used to **define what action needs to be performed** when a form is submitted, or **where the form data should be sent**.

```html
<form action="/action.php">
<form action="/action">
```

---

## 🖊️ Form Input Elements

`<input>` is used to **create multiple form controls**.  
There are **multiple types of inputs** that can be created using the `type` attribute.  
Important: `<input>` has **no closing tag**.

```html
<input type=" ">
```

### Basic Input Tag:
```html
<body>
  <form action="/action">
    Username
    <input type="text"/>
    <br>
    Password
    <input type="password"/>
    <br>
  </form>
</body>
```

### Different Types of Input Attributes:

| Type | Tag |
|------|-----|
| Text | `<input type="text">` |
| Password | `<input type="password">` |
| Number | `<input type="number">` |
| Time | `<input type="time">` |
| Color | `<input type="color">` |

---

## 🏷️ Placeholders & Labels

### Placeholder Attribute:
Shows hint text inside an input box.

```html
<input type="text" placeholder="Enter Name">
<input type="text" placeholder="enter password">
```

### Labels:
Label element represents a **caption for an item in a user interface**.

```html
<!-- Wrapping approach -->
<label>
  Enter your username.
  <input type="text" placeholder="username">
</label>

<!-- Classical Approach (using 'for' attribute) -->
<label for="username">Enter your username:</label>
<input type="text" id="username" placeholder="username">
```

---

## ✅ Input Element — Checkbox

```html
<input type="checkbox" name="age" id="age" checked/>
<label for="age">I am 18+</label>
```

- When checkbox is **ticked** → the URL passed is `age=on`
- When checkbox is **unchecked** → nothing will be passed

---

## 🔘 Input Element — Radio Button

Only **one option** can be selected at a time.

```html
<input type="radio" name="fruit" id="apple" value="apple"/>
<label for="apple">Apple</label>
```

- The information that is passed in URL is in **name = value format**
- To **group radio elements**, the `name` value should be **similar** for all inputs so that only one option will be selected properly rather than multiple options

### Main difference between Checkbox and Radio:
> After grouping, I can still **select multiple options in checkbox**, but in radio it is **not the same** — only one can be selected.

---

## 📋 Input Element — Dropdown

Goes into URL.

```html
<select name="profession" id="profession">
  <option value="student">student</option>
  <option value="dev">Developer</option>
</select>
```

> If we want an **already selected option**, then add `selected` attribute to that `<option>`.

---

## 🔢 Input (Range)

```html
<label for="volume">Volume</label>
<input type="range" min="0" max="100" name="vol">
```

- If we want it to increase by a **specific number**, we use `step`
- If we want to **fix the range** whenever the web opens, we use `value=""`

---

## 📝 Text Area (for paragraph, comment, feedback)

```html
<label for="feedback">Please provide your valuable feedback:</label>
<textarea id="feedback"></textarea>
```

> If we want a **large text box**, we use `rows` and `columns` attributes.

---

## 🔘 Button Element

```html
<button>submit</button>
```

### Type of attribute:
```html
<button type="submit">submit</button>
<button type="button">do something</button>
<button type="reset">do something</button>
```

### Button using Input Element:
```html
<input type="submit">
<input type="submit" value="click me">
```

---

## 🏷️ Name Attribute

Name of the form control. Submitted with the form as part of a **name/value pair**.

```html
<input type="text" placeholder="enter name" id="username" name="username"/>
```

### Example — YouTube Search Form:
```html
<form action="https://www.youtube.com/results?search_query=">
  <input type="text" placeholder="search in youtube" name="search_query">
  <button>Search</button>
</form>
```

---

## 🌈 More Input Types

```html
<input type="color">
<input type="number"/>
<br>
<input type="time"/>
</form>
```

---

*Day 2 Complete! ✅ Tables & Forms mastered! Keep going! 🚀*
