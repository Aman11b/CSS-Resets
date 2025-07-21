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

```css
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
```css
.btn {
  transition: transform 250ms cubic-bezier(0.1, 0.2, 0.3, 0.4);
}
```
>  https://cubic-bezier.com/#.17,.67,.83,.67

### transition can take number of values but only two are important
1. the name of the porperty we wish to animate
2. the duration of the animate

## Animation Performance
1. transform and opacity are cheap to animate
2. GPU (hardware-accelerated)ad CPU handle aniamtion differently
3. will-change (porperty hinf browser that we are going to animate thie element) -> hardware accelerated

### UX touched
1. Deplay -> (transition-delay)
```css
  .dropdown {
    opacity: 0;
    transition: opacity 400ms;
    transition-delay: 300ms;
  }
  .dropdown-wrapper:hover .dropdown {
    opacity: 1;
    transition: opacity 100ms;
    transition-delay: 0ms;
  }
```
# CSS Animations

1. Multiple keyfrarmes -> allow for more complex and detailed animation
2. greater control -> more control over intermediate state
3. Loopeing and alteration -> can loop indefinately or alter between forward anf backwards

### when to user animation 
1. creating loading or spinning progress bar
2. animating elment along a path or tragetory
3. implementing multi step animation with different stages
4. creating standalone animation
```css
@keyframe pulse{

  0%{
    transform: scale(1);
  }
  50%{
    transform: sacle(1.2);
  }
  100%{
    transform: scale(1);
  }
  
}
.element{
  animation: pulse 1s infinite;
}
```
