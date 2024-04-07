
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
	    <label for="name">First name:</label>
	    <input type="text" id="name" name="name" maxlength="15"/>
		
		<!-- Radio buttons input -->
		<input type="radio" id="male" name="sex"/>
		<label for="male">Male</label>
		
		<input type="radio" id="female" name="sex"/>
		<label for="male">Female</label>
		
		<!-- Checkboxes input -->
		<input type="checkbox" id="dev1" name="dev1" value="PC">  
		<label for="device1"> I have a PC</label>
		
		<input type="checkbox" id="dev2" name="dev2" value="Phone">
		<label for="device2"> I have a phone</label><br>
		
		<!-- Date input -->
	    <label for="birth">Birth date:</label>
	    <input type="date" id="birth" name="birth"/>
	    
		<!-- Password input (with min length) -->
	    <label for="pwd">Password:</label>
	    <input type="password" id="pwd" name="pwd" minlength="8"/>
		
	</fieldset>
	
	<!-- Submit and reset inputs -->
	<input type="submit" value="Submit">
    <input type="reset" value="Reset">
	
</form>
```
---
## Form Attributes
```html
<!-- Perform an action --
<form action="/action.php"> ... </form>
```