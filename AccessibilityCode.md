# Common accessibility best practices
 
# Visually Impared accessibility

## lables
> label should be assigned to input
```
  <lable for='name' >Name</lable>
  <input id='name' type='text'/>
```
> label without lable tag
```
<input aria-lable='Name' type='text' />
```

## toast mesages
> when data pops up on screen
```
<div data-container aria-live='polite'></div>
```
+ off
+ assertive -> disturb and informs (immidiate)
+ polite -> wait and then inform


### Image
> Alt text is important
```
<img src='' alt='' />
```

## User semantic HTML
> main aside nav h1(prolly one) h2 h3 h4 h5 (to use hierarchy) header section article button
### link
```
<a href=''>Click to view something ( detailed)</a>
```
+ zoom in out wokring fine
+ contact info (without visuals)
+ test with screen reader

# Keyboard Accessibility

## tab index
>positive tabindex makes it first to access (changes sequence)

>Tab index should be 0(tabable) eg make div tab-able

> -1(doesnt do anything make you skip that) user cant access
```
<button>One</button>
<button tabIndex='3'>Two</button>
```

## skip link
> directly to the main content

# Audio Impaired Accessibility
> Audio Description and closed captions
> Different ways of contacting

# Mobility Impaired accessibility
> clickable button spaced around

> make aria large enough to click

> dont include time based things

# Other accessibility features 
```
@media (perefer-reduced-motion){
 *{
   animation: none !important;
 }
}
```
> swap font feature

> Auto focus
```
<input autofocus />
```
> mobile friendly design

# tools
> lighthouse

> eslint-plugin-jsx-ally










  
