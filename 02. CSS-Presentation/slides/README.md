<!-- section start -->
<!-- attr: { id:'', class:'slide-title', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# CSS Presentation
## How to make things shiny?
<img class="slide-image" src="\imgs\pic00.png" style="top:50.35%; left:48.81%; width:56.67%; z-index:-1" />
<div class="signature">
	<p class="signature-course"></p>
	<p class="signature-initiative"></p>
	<a href="" class="signature-link"></a>
</div>




<!-- section start -->
<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Table of Contents
- Text-related Properties
- Borders
- Backgrounds
  - Background color
  - Background image
  - Gradient Background
- Opacity
<img class="slide-image" src="\imgs\pic01.png" style="top:43.81%; left:57.52%; width:42.78%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Text-related Properties
<img class="slide-image" src="\imgs\pic02.png" style="top:30.26%; left:21.68%; width:64.94%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Text-related CSS Properties
- **color** – specifies the color of the text
- **font-size** – size of font: **xx-small**, **x-small**, **small**, **medium**, **large**, **x-large**, **xx-large**, **smaller**, **larger** or numeric value
- **font-family** – comma separated font names
  - _Example_: **verdana**, **sans-serif**, etc.
  - The browser loads the first one that is available
  - There should always be at least one generic font
- **font-weight** can be **normal**, **bold**, **bolder**, **lighter** or a number in range [100 … 900]


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # CSS Rules for Fonts -->
- **font-style** – styles the font
  - Values: **normal**, **italic**, **oblique**
- **text-decoration** – decorates the text
  - Values: **none**, **underline**, **line-trough**, **overline**, **blink**
- **text-align** – defines the alignment of text or other content
  - Values: **left**, **right**, **center**, **justify**


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Shorthand Font Property
- **font**
  - Shorthand rule for setting multiple font properties at the same time
  - 	is equal to writing this:

```css
font: italic normal bold 12px/16px verdana;
```


```css
font-style: italic;
font-variant: normal;
font-weight: bold;
font-size: 12px;
line-height: 16px;
font-family: verdana;
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Text-related Properties
## [Demo]()
<img class="slide-image" src="\imgs\pic03.png" style="top:10.09%; left:4.16%; width:29.61%; z-index:-1" />
<img class="slide-image" src="\imgs\pic04.png" style="top:8.72%; left:74.75%; width:28.21%; z-index:-1" />
<img class="slide-image" src="\imgs\pic05.png" style="top:6.17%; left:44.29%; width:22.48%; z-index:-1" />
<img class="slide-image" src="\imgs\pic06.png" style="top:53.31%; left:85.42%; width:16.26%; z-index:-1" />
<img class="slide-image" src="\imgs\pic07.png" style="top:53.81%; left:11.28%; width:15.45%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# More Fonts
<img class="slide-image" src="\imgs\pic08.png" style="top:43.78%; left:17.73%; width:25.74%; z-index:-1" />
<img class="slide-image" src="\imgs\pic09.png" style="top:47.04%; left:69.93%; width:24.79%; z-index:-1" />
<img class="slide-image" src="\imgs\pic10.png" style="top:13.51%; left:67.45%; width:34.11%; z-index:-1" />
<img class="slide-image" src="\imgs\pic11.png" style="top:13.94%; left:12.37%; width:42.31%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Font Embeds
- Use **@font-face** to declare font
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

<img class="slide-image" src="\imgs\pic12.png" style="top:15.55%; left:64.75%; width:43.75%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Text Shadow
- Applies shadow to text
- Syntax: **text-shadow: &lt;horizontal-distance&gt; &lt;vertical-distance&gt;&lt;blur-radius&gt; &lt;shadow-color&gt;;**
- Do not alter the size of a box
- text-shadow: 2px 2px 7px #000000;
<img class="slide-image" src="\imgs\pic13.png" style="top:42.09%; left:17.12%; width:68.21%; z-index:-1" />
<img class="slide-image" src="\imgs\pic14.png" style="top:66.12%; left:17.76%; width:67.00%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Text Overflow
- Specifies what should happen when text overflows the containing element
- Syntax: **text-overflow: &lt;value&gt;;**
- Possible values:
  - **ellipsis** - Display ellipses to represent clipped text
  - **clip** - Default value, clips text
- Currently not supported in Firefox and IE
<img class="slide-image" src="\imgs\pic15.png" style="top:70%; left:26.20%; width:59.06%; z-index:-1" />
<img class="slide-image" src="\imgs\pic16.png" style="top:85%; left:26.20%; width:59.06%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Word Wrapping
- Allows long words to be able to be broken and wrap onto the next line
- Syntax: **word-wrap: &lt;value&gt;;**
- Possible values:
  - **normal**
  - **break-word**
- Supported in all major browsers
<img class="slide-image" src="\imgs\pic17.png" style="top:35%; left:45.17%; width:45.60%; z-index:-1" />
<img class="slide-image" src="\imgs\pic18.png" style="top:65%; left:45.17%; width:45.60%; z-index:-1" />


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# More Fonts
## [Demo]()
<img class="slide-image" src="\imgs\pic19.png" style="top:50%; left:33%; width:35%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Borders
<img class="slide-image" src="\imgs\pic20.png" style="top:14.10%; left:6.55%; width:93.44%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Borders
- **border-width**: **thin**, **medium**, **thick** or numerical value (e.g. **10px**)
- **border-color**: color alias or RGB value
- **border-style**: **none**, **hidden**, **dotted**, **dashed**, **solid**, **double**, **groove**, **ridge**, **inset**, **outset**
- Each property can be defined separately for left, top, bottom and right
  - **border-top-style**, **border-left-color**, …


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# Border Shorthand Property
- **border**: shorthand rule for setting border properties at once:

```css
border: 1px solid red
```

- 	is equal to writing:

```css
border-width:1px;
border-color:red;
border-style:solid;
```


- Specify different borders for the sides via shorthand rules: **border-top**, **border-left**, **border-right**, **border-bottom**
  - **border:none** or **border:0**?

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Borders
## [Demo]()
<img class="slide-image" src="\imgs\pic21.png" style="top:10%; left:22%; width:55%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Border color
- Allows you to create cool colored borders
- Only Firefox supports this type of coloring

```css
border: 8px solid #000;
-moz-border-bottom-colors: #555 #666 #777 #888 #999 #aaa #bbb #ccc;
-moz-border-top-colors: #555 #666 #777 #888 #999 #aaa #bbb #ccc;
-moz-border-left-colors: #555 #666 #777 #888 #999 #aaa #bbb #ccc;
-moz-border-right-colors: #555 #666 #777 #888 #999 #aaa #bbb #ccc;
```

<img class="slide-image" src="\imgs\pic22.png" style="top:70.19%; left:13.10%; width:81.10%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Box shadow
- Allows to easily implement multiple drop shadows (outer or inner) on box elements
- Specifying values for color, size, blur and offset
- _Example_:

```css
-moz-box-shadow: 10px 10px 5px #888;
-webkit-box-shadow: 10px 10px 5px #888;
box-shadow: 10px 10px 5px #888;
```

<img class="slide-image" src="\imgs\pic23.png" style="top:65%; left:23.39%; width:61.71%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Rounded Corners
- Rounded corners are a part of CSS 3
  - Supported in all major browsers
  - Firefox, IE 9, Chrome, Opera and Safari
- Done by the **border-radius** property
- Three ways to define corner radius:

```cs
border-radius: [<length>|<%>][<length>|<%>]?
```


```cs
border-radius: 15px;
```


```cs
border-radius: 15px 20px;
```


```cs
border-radius: 15px 15px 15px 10px;
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Other Border Styles
## [Demo]()
<img class="slide-image" src="\imgs\pic24.png" style="top:0.29%; left:6.24%; width:94.03%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Background Properties
<img class="slide-image" src="\imgs\pic25.png" style="top:16.31%; left:9.36%; width:88.15%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Backgrounds
- **background-image**
  - URL of image to be used as background, e.g.:

  ```css
  background-image:url("back.gif");
  ```

- **background-color**
  - Using color and image and the same time
- **background-repeat**
  - **repeat-x**, **repeat-y**, **repeat**, **no-repeat**
- **background-attachment**
  - **fixed** / **scroll**





<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # Backgrounds -->
- **background-position**: specifies vertical and horizontal position of the background image
  - Vertical position: **top**, **center**, **bottom**
  - Horizontal position: **left**, **center**, **right**
  - Both can be specified in percentage or other numerical values
  - _Examples_:

```cs
background-position: top left;
```


```cs
  background-position: -5px 50%;
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size:40px;' } -->
# Background Shorthand Property
- **background**: shorthand rule for setting background properties at the same time:

```cs
background: #FFF0C0 url("back.gif") no-repeat fixed top;
```

- 	is equal to writing:

```cs
background-color: #FFF0C0;
background-image: url("back.gif");
background-repeat: no-repeat;
background-attachment: fixed;
background-position: top;
```

- Some browsers will not apply BOTH color and image for background if using shorthand rule


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Background-image or &lt;img&gt;?
- Background images allow you to save many image tags from the HTML
  - Leads to less code
  - More content-oriented approach
- All images that are not part of the page content (and are used only for "beautification") should be moved to the CSS


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Background Styles
## [Demo]()
<img class="slide-image" src="\imgs\pic26.png" style="top:40%; left:60%; width:30%; z-index:-1" />
<img class="slide-image" src="\imgs\pic27.png" style="top:40%; left:12%; width:30%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Gradient Backgrounds
- Gradients are smooth transitions between two or more specified colors
- Use of CSS gradients can replace images and reduce download time
  - Lots of gradient generators on the WEB
- Create a more flexible layout, and look better while zooming
- Supported in all major browsers via different keywords
- This is still an experimental feature
<img class="slide-image" src="\imgs\pic28.png" style="top:63.04%; left:82.10%; width:18.95%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Gradient Backgrounds _Example_

```cs
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
```

<img class="slide-image" src="\imgs\pic29.png" style="top:63.91%; left:30%; width:30%; z-index:-1" />


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Gradient Background
## [Demo]()
<img class="slide-image" src="\imgs\pic30.png" style="top:40%; left:2%; width:40.92%; z-index:-1" />
<img class="slide-image" src="\imgs\pic31.png" style="top:40%; left:59.18%; width:40.99%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Multiple Backgrounds
- CSS3 allows multiple background images
- Simple comma-separated list of images
- Supported in Firefox (3.6+), Chrome (1.0/1.3+), Opera (10.5+) and Internet Explorer (9.0+)
- Comma separated list for the other properties

```cs
background-image: url(sheep.png), url(grass.png);
```

<img class="slide-image" src="\imgs\pic32.png" style="top:65%; left:4%; width:14.10%; z-index:-1" />
<img class="slide-image" src="\imgs\pic33.png" style="top:65%; left:30%; width:26.78%; z-index:-1" />
<img class="slide-image" src="\imgs\pic34.png" style="top:65%; left:71%; width:26.78%; z-index:-1" />


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Multiple Backgrounds
## [Demo]()
<img class="slide-image" src="\imgs\pic35.png" style="top:50%; left:32%; width:35%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Opacity
<img class="slide-image" src="\imgs\pic36.png" style="top:40%; left:22%; width:54.43%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Opacity
- **opacity**: specifies the opacity of the element
  - Floating point number from 0 to 1
  - For old Mozilla browsers use **–moz-opacity**
  - For IE use **filter:alpha(opacity=value)** where value is from 0 to 100; also, "binary and script behaviors" must be enabled and **hasLayout** must be triggered, e.g. with **zoom:1**


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Opacity
## [Demo]()
<img class="slide-image" src="\imgs\pic37.png" style="top:50%; left:26%; width:48.93%; z-index:-1" />


<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# CSS Presentation
## Questions?


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Free Trainings @ Telerik Academy
- "Web Design with HTML 5, CSS 3 and JavaScript" course @ Telerik Academy
    - html5course.telerik.com
  - Telerik Software Academy
    - academy.telerik.com
  - Telerik Academy @ Facebook
    - facebook.com/TelerikAcademy
  - Telerik Software Academy Forums
    - forums.academy.telerik.com
<img class="slide-image" src="\imgs\pic38.png" style="top:58.18%; left:90.52%; width:16.97%; z-index:-1" />
<img class="slide-image" src="\imgs\pic39.png" style="top:34.35%; left:68.14%; width:36.30%; z-index:-1" />
<img class="slide-image" src="\imgs\pic40.png" style="top:48.92%; left:75.91%; width:10.85%; z-index:-1" />
<img class="slide-image" src="\imgs\pic41.png" style="top:11.88%; left:91.56%; width:14.23%; z-index:-1" />
