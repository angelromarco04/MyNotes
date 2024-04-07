
---
# HTML Forms

[Back to index](../index.md)

---
## Structure of  a Form
```html
<form>
	<!-- To create a grouping with a legend (Not required) -->
	<fieldset>
	    <legend>Legend</legend>
		...
		
	</fieldset>
	
	<!-- Submit and reset inputs -->
	<input type="submit" value="Submit">
    <input type="reset" value="Reset">
	
</form>
```
---
## Form Attributes
```html
<!-- Perform an action of a php file -->
<form action="/action.php"> ... </form>

<!-- Data sent by URL (Do not use for sensitive data) -->
<form action="/action.php" method="get"> ... </form>

<!-- Data sent by an HTTP post -->
<form action="/action.php" method="post"> ... </form>
```
---
## Form Elements
### Input
```html
<form>
	<!-- Text input (with max length) -->
	<label for="name">First name:</label>
	<input type="text" id="name" name="name" maxlength="15"/>

	<!-- Input with predefined options -->
	<label for="browser">Browser:</label>
	<input id="browser" name="browser" list="browsers">  
	<datalist id="browsers">  
	    <option value="Chrome">
	    <option value="Firefox">
	</datalist>
	
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
</form>
```
### Select
```html
<form>
	<label for="car">Choose your car:</label>
	
	<!-- Pannel for selecting from several options -->
	<!-- We see 2 options at once (1 by default) -->
	<!-- We allow multi-select values (Forbiden by default) -->
	<select id="car" name="car" size="2" multiple>
	
		 <!-- This is an option -->
		 <option value="volvo">Volvo</option>
		 
		 <!-- This is the default option -->
		 <option value="fiat" selected>Fiat</option>  
	</select>
</form>
```
### Text area
```html
<textarea name="message" rows="10" cols="30">  
	Write here your message.  
</textarea>
```