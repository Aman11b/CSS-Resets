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
## WAI-ARIA roles and properties
### landmark roles
+ banner   > top area of page content
+ complemetory  > secondary supporting ocntent
+ contentinfo   > footer or mrtadata info
+ form  > group of input element
+ main   > main central page content
+ navigation   > site or page navigation links
+ region  > significant page section
+ search  > search feature or form

### Widget Roles
+ alert  > importamt popup
+ button  > clickable action control
+ checkbox  > binary chickable input
+ dialog  > modal or popup container
+ gridcell  > cell in data grid
+ link  > navigation hyperlink element
+ listbox  > selectabvle list container
+ menuitem    > item in menu
+ menuitemcheckbox  > menu checkbox option
+ meniitemradio   > menu radio option
+ option  > selectable dropdown item
+ progressbar  > show task completion progress
+ radio  > exclusinve choice selector
+ slider  > value adjuster via drag
+ scrollbar  > scroll controll for content
+ spinbutton  > numeric input with arrows
+ status  > synamic status message
+ tab  > switch between two pannels
+ tabpanel > content pannel for a tab
+ textbox > text input field
+ timer > display running time
+ tooltip > hover information popup

### Document Structure Roles
+ article -> standalone complete content
+ columheader ->table column header cell
+ definition ->term or concept explanation
+ directory ->hierarchical list of item
+ document ->entire document container
+ group ->related element container
+ heading ->section or content title
+ img ->image with descriptiom
+ list ->collection of list item
+ listitem ->item of list
+ math ->mathematical expression block
+ note ->supplementay note content
+ presentation ->pure visual layout only
+ row ->table or grid row
+ rowgroup ->group of table rows
+ rowheader ->table row header cell
+ seperator ->divider between container
+ toolbar ->set of user controls

1. aria-label    -> user when no visible lable
2. aria-labelledby    ->refer to ID of visible lable element
3. aria-describledby   ->refer ot help text element
4. aria-live   ->auto read content update

```
<div role='dialog' aria-labelledby='dialog-title' aria-describedby='dialog-description'>
  <h2 id='dialog-title'>Delete comment</h2>
  <p id='dialog-description'>Arue you sure you want to delete this comment? this action cannot be undone.</p>
  <button>Cancel</button>
  <button>Confirm</button>
</div>
```










