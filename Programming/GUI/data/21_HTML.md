
---
# HTML

[Back to index](../index.md)
### Styling tags
```html
<!-- Used to apply styling to blocks of tags -->
<div id=“someID” class=“someClass”> ... </div>

<!-- Used to apply styling to text fragments -->
<span id=“someID” class=“someClass”> ... </span>
```

### Multimedia
- Audio can use:
	- `autoplay` to automatically start playing the audio.
	- `loop` to repeat the audio once it ends.



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
- Attributes `colspan` and `rowspan` are used to expand cells.
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