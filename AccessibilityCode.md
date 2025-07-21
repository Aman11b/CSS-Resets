# Common accessibility best practices

## semaintic well -structured HTML
> user appropirate HTML element for intended purpose
```html
<header>
 <nav>
   <ul>
     <li><a href='/about'>About</a></li>
     <li><a href='/pricing'>Pricing</a></li>
     <li><a href='/contact'>Contact</a></li>
   </ul>
 </nav>
</header>
```

## Sufficient color contrast
> color contrast between background and text is critical

## HSL\HSLa (Hue saturation lightness alpha)
>HSL model was created as an alternative to RGB color model and more closely aligns with how human perceive color

>Hue is qualitative wayn to describe color red 0 green 120 blue 240

>Saturation is intensity of color (0-100) %

>Lightness (color's light or dark character)

> alpha is opacity 0.0 (fully transparent) 1.0 (fully opaque)

+ Deuteramopia (green blind) reduced sensitivity to green light
+ Protanopia (red blind) reduced sensitivity to red color
+ Achromatopsia or monochromatism (complete color blind)
  
### calculate color contrast
> uses relative luminance [ color value ]:1

> 21:1 hightes pure black again pure white

>(L1+0.05)/(L2+0.05)

>L1 (lighter color) L2(Darker color)

> 4.5:1 is minimum for regular size text include image of text

> 3:1 for large size text and icons

+ @prefer-color-scheme (to create dark theme)
+ @prefer-contrast (high contrast)

## Text alternative for image and media
> porviding text alt for non-text content such as image icon media
```html
<img src='' alt = 'Two dogs running throght a field'>
```
## Keyboard-accessible navigation and functionality
>example
```html
<button aria-haspopup='dialog'
        aria-expanded='false'
        onClick='openModel()'>Open Model
</button>
```
## Captions and transcripts for audio/video
```html
<video src='my-video.mp4' controls>
  <track src='captions.vtt' kind='captions' srclang='en' label='English'>
</video>
```
+ caption - > text versions of speech and other important audio content
+ Transcript -> transcript should include descriptions of important audio information (like laughter) and visual information (such as someone entering the room).
+ Audio Descriptions -> Audio descriptions help users with visual disabilities perceive content that is presented only visually

## Descriptive link text and headings
> Wraps the most descriptive part of the text with an anchor tag.
```html
View our <a href="/products">latest products</a>.
```

## Forms with proper labeling and error handling
```html
<label for="email">Email</label>
<input type="email" id="email" name="email" autocomplete="email" required>
```

## Interactive elements must have discernible text
```html
<a aria-label="Follow Frontend Mentor on X" href="https://www.x.com/frontendmentor">
  <svg>
    <!-- SVG content -->  
  </svg>
</a>
```

## Visually Impared accessibility

### lables
> label should be assigned to input
```html
  <lable for='name' >Name</lable>
  <input id='name' type='text'/>
```
> label without lable tag
```html
<input aria-lable='Name' type='text' />
```

## toast mesages
> when data pops up on screen
```html
<div data-container aria-live='polite'></div>
```
+ off
+ assertive -> disturb and informs (immidiate)
+ polite -> wait and then inform


### Image
> Alt text is important
```html
<img src='' alt='' />
```

## User semantic HTML
> main aside nav h1(prolly one) h2 h3 h4 h5 (to use hierarchy) header section article button
### link
```html
<a href=''>Click to view something ( detailed)</a>
```
+ zoom in out wokring fine
+ contact info (without visuals)
+ test with screen reader

## Keyboard Accessibility

### tab index
>positive tabindex makes it first to access (changes sequence)

>Tab index should be 0(tabable) eg make div tab-able

> -1(doesnt do anything make you skip that) user cant access
```html
<button>One</button>
<button tabIndex='3'>Two</button>
```

### skip link
> directly to the main content

## Audio Impaired Accessibility
> Audio Description and closed captions
> Different ways of contacting

## Mobility Impaired accessibility
> clickable button spaced around

> make aria large enough to click

> dont include time based things

### Other accessibility features 
```css
@media (perefer-reduced-motion){
 *{
   animation: none !important;
 }
}
```
> swap font feature

> Auto focus
```html
<input autofocus />
```
> mobile friendly design

### tools
> lighthouse

> eslint-plugin-jsx-ally










  
