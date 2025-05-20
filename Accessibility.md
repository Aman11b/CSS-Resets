## Web Accessibilty

# Intro to web assessibility 

+ screen reader (blind) - titles are imp | well structure | link text | alt text (all very imp)
+ Digital braille display & voice over (deaf and blind)
+ captions  & transcripts (deaf and sighted)

# user web without mouser
+ Tab -> move to next link,element,button
+ Shiht + Tab -> previous Link, form element button
+ Enter -> activates curremt button, link

# large text wrapping
+ wrapped text -> avoid horizontal and vertical scrolling

# Range of ability
1. auditory
2. cognitive
3. physical
4. speech
5. visual

# Assessibility perspective
1. video caption
2. color contrast (backgournd and fore ground)
3. voice recognition
4. text to speech
5. good layout & consistancy
6. notification and feedback
7. Customisable text (size spacing color)
8. understandable content
9. keyboard compartabilty

# Assistive Technologies
> hardware/software that enable people with disability to interact and engage with digital env eg. screen reader
# Adaptive Statergies
> techniques people user to interact with digital env eg. changing browser setting


## Physical Disability

# keyboard accessibility
>(anchor form controls img map area) receive keybaord focus but <span> <div> not hence has to make them interactive.
>hover need porper coading too
>Focus state and focus order is imp
>Skip links(direct to main)

## fly-out funtionality
# Mouse User
```
nav > ul li ul{Display: none;}
nav > ul li:hover{Display: block;}
```
```
var menuItems = document.querySelectorAll('li.has-submenu');
Array.prototype.forEach.call(menuItems, function(el, i){
	el.addEventListener("mouseover", function(event){
		this.className = "has-submenu open";
		clearTimeout(timer);
	});
	el.addEventListener("mouseout", function(event){
		timer = setTimeout(function(event){
			document.querySelector(".has-submenu.open").className = "has-submenu";
		}, 1000);
	});
});
```
# keyboard User
>User parent as toggle
```
var menuItems = document.querySelectorAll('li.has-submenu');
Array.prototype.forEach.call(menuItems, function(el, i){
	el.querySelector('a').addEventListener("click",  function(event){
		if (this.parentNode.className == "has-submenu") {
			this.parentNode.className = "has-submenu open";
			this.setAttribute('aria-expanded', "true");
		} else {
			this.parentNode.className = "has-submenu";
			this.setAttribute('aria-expanded', "false");
		}
		event.preventDefault();
		return false;
	});
});
```

## Switch controls
> another ways to interact with digital content if mouse keyboard voice and gensture is not possible
 ## Sip-and-puff switch
   > sipping straw ->Tabbing
   > Puffing straw -> Clicking
 ## Button Switch
   > can be activate by hand foot or head
 ## camera Switch
   > activate by tilting the head into a camera
 ## Eye Tracking
   > measuring point of gaze or mpthing o an eye relative to head

## speech Input
> make space for scrolling dialog box
> make sure system focus is clearly visible
> allow user to customize keyboard shotcuts

## Browsing without mouse
1. Navigation to most element  -> tab , Shift+tab(backwards)
2. Link -> Enter
3. Button -> Enter / Space
4. Checkbox -> Spacebar
5. Radio buttons -> arrow keys
6. Select menu -> up donw arrow to select the option spacebar to expand
7. autocomplete -> type, arro keys navigation enter complete
8. Dialog -> Esc close
9. Slider -> arrow keys, Home/End  Begin or end
10. Menu Bar -> arroe keys and enter
11. Tab panel -> tab and arrow keys
12. Tree menu -> arrow keys
13. Scroll -> arrow keys-> horizibtal vertical , Spacebar/shift -> scroll by page


## Blindness
> user screen readers
> text alt for img button controls video
> Video AD audio description and text transcription

## Screen Reader
1.reads text heading lists buttons text alt for imag and form input
2.when coaded properly screen reader announce name role and state of element
3. built-in keyboard , jumps between heading lists form element links and navigation sequence























  
  
