
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
		
		<!-- Text input (with max length) -->
	    <label for="firstname" maxlength="15">First name:</label>
	    <input type="text" id="firstname" name="firstname"/>
		
		<input type="radio" id="male" name="firstname"/>

		<!-- Date input -->
	    <label for="birth">Birth date:</label>
	    <input type="date" id="birth" name="birth"/>
	    
		<!-- Password input (with min length) -->
	    <label for="pwd" minlength="8">Password:</label>
	    <input type="password" id="pwd" name="pwd"/>
		
	</fieldset>
	
	<!-- Submit and reset inputs -->
	<input type="submit" value="Submit">
    <input type="reset" value="Reset">
	
</form>
```