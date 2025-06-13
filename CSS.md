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
