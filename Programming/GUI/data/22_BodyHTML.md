
---
# Webpage Body

[Back to index](../index.md)

---
## Body Layout

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
---
## Basics
### Basic Text
```html
<!-- Headers (bigger to smaller) -->
<h1> ... </h1>
<h2> ... </h2>
<h3> ... </h3>
<h4> ... </h4>
<h5> ... </h5>
<h6> ... </h6>

<!-- Text paragraph -->
<p>...</p>

<!-- Line break -->
<br/>

<!-- Horizontal rule. Used to separate contents. -->
<hr/>
```
### Formatting Text
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
---
## Multimedia
### Links
```HTML
<!-- Basic link -->
<a href="http://page.com" > Link </a>

<!-- Basic link (Open in same tab. Default) -->
<a href="http://page.com" target="_self" > Link </a>

<!-- Basic link (Open in other tab) -->
<a href="http://page.com" target="_blank" > Link </a>

<!-- Section link -->
<a href="#section" target="_target"> Go to section </a>

<!-- Email link -->
<a href="mailto:name@example.com"> Send Email </a>

<!-- Phone call link -->
<a href="tel:+1234567890"> Call Us </a>

<!-- SMS link -->
<a href="sms:+1234567890"> Send SMS </a>
```
### Images
```html
<!-- Images (Mandatory alt text for accessibility) -->
<img src="image" alt="Alternative text"/>

<!-- Grouping of images with a caption -->
<figure>
	<figcaption>Caption<figcaption>
	<img src="img1"/>
	<img src="img2"/>
	<img src="img3"/>
</figure>
```
### Audio & Video
```html
<!-- Audio -->
<audio src="audio"></audio>

<!-- Video -->
<video	src="video" alt="Alternative text"></video>

<!-- Several sources can be provided (also for audio) -->
<video alt="Alternative text">
	<source src="video.mp4" type="video/mp4"/>
	<source src="video.ogg" type="video/ogg"/>
	<source src="video.webm" type="video/webm"/>
</video>
```
### Date & Time
```html
<!-- Simple datetime -->
<time>20:00</time>

<!-- Full datetime -->
<time datetime="">text</time>
```