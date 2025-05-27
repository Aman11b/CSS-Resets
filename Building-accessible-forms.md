## Use native HTML form controls
```
  <label for='first-name'>First Name</label>
  <input type='text' id='first-name' name='first-name'>
```
## Provide visible labels
```
<label for='email'>Email</label>
<input type='email' id='email' name='email'>
```
# label controls
```
<input type='text' name='search' aria-labelledby='searchbutton'>
<button id='searchbutton' type='submit'>Search</button>
```
## Group related fields
```
<fieldset>
  <legend>Choose your favorite color</legend>
  <input type='radio' id='red' name='color' value='red'>
  <label for='red'>Red</label>
  <input type='radio' id='blue' name='color' value='blue'>
  <label for='blue'>Blue</label>
  <input type='radio' id='green' name='color' value='green'>
  <label for='green'>Red</label>
</fieldset>
```
## Provide clear instructions
```
<label for='username'>Username</label>
<imput type='text' id='username' name='username' aria-describeby='username-instructions' required>
<p id='username-instructions'>Choose a unique username between 4 and 20 characters.</p>

```

## Enable auto-completion
```
<label for='name'>Full Name</label>
<input type='text' id='name' name='name' autocomplete='name'>
```
## Ensure keyboard accessibility
```
input:focus,textarea:focus,select:focus{
  outline: 2px solid #oo7bff;
}
```













