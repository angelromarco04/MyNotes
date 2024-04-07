
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
		<input type="checkbox" id="device1" name="device1" value="TV">  
  <label for="vehicle1"> I have a bike</label><br>  
  <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">  
  <label for="vehicle2"> I have a car</label><br>



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