## JS Codes

## document object
```
document.getElementById('titlt');  //faster
document.getElementByClassName('selected');
document.querySelector('#title');
document.querySelectorAll('.selected')
```

## DOM manipulation

```
const paragrah ==document.querySelector('p');
paragraph.textContent= 'Hello';
paragraph.style.color= 'red';
paragraph.remove();
document.body.appendChild(paragraph);

```

## Update DOM

```

button.className = 'active';
button.classList.add ('hidden');
button.classList.toggle('active');
button.classList.remove ('hidden);

```

## Event Listerner

```
cont button = document.querySelector ('button');

//direct assignment
button.onclick = function () {
console.log('You clicked me !')
}

//addEventListerner
button.addEventListerner('click',function(){
console.log('you clicked me!)})

```

## Funtion Definitions

```
button.addEventListerner ('click',() => {
console.log(this)});

button.addEventListerner ('click', (event) => {
console.log(event.target);  //element that was clicked
console.log(event.currentTarget); //button (element in which eventlisterner was assigne)
});


```

## Loops

```
const buttons =document.querySelectorAll('button')

for (let i =0; i<buttons.length: i+=1){
buttons[i].addEventListener('click', (e)=>{
screen.style.backgroundColor = e.target.id;});
}
```
```
for(const i in buttons){
buttons[i].addEventListener('click',(e)=>{
screen.style.backgroundColor = e.target.id;})}
```
```
for(const button of buttons){
buttons.addEventListener('click', (e) +>{
screen.style.backgroundColor = e.target.id;})}
```
```
buttons.forEach((button)=>{
buttons.addEventListener('click',(e)=>{
screen.style.backgroundColor = e.target.id;})})
```

##   HTML form

```
   <form id='form' nonvalidate>
      //nonvalidate is to stop html validation
      <div>
         <label for='name'>Name</label>
         <input id='name' name='name' />
         <span aria-live='polite' id='name-error'></span>
      </div>
   </form>
```

## onsubmit

```
const form = document.getElementById('form');
   function handleSubmit (e) {
      e.preventDefault ()
   }
form.addEventListener('Submit',handleSubmit);
```
## retrieveing data from form

```
const form = document.getElementById ("form");

const handleSubmit = (e) => {
   e.preventSubmit(e);

   const fomrDate = new FormData(e.target);  //converted into key/value
   const data = Object.formEntries (formData); // entried into objects

   console.log(data);
};
form.addEventListener("Submit", handleSubmit);

```

## using fetch

```
fetch('/data.json').then((response)=>{
if(!response.ok) return console.log('Oops ! something went wrong');

return response.json();
}).then((data)=>{
console.log(data);
})

```

Updating UI

```
<button id='toggle'>Hiide completed </button>
<ol id='todos-container'></ol>
```
```
const appendItem = (Item) => {
const todo = document.createElement('li');
todo.inneHTML=
`
<span>${item.task}</span>
<input type='checkbox' ${item.completed ? 'checked' : '' }/>
`
constiner.appendChild(todo);
};

```
```
const appenItem = (Item) => {
container.innerHTML +=
`
<li>
<span>${item.task}</span>
<imput type='checkbox' ${item.completed ? 'checked' : '' } />
</li>
`
}
```

## Modifying DOM
```
<button id='toggle'>Hide Completed</button>
<ul id=todos-container' data-completed='true'></ul>

```

```

#todos-container[data-completed=false] li:has(input:checked){
display:none;
}
```
```
conat toggleBtn = document.getElementById('toggle');
const handleToggle = (e) =>{
let displayAll = e.target.textContent === 'Show complted';
container.dataset.completed = diaplayAll
e.target.textContent = displayAll ? 'Hide completed' : 'show completed'
}
```

## Refractor

# Keeping code DRY (Do not Repeat Yourself)
# Break up large functions

```
const form = document.querySelector('form');
const clearError = () =>{}
const renderError = (message) =>{}
const dataIsValid =(name, value) => {}
const handleChange = (e) => {
   clearError();
}
const handleSubmit = (e) => {
   e.preventDefault();
   
   let isValid =true;
   //getting data
   const data =Object.fromEntries(new FormData(e.target));

   //loopig over data
   Object.keys(data).forEach((name)=>{
      if(!dataIsValid(name, data[name])){
         isValid=false;
      }
      });
      if(isValid){
         renderSuccess()
      }else{
         renderError('data invalid')
   }
}
```

## validation
```
const dataIsValid =(key, value) => {
   if(key === 'name'){
      if(!value.trim()) return false;
   }
   if(key === 'email'){
      if(!value || value.length <12) return false;
   }
}
```

# better apparoach

```
const validations ={
name:(value) => !!value.trim(),
email: (value) => value.include('@'),
pasowrd: (value) => value.length >=12,
}

const dataIsValid =(key, value)=>{
   if(!validations[key]) return true; // if there is not validation
   return validations[key](value);
}
```

## coverting it into pure function 
```
const dataIsValid =(key, value, validations) =>{
if(!validations[key]) return false
}
```
