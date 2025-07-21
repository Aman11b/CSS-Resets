### CSS preprocessors are scripting languages that extend the capabilities of CSS, enabling you to write more maintainable and reusable code

1. SCSS (Sassy CSS)
   + .scss (extention)
   + valid css is valied in scss
   + required {} and :
2. Sass (Indented Syntax)
   + .sass
   + indentation required

### Variables
> its like custom porperty in css

```scss
$primary-color: #ff000
$font-size: 1.2rem;

.button{
  color:$primary-color;
  font-size: $font-size
}

```

### nesting
```scss
  nav{
    ul{
      margin:0;
    }
    li{display:block;}
    a{
      padding:block;
    }
  }
```

### Partials and @use

in _variable.scss we can have variables and then we can import it via @use
```scss
@use 'variables';
.button{
color:pink;
}
```

### Mixins
> reusable block of CSS can be used in multiple selector

```scss
   @mixin breakpoint($size){
      @if $size == mobile {
         @media (min-width: 30em){
            @content;
         }
      }
      @else if $size == tablet{
         @media (min-width:48em){
            @content;
         }
      }
   }
   .testimonials{
      display:flex;fle
      x-direction:column;
      @include breakpoint(mobile){
         flex-direction:row;
      }
   
   }
```

### Extend

```scss
.message{
   border:1px solid #ccc;
}
.success{
   @extend .message;
   border-color:green;
}


```


  
