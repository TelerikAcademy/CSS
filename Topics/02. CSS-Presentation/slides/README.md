<!-- section start -->
<!-- attr: {  class:'slide-title', showInPresentation:true, hasScriptWrapper:true } -->
# CSS Presentation
## How to make things shiny?
<div class="signature">
	<p class="signature-course">CSS Styling</p>
	<p class="signature-initiative">Telerik Software Academy</p>
	<a href="https://telerikacademy.com" class="signature-link">https://telerikacademy.com</a>
</div>

<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic00.png" style="top:53%; left:52%; width:50%; z-index:-1" /> -->

<!-- section start -->
<!-- attr: { showInPresentation:true, hasScriptWrapper:true } -->
# Table of Contents
- [Text-related Properties](#textprops)
- [Borders](#border)
- [Backgrounds](#backgrounds)
  - [Background image](#bckgimage)
  - [Gradient Background](#bckggradient)
- [Opacity](#opacityslide)

<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic01.png" style="top:43.81%; left:57.52%; width:42.78%; z-index:-1" /> -->


<!-- section start -->
<!-- attr: {  class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Text-related Properties -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic02.png" style="top:45%; left:29%; width:40%; z-index:-1; border: 2px solid white; border-radius: 10px;" /> -->


<!-- attr: {  id:'textprops', showInPresentation:true, hasScriptWrapper:true, style: "font-size: 0.8em" } -->
# <a id="textprops"></a>Text-related CSS Properties
- `color` – specifies the color of the text
- `font-size` – size of font: `xx-small`, `x-small`, `small`, `medium`, `large`, `x-large`, `xx-large`, `smaller`, `larger` or numeric value
- `font-family` – comma separated font names
  - _Example_: `verdana`, `sans-serif`, etc.
  - The browser loads the first one that is available
  - There should always be at least one generic font
- `font-weight` can be `normal`, `bold`, `bolder`, `lighter` or a number in range [100 … 900]


<!-- attr: {   showInPresentation:true, hasScriptWrapper:true } -->
<!-- # CSS Rules for Fonts -->
- `font-style` – styles the font
  - Values: `normal`, `italic`, `oblique`
- `text-decoration` – decorates the text
  - Values: `none`, `underline`, `line-trough`, `overline`, `blink`
- `text-align` – defines the alignment of text or other content
  - Values: `left`, `right`, `center`, `justify`


<!-- attr: {   showInPresentation:true, hasScriptWrapper:true, style:'font-size: 0.9em' } -->
# Shorthand Font Property
- `font`

  - Shorthand rule for setting multiple font properties at the same time

```css
#selector { font: italic normal bold 12px/16px verdana; }
```

  - is equal to writing this:

```css
.selector {
	font-style: italic;
	font-variant: normal;
	font-weight: bold;
	font-size: 12px;
	line-height: 16px;
	font-family: verdana;
}
```

<!-- attr: {  class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Text-related Properties
## [Demo](./../demos/1. text-related-preperties.html) -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic06.png" style="top:55%; left:42%; width:16.26%; z-index:-1" /> -->




<!-- section start -->
<!-- attr: {  class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # More Fonts -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic10.png" style="top:45%; left:33%; width:34.11%; z-index:-1; border: 2px solid white; border-radius: 10px;" /> -->


<!-- attr: {   showInPresentation:true, hasScriptWrapper:true } -->
# Font Embeds
- Use `@font-face` to declare font
- Point to font file on server
- Call font with font-family
- Currently not supported in IE
- Use font embedding instead of images

```css
@font-face {
	font-family: SketchRockwell;
	src: url('SketchRockwell-Bold.ttf');
}
.my_CSS3_class {
	font-family: SketchRockwell;
	font-size: 3.2em;
}
```

<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic12.png" style="top:20%; left:64.75%; width:35%; z-index:-1" /> -->


<!-- attr: {   showInPresentation:true, hasScriptWrapper:true } -->
# Text Shadow
- Applies shadow to text
- Syntax: <code>text-shadow: &lt;horizontal-distance&gt; &lt;vertical-distance&gt; &lt;blur-radius&gt; &lt;shadow-color&gt;;</code>
- Do not alter the size of a box
<br/>
<br/>

```
.selector {
	text-shadow: 2px 2px 7px #000000;
}
```
<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic13.png" style="top:53%; left:17.12%; width:45%; z-index:-1" /> -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic14.png" style="top:80%; left:17.76%; width:45%; z-index:-1" /> -->


<!-- attr: {   showInPresentation:true, hasScriptWrapper:true } -->
# Text Overflow
- Specifies what should happen when text overflows the containing element
- Syntax: <code>text-overflow: &lt;value&gt;;</code>
- Possible values:
  - `ellipsis` - Display ellipses to represent clipped text
<br/>

  - `clip` - Default value, clips text
<br/>
<br/>
- Currently not supported in Firefox and IE

<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic15.png" style="top:57%; left:26.20%; width:40%; z-index:-1" /> -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic16.png" style="top:75%; left:26.20%; width:40%; z-index:-1" /> -->


<!-- attr: {   showInPresentation:true, hasScriptWrapper:true } -->
# Word Wrapping
- Allows long words to be able to be broken and wrap onto the next line
- Syntax: <code>word-wrap: &lt;value&gt;;</code>
- Possible values:
  - `normal`
  <br/>
  <br/>
  <br/>
  - `break-word`
  <br/>
  <br/>
- Supported in all major browsers

<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic17.png" style="top:45%; left:30%; width:35%; z-index:-1" /> -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic18.png" style="top:65%; left:35%; width:35%; z-index:-1" /> -->


<!-- attr: {  class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # More Fonts
## [Demo](./../demos/2. Fonts.html) -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic19.png" style="top:55%; left:33%; width:35%; z-index:-1" /> -->




<!-- section start -->
<!-- attr: {  class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Borders -->

<!-- attr: {  id:'border', showInPresentation:true, hasScriptWrapper:true } -->
# <a id="border"></a> Borders
- `border-width`: `thin`, `medium`, `thick` or numerical value (e.g. `10px`)
- `border-color`: color alias or RGB value
- `border-style`: `none`, `hidden`, `dotted`, `dashed`, `solid`, `double`, `groove`, `ridge`, `inset`, `outset`
- Each property can be defined separately for left, top, bottom and right
  - `border-top-style`, `border-left-color`, …


<!-- attr: {   showInPresentation:true, hasScriptWrapper:true, style:'font-size: 0.75em;' } -->
# Border Shorthand Property
- `border`: shorthand rule for setting border properties at once:

```css
#selector { border: 1px solid red }
```

- 	is equal to writing:

```css
#complex .selector {
	border-width:1px;
	border-color:red;
	border-style:solid;
}
```


- Specify different borders for the sides via shorthand rules: `border-top`, `border-left`, `border-right`, `border-bottom`
  - `border:none` or `border:0`?

<!-- attr: {  class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Borders
## [Demo](./../demos/3. borders.html) -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic21.png" style="top:10%; left:22%; width:55%; z-index:-1" /> -->


<!-- attr: {   showInPresentation:true, hasScriptWrapper:true } -->
# Border color
- Allows you to create cool colored borders
- Only Firefox supports this type of coloring

```css
.selector-for-gradient {
	border: 8px solid #000;
	-moz-border-bottom-colors: #555 #666 #777 #888 #999 #aaa #bbb #ccc;
	-moz-border-top-colors: #555 #666 #777 #888 #999 #aaa #bbb #ccc;
	-moz-border-left-colors: #555 #666 #777 #888 #999 #aaa #bbb #ccc;
	-moz-border-right-colors: #555 #666 #777 #888 #999 #aaa #bbb #ccc;
}
```

<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic22.png" style="top:70.19%; left:13.10%; width:81.10%; z-index:-1" /> -->


<!-- attr: {   showInPresentation:true, hasScriptWrapper:true } -->
# Box shadow
- Allows to easily implement multiple drop shadows (outer or inner) on box elements
- Specifying values for color, size, blur and offset
- _Example_:

```css
.box-shadow {
	-moz-box-shadow: 10px 10px 5px #888;
	-webkit-box-shadow: 10px 10px 5px #888;
	box-shadow: 10px 10px 5px #888;
}
```

<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic23.png" style="top:75%; left:23.39%; width:50%; z-index:-1" /> -->


<!-- attr: {   showInPresentation:true, hasScriptWrapper:true, style:'font-size: 0.8em' } -->
# Rounded Corners
- Rounded corners are a part of CSS 3
  - Supported in all major browsers
  - Firefox, IE 9, Chrome, Opera and Safari
- Done by the `border-radius` property

```css
.selector { border-radius: [<length>|<%>][<length>|<%>]? }
```

- Four ways to define corner radius:

```css
.selector { border-radius: 15px; }
```


```css
.selector { border-radius: 15px 20px; }
```


```css
.selector { border-radius: 15px 15px 15px 10px; }
```

```css
.selector { border-top-left-radius: 15px }
```

<!-- attr: {  class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Other Border Styles
## [Demo](./../demos/4. borders-other-styles.html) -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic24.png" style="top:0.29%; left:6.24%; width:94.03%; z-index:-1" /> -->




<!-- section start -->
<!-- attr: {  class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Background Properties -->


<!-- attr: {  id:'backgrounds', showInPresentation:true, hasScriptWrapper:true, style:'font-size:0.9em' } -->
# <a id="backgrounds"></a>Backgrounds
- `background-image`
  - URL of image to be used as background, e.g.:

  ```css
  background-image:url("back.gif");
  ```

- `background-color`
  - Using color and image and the same time
- `background-repeat`
  - `repeat-x`, `repeat-y`, `repeat`, `no-repeat`
- `background-attachment`
  - `fixed` / `scroll`

<!-- attr: {   showInPresentation:true, hasScriptWrapper:true, style:'font-size:0.9em' } -->
<!-- # Backgrounds -->
- `background-position`: specifies vertical and horizontal position of the background image
  - Vertical position: `top`, `center`, `bottom`
  - Horizontal position: `left`, `center`, `right`
  - Both can be specified in percentage or other numerical values
  - _Examples_:

```css
.first-selector {
	background-position: top left;
}

.second-selector {
  background-position: -5px 50%;
}
```

<!-- attr: {   showInPresentation:true, hasScriptWrapper:true, style:'font-size:40px;' } -->
# Background Shorthand Property
- `background`: shorthand rule for setting background properties at the same time:

```css
background: #FFF0C0 url("back.gif") no-repeat fixed top;
```

- 	is equal to writing:

```css
#selector {
	background-color: #FFF0C0;
	background-image: url("back.gif");
	background-repeat: no-repeat;
	background-attachment: fixed;
	background-position: top;
}
```

- Some browsers will not apply BOTH color and image for background if using shorthand rule


<!-- attr: {  id:'bckgimage', showInPresentation:true, hasScriptWrapper:true } -->
# <a id="bckgimage"></a>Background-image or &lt;img&gt;?
- Background images allow you to save many image tags from the HTML
  - Leads to less code
  - More content-oriented approach
- All images that are not part of the page content (and are used only for "beautification") should be moved to the CSS


<!-- attr: {  class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Background Styles
## [Demo](./../demos/5. backgrounds.html) -->


<!-- attr: {  id:'bckggradient', showInPresentation:true, hasScriptWrapper:true } -->
# <a id="bckggradient"></a>Gradient Backgrounds
- Gradients are smooth transitions between two or more specified colors
- Use of CSS gradients can replace images and reduce download time
  - Lots of gradient generators on the WEB
- Create a more flexible layout, and look better while zooming
- Supported in all major browsers via different keywords
- This is still an experimental feature

<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic28.png" style="top:75%; left:82.10%; width:18.95%; z-index:-1" /> -->


<!-- attr: {   showInPresentation:true, hasScriptWrapper:true } -->
# Gradient Backgrounds _Example_

-	_Example_: linear vertical gradient:

```css
.linear-gradient {
	/* Firefox 3.6+ */
	background: -moz-linear-gradient(100% 100% 90deg,   
	  #FFFF00, #0000FF);
	/* Safari 4-5, Chrome 1-9 */
	background: -webkit-gradient(linear, 0% 0%, 0%
	  100%, from(#0000FF), to(#FFFF00));
	/* Safari 5.1+, Chrome 10+ */
	background: -webkit-linear-gradient(#FFFF00,
	  #0000FF);
	/* Opera 11.10+ */
	background: -o-linear-gradient(#2F2727, #0000FF);
}
```

<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic29.png" style="top:77%; left:10%; width:70%; height: 20%; z-index:-1" /> -->


<!-- attr: {  class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Gradient Background
## [Demo](./../demos/6. gradient-backgrounds.html) -->


<!-- attr: {   showInPresentation:true, hasScriptWrapper:true } -->
# Multiple Backgrounds
- **CSS3** allows multiple background images
- Simple comma-separated list of images
- Supported in **Firefox (3.6+), Chrome (1.0/1.3+), Opera (10.5+) and Internet Explorer (9.0+)**
- Comma separated list for the other properties

```css
background-image: url(sheep.png), url(grass.png);
```

<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic32.png" style="top:65%; left:4%; width:14.10%; z-index:-1" /> -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic33.png" style="top:65%; left:30%; width:26.78%; z-index:-1" /> -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic34.png" style="top:65%; left:71%; width:26.78%; z-index:-1" /> -->


<!-- attr: {  class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Multiple Backgrounds
## [Demo](./../demos/7. multiple-backgrounds.html) -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic35.png" style="top:55%; left:32%; width:35%; z-index:-1; border-radius: 15px;" /> -->




<!-- section start -->
<!-- attr: {  class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Opacity -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic36.png" style="top:45%; left:29%; width:40%; z-index:-1; border-radius: 15px;" /> -->


<!-- attr: {  id:'opacityslide', showInPresentation:true, hasScriptWrapper:true } -->
# <a id="opacityslide"></a>Opacity
- `opacity`: specifies the opacity of the element
  - Floating point number from 0 to 1
  - For old Mozilla browsers use `–moz-opacity`
  - For IE use `filter:alpha(opacity=value)` where value is from 0 to 100; also, "binary and script behaviors" must be enabled and `hasLayout` must be triggered, e.g. with `zoom:1`


<!-- attr: {  class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Opacity
## [Demo](./../demos/8. opacity.html) -->

<!-- section start -->

<!-- attr: {  class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
# CSS Presentation
## Questions?


<!-- attr: { showInPresentation: true, hasScriptWrapper: true, style:'font-size: 1em' } -->
# Free Trainings @ Telerik Academy
- "Web Design with HTML 5, CSS 3 and JavaScript" course @ Telerik Academy
    - [html5course.telerik.com](html5course.telerik.com)
  - Telerik Software Academy
    - [academy.telerik.com](academy.telerik.com)
  - Telerik Academy @ Facebook
    - [facebook.com/TelerikAcademy](facebook.com/TelerikAcademy)
  - Telerik Software Academy Forums
    - forums.academy.telerik.com

<!-- <img class="slide-image" showInPresentation="true" src="imgs\pic39.png" style="top:38%; left:68.14%; width:30%; z-index:-1" /> -->
