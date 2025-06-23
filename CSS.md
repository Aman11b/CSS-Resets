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

   input:focus, textarea:focus, select:focus {
     outline: 2px solid #007bff;
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

   .sr-only{
     clip-path:inset(100%);
     clip:rect(0 0 0 0 );
     height:1px;
     overflow:hidden;
     position: absolute;
     white-space:nowrap;
     width:1px
   }

   :root{

   }

   @media screen and (max-width: 375px) {
   }

   @media only screen and (min-width: 764px) and (max-width: 1024px) {
   
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
## Methodologies and architectures

### BEM (Block, Element, Modifier)
+ divide UI into independent blocks
+ blocks can have elements
+ both block and element can have modifier

1. block -> standalone entity that is meaninginful nav, list, card etc
2. element -> no standalone meaning not standalone but semantically tied to tied to block  nav > item  , list>item , card >title
3. modifier -> flog on block or element to chnage appearance or behaviour   selected, disabled, highlighted, checked

```
/* Block component */
.btn {}

/* Element that depends upon the block */ 
.btn__price {}

/* Modifier that changes the style of the block */
.btn--orange {} 
.btn--big {}
```

```
<nav class='nav'>
   <ul class='nav__list'>
      <li class='nav__item'>
         <a href="/about" class='nav__link nav__link--active'>About</a>
      </li>
      <li class='nav__item'>
         <a href='/pricing' class=''nav__link>Pricing</a>
      </li>
   </ul>
</nav> 
```
+ .nav -> class represent the main block
+ .nav__list represent each item in the navigation list
+ .nav__list--active this for additional styling


