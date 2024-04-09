
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
h1 {
	text-align: center;
	font-size: 300%;
}
```
### Using IDs
```css
/* All h1 will have this style */
#id {
	text-align: center;
	font-size: 300%;
}
```
### Using Classes

```html
<html>
	<head>
		<style>
			#header1 {text-align: center;}
			.red_headers {color:red;}
			h1 {font-size: 300%;}
		<style>
	</head>
	
	<body>
		<h1 id="header1" class="red_headers">Header</h1>
	<body>
</html>
```