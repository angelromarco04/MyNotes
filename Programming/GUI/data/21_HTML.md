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
### Basic tags

```html
<!-- Paragraphs -->
<p>...</p>

<!-- Header of a block -->
<header> ... </header>

<!-- Footer of a block -->
<footer> ... </footer>

<!-- Sections of a block -->
<section> ... </section>

<!-- Headers (bigger to smaller) -->
<h1> ... </h1>
<h2> ... </h2>
<h3> ... </h3>
<h4> ... </h4>
<h5> ... </h5>
<h6> ... </h6>

<!-- ? -->
<br>

<!-- ? -->
<hr>
```

---
### Block markup
```html
<div id=“someID” class=“someClass”> ... </div>

<span> ... </span>
```

---
### Media
```html
<img>
<input>
```