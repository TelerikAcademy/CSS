<!-- section start -->
<!-- attr: { class:'slide-title', showInPresentation:true, hasScriptWrapper:true } -->
# CSS Layout
## Control the arrangement of the HTML elements
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic00.png" style="top:51.39%; left:53.53%; width:49.76%; z-index:-1" />  -->

<!-- <img class="slide-image" showInPresentation="false" src="imgs/pic01.png" style="top:51%; left:10.02%; width:40.99%; z-index:-1" />  -->

<div class="signature">
	<p class="signature-course">CSS Styling</p>
	<p class="signature-initiative">Telerik Software Academy</p>
	<a href="https://telerikacademy.com" class="signature-link">https://telerikacademy.com</a>
</div>

<!-- section start -->
<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
# Table of Contents
- [Width and Height](#width)
- [Overflow](#overflows)
- [Display](#display)
- [Visibility](#visibility)
- [Margins and Paddings](#margins-and-paddings)
- [CSS Box Model](#boxmodel)
- [Positioning](#position)
- [Floating](#float)
- [Flexbox](#flex)

<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic02.png" style="top:12.34%; left:56.01%; width:40%; z-index:-1; border-radius: 30px 0 30px 0" />  -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic03.png" style="top:50%; left:64.61%; width:30.86%; z-index:-1" />  -->



<!-- section start -->
<!-- attr: {  class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Width and Height -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic04.png" style="top:40%; left:25%; width:48%; z-index:-1" />  -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic05.png" style="top:43%; left:32%; width:25%; z-index:-1" />  -->


<!-- attr: { id:'width', showInPresentation:true, hasScriptWrapper:true, style:'font-size: 0.9em' } -->
# <a id="width"></a>Width
- The **width** property defines numerical value for the width of element, e.g. `200px`
- Applies only for block elements
  - Their with is `100%` by default
  - The width of inline elements is always the width of their content, by concept
- **min-width**
  - defines the minimal width
  - overrides width if **width < min-width**
- **max-width**
  - defines the maximal width
  - overrides width if **width > max-width**


<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Width
## [Demo](https://github.com/TelerikAcademy/CSS/blob/master/Topics/03.%20CSS-Layout/demos/01.%20width.html) -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic06.png" style="top:55%; left:27.5%; width:45%; z-index:-1" />  -->


<!-- attr: { showInPresentation:true, hasScriptWrapper:true, style:'font-size: 0.9em' } -->
# Height
- The **height** property defines numerical value for the height of element, e.g. `100px`
- Applies only on block elements
  - The height of inline elements is always the height of their content
- **min-height**
  - defines the minimal height
  - overrides height if **height < min-height**
- **max-height**
  - defines the maximal height
  - overrides height if **height < min-height**


<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
# Width and Height Values
- The values of the **width** and **height** properties **are numerical**:
  - Pixels (`px`)
  - Centimeters (`cm`)
  - Ems (`em`)
  - Or percentages
    - A percent of the available width


<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Height
## [Demo](https://github.com/TelerikAcademy/CSS/blob/master/Topics/03.%20CSS-Layout/demos/02.%20height.html) -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic07.png" style="top:55%; left:35%; width:30%; z-index:-1; border-radius: 15px" />  -->


<!-- section start -->
<!-- attr: { id:'overflow', class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # <a id="overflow"></a>Overflow -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic09.png" style="top:45%; left:55%; width:37.91%; z-index:-1;border-radius: 15px" />  -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic10.png" style="top:45%; left:5%; width:38%; z-index:-1;border-radius: 15px" />  -->


<!-- attr: { id:'overflows', showInPresentation:true, hasScriptWrapper:true } -->
# <a id="overflows"></a>Overflow
- The **overflow** property defines the behavior of element when content needs more space than the available
- Values:
  - `visible` (default) – content spills out of the element
  - `auto` – show scrollbars if needed
  - `scroll` – always show scrollbars
  - `hidden` – any content that cannot fit is clipped


<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Overflow
## [Demo](https://github.com/TelerikAcademy/CSS/blob/master/Topics/03.%20CSS-Layout/demos/03.%20overflow.html) -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic11.png" style="top:55%; left:59.88%; width:35.42%; z-index:-1; border-radius: 15px; border: 2px solid white" />  -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic12.png" style="top:55%; left:15%; width:26.45%; z-index:-1; border-radius: 15px; border: 2px solid white" />  -->


<!-- section start -->
<!-- attr: { id:'display', class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # <a id="display"></a>Display -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic13.png" style="top:40%; left:20%; width:60%; z-index:-1" />  -->


<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
# Display
- The **display** property controls the display of the element and the way it is rendered and if breaks should be placed before and after the element
- Values:
  - `inline`: **no breaks are placed** before or after (`<span>` is an inline element)
    - height and width depend on the content
  - `block`:  **breaks are placed** before AND after the element (`<div>` is a block element)
    - height and width may not depend on the size of the content


<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
# Display
- More values:
  - `none`: **element is hidden** and its dimensions are not used to calculate the surrounding elements rendering
    - differs from `visibility: hidden`
  - `inline-block`: **no breaks are placed** before and after (like **inline**)
    - height and width can be applied (like `block`)
  - `table`, `table-row`, `table-cell`: the elements are **arranged in a table-like layout**


<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Display
## [Demo](https://github.com/TelerikAcademy/CSS/blob/master/Topics/03.%20CSS-Layout/demos/04.%20display.html) -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic14.png" style="top:35%; left:5%; width:35%; z-index:-1" />  -->


<!-- section start -->
<!-- attr: { id:'visibility', class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # <a id="visibility"></a>Visibility -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic15.png" style="top:45%; left:28.36%; width:42%; z-index:-1" />  -->


<!-- attr: { showInPresentation:true, hasScriptWrapper:true, style:'font-size: 0.95em' } -->
# Visibility
- The **visibility** property
  - Determines whether the element is visible
  - `hidden`: element is **not rendered, but still occupies place** on the page
    - similar to `opacity:0`
  - `visible`: element is **rendered normally**
  - `collapse`: collapse **removes a row or column**, but it does not affect the table layout
    - only for table elements
    - The space taken up by the row or column will be available for other content


<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Visibility
## [Demo](https://github.com/TelerikAcademy/CSS/blob/master/Topics/03.%20CSS-Layout/demos/06.%20visibility.html) -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic16.png" style="top:55%; left:54.27%; width:35%; z-index:-1" />  -->




<!-- section start -->
<!-- attr: { id:'margins-and-paddings', class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # <a id="margins-and-paddings"></a>Margins and Paddings -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic17.png" style="top:45%; left:20%; width:60%; z-index:-1" />  -->


<!-- attr: { id:'margins', showInPresentation:true, hasScriptWrapper:true, style:'font-size: 0.9em' } -->
# <a id="margins"></a>Margin and Padding
- The **margin** and **padding** properties define the spacing around the element
  - They take numerical value, e.g. `10px` or `-5px`
  - Can be defined for each of the four sides separately – `margin-top`, `padding-left`, …
  - **margin** is the spacing outside of the border
  - **padding** is the spacing between the border and the content
- **Collapsing margins**
  - When the vertical margins of two elements are touching, only the margin of the element with the largest margin value will be honored


<!-- attr: { showInPresentation:true, hasScriptWrapper:true} -->
# Margin and Padding: Short Rules

- Sets all four sides to have margin of `5px`

```css
.container {
    margin: 5px;
}
```


- top and bottom to `10px`, left and right to `20px`

```css
.container {
    margin: 10px 20px;
}
```


<!-- attr: { showInPresentation:true, hasScriptWrapper:true} -->
<!-- # Margin and Padding: Short Rules -->

- top `5px`, left and right `3px`, bottom `8px`

```css
.container {
    margin: 5px 3px 8px;
}
```

- top, right, bottom, left (clockwise from top)

```css
.container {
    margin: 1px 3px 5px 7px;
}
```

- Same for **padding**


<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Margins and Paddings
## [Demo](https://github.com/TelerikAcademy/CSS/blob/master/Topics/03.%20CSS-Layout/demos/07.%20margins-paddings-rules.html) -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic18.png" style="top:55%; left:35%; width:30%; z-index:-1; border-radius: 15px" />  -->

<!-- section start -->
<!-- attr: { class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Box Model -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic19.png" style="top:45%; left:27.5%; width:45%; z-index:-1; border-radius: 15px" />  -->


<!-- attr: { id:'boxmodel', showInPresentation:true, hasScriptWrapper:true , style:'font-size:0.9em'} -->
# <a id="boxmodel"></a> CSS3 box-sizing
- Determine whether you want an element to render it's borders and padding within its specified width, or outside of it.
- Possible values:

- Content-box

  ```css
  .container {
      width: 300px;
      box-sizing: content-box;
  }
  ```
  - box width: `288px` + `10px` padding + `1px` border on each side = `300px`

<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
<!-- # CSS3 box-sizing -->

- Border-box

  ```css
  .container {
      width: 300px;
      box-sizing: border-box;
  }
  ```
  - box width: `300px`, including padding and borders


<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
<!-- # CSS3 box-sizing (_Example_) -->
- _Example_: Box with total width of `300px` (including paddings and borders)

```css
.container {
    width: 300px;
    border: 1px solid black;
    padding: 5px;

    /* Firefox */
    -moz-box-sizing: border-box;
    /* WebKit */
    -webkit-box-sizing: border-box;
    /* Opera 9.5+, Google Chrome */
    box-sizing: border-box;
}
```



<!-- attr: { showInPresentation:true, hasScriptWrapper:true, style:'font-size: 0.95em' } -->
# IE Quirks Mode
- When using quirks mode<br /> (pages with no DOCTYPE <br /> or with a HTML 4 <br /> Transitional DOCTYPE)
  
    - Internet Explorer violates<br /> the box model standard!

<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic20.png" style="top:13.02%; left:56.14%; width:40%; z-index:-1" />  -->


<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Box Model
## [Demo](https://github.com/TelerikAcademy/CSS/blob/master/Topics/03.%20CSS-Layout/demos/08.%20box-model.html) -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic21.png" style="top:55%; left:25%; width:50%; z-index:-1" />  -->




<!-- section start -->
<!-- attr: { class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Positioning -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic22.png" style="top:50%; left:0%; width:30.29%; z-index:-1; border-radius: 15px" />  -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/troll.png" style="top:30%; left:75%; width:30.29%; z-index:-1" />  -->



<!-- attr: { id:'position', showInPresentation:true, hasScriptWrapper:true } -->
# <a id="position"></a> Positioning

- The **position** property defines the positioning of the element in the page content flow
-  The value is one of:
  - `static` is the default value
  - `relative` – relative position according to where the element would appear with static position
  - `absolute` – relative to the first parent element that has a position other than static
  - `fixed` – relative to the browser window, but ignores page scrolling


<!-- attr: { showInPresentation:true, hasScriptWrapper:true} -->
<!-- # Positioning -->
- **Margin** VS **relative positioning**
- Fixed and absolutely positioned elements do not influence the page normal flow and usually stay on top of other elements
  - Their position and size are ignored when calculating the size of parent element or position of surrounding elements
  - Overlaid according to their `z-index`
  - Inline fixed or absolutely positioned elements can apply height like block-level elements


<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Positioning -->
- `top`, `left`, `bottom`, `right`: specifies offset of absolute/fixed/relative positioned element as numerical values
- `z-index` : specifies the stack level of positioned elements
  - Understanding stacking context

<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic23.png" style="top:52.75%; left:70.80%; width:29.38%; z-index:-1" />  -->


<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Positioning
## [Demo](https://github.com/TelerikAcademy/CSS/blob/master/Topics/03.%20CSS-Layout/demos/09.%20positioning-rules.html) -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic24.png" style="top:55%; left:62%; width:28%; z-index:-1; border-radius: 15px" />  -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic25.png" style="top:55%; left:10%; width:29%; z-index:-1; border-radius: 15px" />  -->


<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
# Inline element positioning
- The **vertical-align** property sets the vertical alignment of an inline element, according to the line height
  - Values: `baseline`, `sub`, `super`, `top`, `text-top`, `middle`, `bottom`, `text-bottom` or numeric
  - Also used for content of table cells (which apply  `middle` alignment by default)


<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Alignment and Z-Index
## [Demo](https://github.com/TelerikAcademy/CSS/blob/master/Topics/03.%20CSS-Layout/demos/10.%20alignments-and-z-index-rules.html) -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic26.png" style="top:50%; left:6.26%; width:15%; z-index:-1" />  -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic27.png" style="top:50%; left:80.87%; width:20%; z-index:-1" />  -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic28.png" style="top:55%; left:34.62%; width:30%; z-index:-1; border-radius: 15px" />  -->




<!-- section start -->
<!-- attr: {  class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Floating -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic29.png" style="top:45%; left:63.57%; width:30.09%; z-index:-1; border-radius: 15px" />  -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic30.png" style="top:45%; left:13.10%; width:36.73%; z-index:-1; border-radius: 15px" />  -->


<!-- attr: { id:'float', showInPresentation:true, hasScriptWrapper:true} -->
# <a id="float"></a> Floating
- The **float** property makes the element “float” to one side
  - `left`: places the element on the left and following content on the right
  - `right`: places the element on the right and following content on the left
  - floated elements should come before the content that will wrap around them in the code
  - margins of floated elements do not collapse
  - floated inline elements can apply height


<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Float -->
- How floated elements are positioned

<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic31.png" style="top:25%; left:22.5%; width:55%; z-index:-1" />  -->


<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
# Clear
- What does **clear** do?
  - **Sets the sides of the element where other floating elements are NOT allowed**
  - Used to "drop" elements below floated ones or expand a container, which contains only floated children
  - Values: `left`, `right`, `both`

<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Clear -->
- Clearing floats
  - Clear using pseudo-class `:after`
  - Snippet after IE8
  
  ```css
  .group:after {
  content: "";
  display: table;
  clear: both;
}
```
  - Additional element (`<div>`) with a clear style
    - Deprecated - semantically unused div
  - [Additional info about floats](https://css-tricks.com/all-about-floats/)

<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true, style:'font-size: 0.9em' } -->
# Floating elements
## [Demo](https://github.com/TelerikAcademy/CSS/blob/master/Topics/03.%20CSS-Layout/demos/11.%20float-rules.html)


<!-- section start -->
<!-- attr: {  class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Flexbox
## The Next Generation of CSS Layout -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/flexbox.jpg" style="top:55%; left:33%; width:35%; z-index:-1" />  -->

<!-- attr: { id:'flex', showInPresentation:true, hasScriptWrapper:true } -->
# <a id="flex"></a>Flexbox
- **Flexbox Layout**
  - Layout mode for the arrangement of elements on a page
  - The elements behave predictably on different screen sizes and different display devices
- Browser compatibility
  - [compatibility table](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes#Browser_compatibility)
- Complete guide
  - [guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

  <!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
# Flexbox vocabulary

- Flex container
- Flex item
- Axes
- Directions
- Lines
- Dimensions

  <!-- <img class="slide-image" showInPresentation="true" src="imgs/flexbox.png" style="top:15%; left:40%; width:65%; z-index:-1" />  -->

  <!-- attr: { showInPresentation:true, hasScriptWrapper:true} -->
  # Parent properties
- **display** - enables flex for all children

```css
.container {
  display: flex; /* or inline-flex */
}
```

- **flex-direction** - establishes the main-axis

```css
.container {
  flex-direction: row | row-reverse | column | column-reverse;
}
```

<!-- attr: { showInPresentation:true, hasScriptWrapper:true} -->
<!-- # Parent properties -->

- **flex-wrap** - flex items will all try to fit onto one line by default

```css
.container {
  flex-wrap: nowrap | wrap | wrap-reverse;
}
```

- **flex-flow** - shorthand for **flex-direction** and **flex-wrap**

```css
.container {
  flex-flow: <‘flex-direction’> || <‘flex-wrap’>
}
```

<!-- attr: { showInPresentation:true, hasScriptWrapper:true} -->
<!-- # Parent properties -->
- **justify-content** - defines the alignment along the main axis

```css
.container {
  justify-content: flex-start | flex-end
                   | center | space-between | space-around;
}
```

<!-- <img class="fragment balloon" showInPresentation="true" src="imgs/justify.png" style="top:20%; left:33%; width:45%; z-index:0" />  -->

<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Parent properties -->
- **align-items** - justify-content version for the cross-axis

```css
.container {
  align-items: flex-start | flex-end
               | center | baseline | stretch;
}
```

- **align-content** - flex container's lines within when there is extra space in the cross-axis

```css
.container {
  align-content: flex-start | flex-end | center | space-between | space-around | stretch;
}
```

<div class="fragment balloon" style="top:20%; left:5%; width:45%;">
    <img  src="imgs/align-items.png"  />
</div>
<div class="fragment balloon" style="top:20%; left:55%; width:45%;">
    <img  src="imgs/align-content.png"  />
</div>

<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
# Children properties
- **order** - controls the order in which the children appear in the flex container

```css
.item {
  order: <integer>;
}
```

- **flex-grow** - defines the ability for a flex item to grow if necessary

```css
.item {
  flex-grow: <number>; /* default 0 */
}
```

<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Children properties -->
- **flex-shrink** - defines the ability for a flex item to shrink if necessary

```css
.item {
  flex-shrink: <number>; /* default 1 */
}
```

- **flex-basis** - defines the default size of an element before the remaining space is distributed

```css
.item {
  flex-basis: <length> | auto; /* default auto */
}
```

<!-- attr: { showInPresentation:true, hasScriptWrapper:true, style:'font-size: 0.9em' } -->
<!-- # Children properties -->
- **flex** - shorthand for **flex-grow**, **flex-shrink** and **flex-basis** combined (**recommended**)

```css
.item {
  flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]
}
```

- **align-self** - allows the default alignment (or the one specified by align-items) to be overridden for individual flex items

```css
.item {
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}
```

<div class="fragment balloon" style="top:45%; left:55%; width:25%;">
    <img  src="imgs/align-self.png"  />
</div>



<!-- attr: { class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->

<!-- # CSS Layout
## Questions? -->


<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
# Free Trainings @ Telerik Academy
- "Web Design with HTML 5, CSS 3 and JavaScript" course @ Telerik Academy
    - [css course](http://academy.telerik.com/student-courses/web-design-and-ui/css-styling/about)
  - Telerik Software Academy
    - [academy.telerik.com](academy.telerik.com)
  - Telerik Academy @ Facebook
    - [facebook.com/TelerikAcademy](facebook.com/TelerikAcademy)
  - Telerik Software Academy Forums
    - [forums.academy.telerik.com](http://telerikacademy.com/Forum/Home)

<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic35.png" style="top:40%; left:68.14%; width:30%; z-index:-1" />  -->
