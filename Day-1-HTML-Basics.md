# 🌐 Day 1 - HTML Basics (Web Development)

> **Course:** MERN Stack Learning Journey  
> **Topic:** HTML (Level 1) — HyperText Markup Language

---

## 📌 What is HTML?

**HTML** stands for **HyperText Markup Language** — it is used for **structure and formatting** of web pages.  
We use HTML to present formatted and structured content.

---

## 🏗️ HTML Elements

Standard elements that the browser recognizes:

| Element | Opening Tag | Closing Tag |
|---------|-------------|-------------|
| Paragraph | `<p>` | `</p>` |
| Heading | `<h1>` | `</h1>` |
| Image | `<img>` | — |

### Structure of an HTML Tag:
```
<p> This is paragraph </p>
 ↑         ↑            ↑
Opening   Content    Closing Tag
 tag               = Element
```

---

## 🗂️ HTML Boilerplate Code

This is the standard format or skeleton of writing HTML:

```html
<!DOCTYPE html>
<html>         <!-- root tag -->
  <head>
    <title>My First Page</title>   <!-- This is the website name -->
  </head>
  <body>
    <p>hello world</p>
  </body>
</html>
```

> **Note:** Linking or metadata we store in `<head>` tag.  
> Use **indentation** for proper spacing.  
> Save file with `.html` extension (e.g., `helloworld.html`).

---

## 🔤 Paragraph Element

- `<p>` tag is used to show text content.
- If we want to show multiple content in multiple paragraphs, we must use multiple `<p>` tags.
- In a single paragraph tag, it does **not** detect spacing by giving space only — it fails.

```html
<p>Kulshree is a clever girl.</p>
```

---

## 🔢 Nesting → Nested Tags

When we give a tag within a tag, this is called **nested tag** or **nesting**.

```html
<p>Hello World <b>Kulshree</b></p>
```
> `<b>` tag is nested inside `<p>` tag, so `bold` tag is nested tag.

---

## 🔠 Heading Elements

The `<h1>` to `<h6>` HTML elements represent **six levels of section headings**.  
`<h1>` is the **highest** section level and `<h6>` is the **lowest**.  
All headings have their own **default size font**.

```html
<h1> heading elements </h1>
```

### Practice:
```html
<h1>Avengers</h1>
<h2>Iron Man</h2>
<p>Also goes by the name Tony Stark</p>
<h2>Captain America</h2>
<p>Also goes by the name Steve Rogers</p>
<h3>Hulk</h3>
<p></p>
```

---

## 📋 Lists in HTML

### Unordered List (ul):
```html
<ul>
  <li>Butter</li>
  <li>Ram</li>
  <li>Seeta</li>
</ul>
```

### Ordered List (ol):
```html
<ol>
  <li>Deepak</li>
  <li>Epsita</li>
  <li>Lakshita</li>
  <li>Tanmay</li>
  <li>Agrim</li>
</ol>
```

> We can use other tags in list tag as well:
```html
<ul>
  <li><h2>Want to buy: Bread</h2></li>
</ul>
```

---

## 🔗 Anchor Element

Used to **add links** to our page.

```html
<a href="https://google.com">Google</a>
```

- `href` attribute = **hypertext reference**
- Links can be **absolute** (internet URL) or **relative** (local file)

### Example:
```html
<a href="https://www.apnacollege.com">Go to Apna College</a>

<!-- Multiple links -->
<a href="https://www.google.com">Google</a>
<a href="https://www.youtube.com">YouTube</a>
<a href="https://www.facebook.com">Facebook</a>
```

---

## 🖼️ Image Element

Used to **add images** to our page.

```html
<img src="image.png" alt="Random Image">
```

- `src` = source (absolute URL or relative file path)
- `alt` = alternative text shown if image fails to load

```html
<!-- From internet -->
<img src="absolute_url" alt="Random Image">

<!-- From local file -->
<img src="relative_path" alt="Random Image">
```

---

## 📐 Inline vs Block Elements

### Block Elements:
- Take up the **full width available** (whole block)
- Always **start from a new line**

### Inline Elements:
- Take up **only necessary width**
- **Don't start** from a new line

| Element | Type |
|---------|------|
| `<p>` | Block |
| `<h1>`–`<h6>` | Block |
| `<div>` | Block |
| `<a>` | Inline |
| `<img>` | Inline |
| `<span>` | Inline |

---

## 📦 DIV Element

`<div>` is a **Content Division Element** — a container used to hold other HTML elements or group elements together.  
It is a **block element**.

```html
<div>
  <a href="https://www.google.com">Google</a>
  <a href="https://www.youtube.com">YouTube</a>
  <a href="https://www.facebook.com">Facebook</a>
</div>
```

---

## 🏷️ Span Element

`<span>` is also a **generic container** used to hold other HTML elements or group elements together.  
It is an **inline element**.

```html
<p>for eq.</p>
```

---

## ➖ HR Tag (Horizontal Rule Element)

Creates a **horizontal line** — used to **divide sections**.

```html
<hr>
```

---

## 📝 Sup & Sub Tags

```html
<!-- Superscript -->
<sup>2</sup>   →  a²

<!-- Subscript -->
<sub>2</sub>   →  H₂O
```

**Example:**
```html
<!-- Pythagoras theorem -->
<p>a <sup>2</sup> + b <sup>2</sup> = c <sup>2</sup></p>

<!-- Glucose formula -->
<p>C <sub>12</sub> H <sub>22</sub> O <sub>11</sub></p>
```

---

## 💪 Bold, Italic & Underline Tags

| Tag | Use |
|-----|-----|
| `<b>` | **Bold** — darker text |
| `<i>` | *Italic* — highlight text |
| `<u>` | <u>Underline</u> |

---

## 🔀 BR Tag

Used to **add a new line** (line break) to our page.

```html
<p>Twinkle Twinkle <br> little star <br> how <br> wonder <br> what you are</p>
```

---

## 💬 Comments in HTML

```html
<!-- This is a comment -->
<!-- ctrl + / (forward slash) for comment the specific line -->
```

---

## 🔤 HTML Entities

An HTML entity is a piece of text (`"string"`) that:
1. Begins with an `&` (ampersand) and ends with a `;` (semicolon)
2. Used to display **reserved characters** (which would otherwise be interpreted as HTML code) and **invisible characters** (like non-breaking spaces)
3. Can also be used in place of characters that are **difficult to type** with a standard keyboard
4. Browser interprets them and renders the correct character

| Character | Entity | Note |
|-----------|--------|------|
| `&` | `&amp;` | Beginning of an entity or character |
| `<` | `&lt;` | Beginning of a tag |
| `>` | `&gt;` | Ending of a tag |
| `"` | `&quot;` | Value (beginning and end of an attribute) |

**Example:**
```html
<h1>The sky is cloudy &#9729; &#9733; &#9728;</h1>
<h1>The sky is cloudy &amp; it will rain &#9728;</h1>
```

---

## 🏛️ Semantic Markup

It is the markup that **relates to the meaning of content**.

**Benefits:**
1. Meaningful / layout structured
2. SEO friendly
3. Readable + Screen readers (UI improve)

### Semantic Tags:
```html
<header> </header>
<main> </main>
<footer> </footer>
<nav> </nav>
```

### Non-Semantic Tags:
```html
<div>
<span>
```

---

## ⚙️ Attributes in HTML

Attributes are used to **add more information to the tag**.
- Uses `"double quotes"` and `single quotes` — both have the same meaning in HTML.

---

## ✨ Emmet — emmet.io

A shortcut tool for writing HTML faster.

- `#` = parent-child relation
- `#` = sibling

```
child1
  child2
    child3
```

---

## 📚 Resources

- **MDN Web Docs** — Best resource for development
- **JavaScript** = case sensitive
- HTML is **not** case sensitive

---

Day 1 Complete! ✅ 
