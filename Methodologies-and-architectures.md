# Methodologies and architectures

## BEM (Block, Element, Modifier)
+ divide UI into independent blocks
+ blocks can have elements
+ both block and element can have modifier

1. block -> standalone entity that is meaninginful nav, list, card etc
2. element -> no standalone meaning not standalone but semantically tied to tied to block  nav > item  , list>item , card >title
3. modifier -> flog on block or element to chnage appearance or behaviour   selected, disabled, highlighted, checked

```css
/* Block component */
.btn {}

/* Element that depends upon the block */ 
.btn__price {}

/* Modifier that changes the style of the block */
.btn--orange {} 
.btn--big {}
```

```html
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

## CUBE CSS (Composition, utility, block, exception)
+ most of the work is alredy done for you with global and high-level styles
+ colors trpography other global styles are defined first

1. Composition -> how different part of page fit together
2. utility -> small single purpose class used to modify appearance of element
3. block -> main building block like cards header footer section button
4. Exception -> exception are styles taht deviate from the global and block level styles  added via data attributes


```html
<nav class = 'nav'>
   <ul class='[ nav__list ] [ flex flex-wrap ] [ gap-sm ]'>
      <li class="nav__item">
         <a href="/about" class="[ nav_link ] [ padding-sm ]" data-state="active">About </a>
      </li>
      <li class="nav__item">
         <a href="/pricing" class="[nav__link] [paddin-sm]">Pricing</a>
      </li>
   </ul>
</nav>
```
1. composition      .flex  .flex-wrap create a flexible ,wrapping layout
2. Utility   .gap-sm .padding-sm  reusable style applied across component
3. Blocks.nav .nav__list .nav__item .nav__link
4. Exception  data-state="active"
> [] as we dont apply style to bracket they are ignored by html and css

## SMACSS (Scalable and Modular Architecture for CSS)
1. Base   ->default element style such as html body a etx
2. Layout ->pages into major section,one or mor emodule holds header footer main etc
3. Module ->reuasable modular part navigation fomr lists
4. State  ->describe how modules and layour will look in a particular state   hidden expanded, active inactive
5. Theme  ->visula styling applied across different section/page to provide oncsistant look and feel   dark light theme

```html
<nav class="nav">
  <ul class="nav-list">
    <li class="nav-item">
      <a href="/about" class="nav-link is-active">About</a>
    </li>
    <li class="nav-item">
      <a href="/pricing" class="nav-link">Pricing</a>
    </li>
    <li class="nav-item">
      <a href="/contact" class="nav-link">Contact</a>
    </li>
  </ul>
</nav>
```

1. base.css > body{} a{}
2. layout.css  > header{}
3. module.css > .nav{}  .nav-list{}  .nav-item{}  .nav-link{}
4. state.css  > .nav-link.is-active{}
