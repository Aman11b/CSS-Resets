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

```
$primary-color: #ff000
$font-size: 1.2rem;

.button{
  color:$primary-color;
  font-size: $font-size
}

```

### nesting
```
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
```
@use 'variables';
.button{
color:pink;
}
```



  
