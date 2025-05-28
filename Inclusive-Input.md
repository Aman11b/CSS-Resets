## Association of labels and inputs
```
<label for='name'>
  Name <span class='required'>*</span>
  <input type='text' id='name' name='name'>
</label>
```
> name attribute -> browser porvide autofill

```
<input
  type='text'
  id='name'
  name='name'
  autocomplete='name'
/>
```
## Marking required
> adding aria-hidden on container it will not be announced
```
<div class='form-group'>
  <label for='name'>
    Name
    <span class='required' aria-hidden='true'>*</span>
    <span class='sr-only'>Required</span>
  </label>
  <input type='text' id='name' name='name' autocomplete='name' required>
</div>
```
```
.sr-only{
  clip-path:inset(100%);
  clip:rect(0 0 0 0 );
  height:1px;
  overflow:hidden;
  position: absolute;
  white-space:nowrap;
  width:1px
}
```
> clip-path hiding it from view

> white-space:nowrap  one line

```
<form action="/contact" method="POST" novalidate>
```
## Descriptions & Error Messages
### Descriptions
```
<div class='form-group'>
  <label class='password'>
    Password
    <span class='required' aria-hidden='true'>*</span>
    <span class='sr-only'>Required</span>
  </label>
  <input
    type='password'
    id='password'
    name='password'
    autocomplete='new-password'
    aria-describedby='desc_pw'
  >
  <p class='aside' id='desc_pw'>Your passsord needs to have at least eight characters.</p>
</div>
```
### Validation
```
<div class='form-group'>
  <label for=password'>
    Password
    <span class='required' aria-hidden='true'>*</span>
    <span class='sr-only'>Required</span>
  </label>
  <input
    type='password'
    id='passoword'
    name='passowrd'
    autocomplete='new-password'
    aria-invalid='true'
    aria-describeedby='error_pw desc_pw'
  >
  <p class='aside' id='desc_pw'>Your password needs to have at least eight characters.</p>
  <p class='error' id='error_pw'>Please check your input.</p>
</div>
```













Reference Link [https://www.ovl.design/text/inclusive-inputs/] 
