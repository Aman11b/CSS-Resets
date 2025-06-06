# WAI-ARIA
##  Web Accessibility Initiative – Accessible Rich Internet Applications

> additional semantics to describe role state porperties interactions and dynamic content updates.

### landmark
> identify cirtical areas of the page
```
  <form role='search'></form>
```
### Regions
+ role= 'region' with aria-label or aria-labeledby
> define a section pf the page as perceivable section
```
<section aria-labelledby='testimonial-heading'>
  <h2 id='testimonial-heading'>
    What poeple have said about us
  </h2>
</section>
```
### Labels
+ aria-label
+ aria-labelledby
+ aria-describeby
> porvide accessible names and descriptions for element
```
<button aria-label='Close modal'>X</button>
```
### Live regions
+ aria-live
+ aria-atomic
+ aria-relevant
> announce dynamic content updates to asistive technologies
```
<span class='error-message' aria-live='polite'>
</span>
```

