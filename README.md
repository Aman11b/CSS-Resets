### Essentaial codes

## CSS-Resets
General every time needed CSS code 

```
    *,
    *::before,
    *::after {
      box-sizing: border-box;
    }
    
    
    html {
      -moz-text-size-adjust: none;
      -webkit-text-size-adjust: none;
      text-size-adjust: none;
    }
    
    html:focus-within {
      scroll-behavior: smooth;
    }
    
    
    body,
    h1, h2, h3, h4, p,
    figure, blockquote, dl, dd {
      margin: 0;
    }
    
    
    body {
      min-height: 100vh;
      line-height: 1.5;
      text-rendering: optimizeSpeed;
      font-family: inherit;
    }
    
    
    h1, h2, h3, h4,
    button, input, label {
      line-height: 1.1;
    }
    
    
    h1, h2,
    h3, h4 {
      text-wrap: balance;
    }
    
    
    a:not([class]) {
      text-decoration-skip-ink: auto;
      color: currentColor;
    }
    
    
    img, picture {
      max-width: 100%;
      display: block;
    }
    
    
    input, button,
    textarea, select {
      font-family: inherit;
      font-size: inherit;
    }
    
    
    textarea:not([rows]) {
      min-height: 10em;
    }
    
    
    :target {
      scroll-margin-block: 5ex;
    }
    
    
    ul[role='list'],
    ol[role='list'] {
      list-style: none;
    }
```
```
    
    .my-element {
      font-size: clamp(2rem, calc(1rem + 5vw), 10rem);
    }
```
```
    
    p, li, blockquote:not([class]) {
      max-width: 50ch;
    }

```
    h1, h2, h3 {
      max-width: 20ch;
    }

```
    
    :root {
      --clr-primary: #0042bf;
      --space: 1rem; /* Example variable name corrected */
      --step-size: 0.5rem; /* Example variable name corrected */
      --gutter: 1rem;
      --border-radius: 0.25rem;
      --transition-base: 200ms;
      --tracking: normal;
    }
```
```
    
    body {
      color: var(--clr-primary);
      background: #f9f9f9; /* Example background color */
      font-size: 16px;
      letter-spacing: var(--tracking);
    }
```
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




