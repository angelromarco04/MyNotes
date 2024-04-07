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

---
## Introduction
### HTML Tags

- There are 2 types of tags:
	- Open/Close tags.
	```HTML
	<tag>contents</tag>
	```
	- Standalone tags.
	```HTML
	<tag/>
	```

- Tags can also have some attributes
```Html
<tag attribute="something"> ... </tag>
<tag attribute="something"/>
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
<meta charset="utf-8"/>
<meta name="description" content="my page description"/>
<meta name="keywords" content="keyword1, keyword2"/>
<meta name="author" content="author's name"/>
<meta name="viewport"
	  content="width=device-width, initial-scale=1.0">
<!-- Base URL for a page relative links -->
<base html href="base URL" target="_blank"/>
```

---
## Body 

### Body Layout

- [HTML Layout](https://www.w3schools.com/html/html_layout.asp)

```html
<!-- Header of the page -->
<header> ... </header>

<!-- Navigation bar of the page -->
<nav> ... </nav>

<!-- Sections of the page -->
<section> ... </section>

<!-- Articles of the page -->
<article> ... </article>

<!-- Sidebar of the page -->
<aside> ... </aside>

<!-- Footer of the page -->
<footer> ... </footer>
```

### Headers
```html
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

<!-- Line break -->
<br/>

<!-- Horizontal rule. Used to separate contents. -->
<hr/>
```
### Formatting tags
```html
<!-- Preformated text -->
<pre> ... </pre>

<!-- Highlight (by default bold) -->
<strong> ... </strong>

<!-- Emphasise (by default italics) -->
<em> ... </em>

<!-- Subscript -->
<sub> ... </sub>

<!-- Superscript -->
<sup> ... </sup>
```
### Quotations & Definitions
```html
<!-- Blockquote -->
<blockquote cite="URL"> ... </blockquote>

<!-- Inline quotation -->
<q> ... </q>

<!-- Abbreviations -->
<abbr title="Complete"> Abbreviation </abbr>

<!-- Acronyms -->
<acronym title="Complete"> ... </acronym>

<!-- Definitions -->
<dfn title="Definition"> ... </dfn>
```
### Other blocks
```html
<!-- Codeblock -->
<code> ... </code>

<!-- Collapsible Block -->
<details>
  <summary>Click to expand</summary>
  ...
</details>

<!-- Select Option -->
<select>
   <optgroup label="Menu1">
      <option>One option</option>
      ...
   </optgroup>
   <optgroup label="Menu2">
      <option>Other option</option>
      ...
   </optgroup>
</select>

```
### Styling tags
```html
<!-- Used to apply styling to blocks of tags -->
<div id=“someID” class=“someClass”> ... </div>

<!-- Used to apply styling to text fragments -->
<span id=“someID” class=“someClass”> ... </span>
```
### Links
```HTML
<!-- Basic link -->
<a href="http://page.com" target="_target"> Link </a>

<!-- Section link -->
<a href="#section" target="_target"> Go to section </a>

<!-- Email link -->
<a href="mailto:name@example.com"> Send Email </a>

<!-- Phone call link -->
<a href="tel:+1234567890"> Call Us </a>

<!-- SMS link -->
<a href="sms:+1234567890"> Send SMS </a>
```

- The `_target` can be:
	- `_blank`. Opens the link to a new tab.
	- `_self`. Opens the same tab (default).
### Multimedia
- An alternative (`alt`) must always be provided for accessibility.
- Audio can use:
	- `autoplay` to automatically start playing the audio.
	- `loop` to repeat the audio once it ends.

```html
<!-- Images -->
<img src="image" alt="Alternative text"/>

<!-- Images can be grouped inside a figure -->
<figure>
	<figcaption>Caption<figcaption>
	<img src="img1"/>
	<img src="img2"/>
	<img src="img3"/>
</figure>

<!-- Audio -->
<audio src="audio"></audio>

<!-- Videos -->
<video	src="video" alt="Alternative text"></video>

<!-- Several sources can be provided (also for audio) -->
<video alt="Alternative text">
	<source src="video.mp4" type="video/mp4"/>
	<source src="video.ogg" type="video/ogg"/>
	<source src="video.webm" type="video/webm"/>
</video>

<!-- Time and dates -->
<time datetime="datetime">text</time>
```

- Areas inside images can be defined: [Image Map (w3schools.com)](https://www.w3schools.com/html/html_images_imagemap.asp).
### Lists
```html
<!-- Ordered list -->
<ol>
	<li>List element</li>
</ol>

<!-- Unordered list -->
<ul>  
  <li>List element</li>
</ul>

<!-- Definition list -->
<dl>
	<dt>Element</dt>
		<dd>Definition</dd>
</dl>
```

### Tables

- `<table>` is used for creating a table.
- `<thead>`, `<tbody>` and `<tfoot>` are used to define the structure.
- `<tr>` is used for creating a table row.
- `<th>` is used for creating a table header cell.
- `<td>` is used for creating some table data cell.
- Attributes `colpan` and `rowspan` are used to expand cells.
- Table columns can be grouped with `<colgroup>`

```html
<table>
	<caption>Table title</caption>
	<thead>
		<tr>  
		    <th>Table Header</th>
		</tr>
	</thead>
	<tbody>
		<tr>  
		    <td>Table Data</td>  
		</tr>
	</tbody>
	<tfoot>
		<tr>  
		    <td>Table foot</td>  
		</tr>
	</tfoot>
</table>
```
### Forms

- Input type can be: `text`, `password`, `date`, `submit` or `reset`

```html
<form>
	<!-- To create a grouping with a legend (Not required) -->
	<fieldset>
	    <legend>Personal details</legend>

		<!-- Input for a form -->
	    <label for="firstname">First name:</label>
	    <input type="text" id="firstname" name="firstname"/>
	    
   </fieldset>

	<!-- To specify input length-->
	<input type="text" minlength="5" maxlength="9">
</form>
```

---