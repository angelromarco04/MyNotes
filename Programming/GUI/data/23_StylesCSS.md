
---
# Webpage Styling

[Back to index](../index.md)

---
## CSS Syntax

```css
/* GENERAL */
selector {
	propertie:value;
	...
}

/* EXAMPLE */
h1 {
	color:red;
}
```
## CSS Selector

### Basic
```css
/* All h1 will have this style */
/* Used to apply a style to all elements of a tag */

h1 {
	text-align: center;
	font-size: 300%;
}
```
### Using IDs
```css
/* Each element can have ONE UNIQUE id */
/* Used to apply a style to a specific element */
/* Example: <h1 id="header1">...</h1> */

#header1 {
	text-align: center;
	font-size: 300%;
}
```
### Using Classes
```css
/* Each element can have one or several classes */
/* Used to apply a style to related elements */
/* Example: <h1 class="centered big">...</h1> */

.centered {
	text-align: center;
}
.big {
	font-size: 200%;
}

/* Applied only to h1 that are big */
h1.big {
	font-size: 300%;
}
```