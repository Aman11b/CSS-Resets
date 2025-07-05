# CSS transitions
> transition between to state of element smoothly

1. smooth interposlation between an elments; property
2. triggered by state change
3. limited to two starting and ending state
4. simpler syntax then animation

> best suited for simpler state change
1. changing color backgroud border on hover
2. soomthy expanding or colapsing an element when class is added or removed
3. smmothy chnage border color or form field when gains focus
4. displaying dropdown when hovering over parent

```
.button{
  background-color: #3498db;
  transition: backgroud-color 0.3s ease;
}
.button:hover{
  backgroud-color: #2980b9;
}
```
### Easing functions
> rate at which porperty chnagess
1. liner -> constant
2. ease -> start slow speed up in the middle and slow down (default)
3. ease-in -> start slow ,progressively gets faster untill end
4. ease-out -> start fast, progessively gets slower ubtill the end
5. ease-in-out ->similar to ease faster acceleration in between
> using cibic-bezier() define custom easing curve
```
.btn {
  transition: transform 250ms cubic-bezier(0.1, 0.2, 0.3, 0.4);
}
```
>  https://cubic-bezier.com/#.17,.67,.83,.67
