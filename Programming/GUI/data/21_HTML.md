---
Author: AAM
Date: 2024-03-24
tags:
  - "#programming"
  - frontend
---
---
# HTML

[Back to index](../GUI.md)

---
## Introduction
### Tags

- There are 2 types of tags:
	- Open/Close tags.
	```HTML
	<tag>contents</tag>
	```
	- Standalone tags.
	```HTML
	<tag>
	```

- Tags can also have some attributes
```Html
<tag attribute="something">
```
### Page Structure

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<!-- Not displayed information -->
	</head>
	<body>
		<!-- Content of the webpage -->
	</body>
</html>
```

---
## Head

```html
<!-- Title of the page -->
<title> ... </title>

<!-- Defines the page style (CSS) -->
<style> ... </style>

<!-- Defines the page style (CSS) -->
<script> ... </script>

<!-- Defines the page scripts (JS) -->
<link> ... </link>

<!-- Some page metadata -->
<meta charset="utf-8">
<meta name="description" content="my page description">
<meta name="keywords" content="keyword1, keyword2">
<meta name="author" content="author's name">

<!-- Base URL for a page relative links -->
<base html href="base URL" target="_blank">
```

---
## Body 

### Structure
```html
<!-- Goup of related contents -->
<section> ... </section>

<!-- Headers (bigger to smaller) -->
<h1> ... </h1>
<h2> ... </h2>
<h3> ... </h3>
<h4> ... </h4>
<h5> ... </h5>
<h6> ... </h6>
```
### Basic tags
```html
<!-- Paragraph -->
<p>...</p>

<!-- Header of a block -->
<header> ... </header>

<!-- Footer of a block -->
<footer> ... </footer>

<!-- Line break -->
<br>

<!-- Horizontal rule. Used to separate contents. -->
<hr>

<!-- Preformated text -->
<pre> ... </pre>
```
### Formatting tags
```html
<!-- Highlight (by default bold) -->
<strong> ... </strong>

<!-- Emphasise (by default italics) -->
<em> ... </em>

<!-- Subscript -->
<sub> ... </sub>

<!-- Superscript -->
<sup> ... </sup>
```
### Quotations
```html
<!-- Blockquote -->
<blockquote cite="URL"> ... </blockquote>

<!-- Inline quotation -->
<q> ... </q>

<!-- Abbreviations -->
<abbr title="Complete"> Abbreviation </abbr>
```
### Styling tags
```html
<!-- Used to apply styling to blocks of tags -->
<div id=“someID” class=“someClass”> ... </div>

<!-- Used to apply styling to text fragments -->
<span> ... </span>
```

### Links
```HTML
<a href="URL" target="_target"> Displayed text </a>
```

- The `URL` can be internal/external and absolute/relative.
	- To have a link to an email  use URL `mailto:email.
	- To have a link to a section use URL `#section`
- The `_target` can be:
	- `_blank`. Opens the link to a new tab.
	- `_self`. Opens the same tab (default).
### Multimedia
- An alternative (`alt`) must always be provided for accessibility.

```html
<img src="image" alt="Alternative text">
```

### Lists
```html
<!-- Ordered list -->
<ol>
	<a>
</ol>

<!-- Unordered list -->

```

### Tables
```html

```

---
## CSS
### In-line styling
