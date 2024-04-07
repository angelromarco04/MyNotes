
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