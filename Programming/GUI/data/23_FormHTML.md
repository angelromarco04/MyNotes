
---
# HTML Forms

[Back to index](../index.md)

---
## Creating a Form
```html
<form>
	<!-- To create a grouping with a legend (Not required) -->
	<fieldset>
	    <legend>Personal details</legend>

		<!-- Text input -->
	    <label for="firstname">First name:</label>
	    <input type="text" id="firstname" name="firstname"/>
	    
   </fieldset>

	<!-- To specify input length-->
	<input type="text" minlength="5" maxlength="9">
</form>
```