 ## Visually Impared accessibility

# lables
> label should be assigned to input
```
  <lable for='name' >Name</lable>
  <input id='name' type='text'/>
```
> label without lable tag
```
<input aria-lable='Name' type='text' />
```

# toast mesages
> when data pops up on screen
```
<div data-container aria-live='polite'></div>
```
+ off
+ assertive -> disturb and informs (immidiate)
+ polite -> wait and then inform
  
