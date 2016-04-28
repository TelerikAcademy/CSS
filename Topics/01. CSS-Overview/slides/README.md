<!-- section start -->
<!-- attr: { id:'', class:'slide-title', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# CSS Overview
## Cascading Style Sheets
<img class="slide-image" src="\imgs\pic00.png" style="top:27.37%; left:6.83%; width:18.21%; z-index:-1" />
<img class="slide-image" src="\imgs\pic01.png" style="top:6.49%; left:79.34%; width:15.49%; z-index:-1" />
<img class="slide-image" src="\imgs\pic02.png" style="top:6.69%; left:33.18%; width:20.23%; z-index:-1" />
<img class="slide-image" src="\imgs\pic03.png" style="top:54.66%; left:59.94%; width:42.31%; z-index:-1" />
<div class="signature">
	<p class="signature-course"></p>
	<p class="signature-initiative"></p>
	<a href="" class="signature-link"></a>
</div>




<!-- section start -->
<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Table of Contents
- What is CSS?
- Styling with Cascading Style Sheets (CSS)
- CSS Selectors
  - Select by element name, id or class
  - Nested Selectors
- Importing CSS into HTML
- Selectors
  - Attribute selectors
  - Pseudo Selectors
<img class="slide-image" src="\imgs\pic04.png" style="top:31.20%; left:86.81%; width:22.86%; z-index:-1" />
<img class="slide-image" src="\imgs\pic05.png" style="top:2.06%; left:31.72%; width:26.19%; z-index:-1" />
<img class="slide-image" src="\imgs\pic06.png" style="top:53.77%; left:73.57%; width:30.30%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Cascading Style Sheets
## Separating Content from Presentation
<img class="slide-image" src="\imgs\pic07.png" style="top:12.34%; left:3.99%; width:96.97%; z-index:-1" />
<img class="slide-image" src="\imgs\pic08.png" style="top:46.80%; left:3.99%; width:28.21%; z-index:-1" />
<img class="slide-image" src="\imgs\pic09.png" style="top:49.04%; left:76.72%; width:28.44%; z-index:-1" />
<img class="slide-image" src="\imgs\pic10.png" style="top:49.08%; left:34.88%; width:36.24%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# CSS: A New Philosophy
- Separate content from presentation!
- Title
- Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Suspendisse at pede ut purus malesuada dictum. Donec vitae neque non magna aliquam dictum.
-  Vestibulum et odio et ipsum
-  accumsan accumsan. Morbi at
-  arcu vel elit ultricies porta. Proin
-  tortor purus, luctus non, aliquam nec, interdum vel, mi. Sed nec quam nec odio lacinia molestie. Praesent augue tortor, convallis eget, euismod nonummy, lacinia ut, risus.


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;  ' } -->
# The Resulting Page
- Title
- Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Suspendisse at pede ut purus malesuada dictum. Donec vitae neque non magna aliquam dictum.
  -  Vestibulum et odio et ipsum
  -  accumsan accumsan. Morbi at
  -  arcu vel elit ultricies porta. Proin
- Tortor purus, luctus non, aliquam nec, interdum vel, mi. Sed nec quam nec odio lacinia molestie. Praesent augue tortor, convallis eget, euismod nonummy, lacinia ut, risus.




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# CSS Intro
## Styling with Cascading Stylesheets
<img class="slide-image" src="\imgs\pic11.png" style="top:50%; left:60.73%; width:37.64%; z-index:-1" />
<img class="slide-image" src="\imgs\pic12.png" style="top:50%; left:13.72%; width:33.79%; z-index:-1" />
<img class="slide-image" src="\imgs\pic13.png" style="top:50%; left:44.71%; width:19.14%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# CSS Introduction
- Cascading Style Sheets (CSS)
  - Used to **describe** the presentation of documents
  - Define **sizes**, **spacing**, **fonts**, **colors**, **layout**, etc.
  - Improve content **accessibility**
  - Improve **flexibility**
- Designed to separate presentation from content
- Due to CSS, all **HTML presentation** tags and **attributes** are **deprecated**, e.g. **font**, **center**, etc.


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # CSS Introduction -->
- CSS can be applied to any XML document
  - Not just to HTML / XHTML
- CSS can specify different styles for different **media**
  - On-screen
  - In print
  - Handheld, projection, etc.
  - … even by voice or Braille-based reader


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Why “Cascading”?
- Priority scheme determining which style rules apply to element
  - **Cascade priorities** or **specificity (weight)** are calculated and assigned to the rules
  - Child elements in the HTML DOM tree inherit styles from their parent
    - Can override them
    - Control via **!important** rule


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- # Why "Cascading"? -->
<img class="slide-image" src="\imgs\pic14.png" style="top:13.22%; left:23.54%; width:57.61%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Style Inheritance
- Some CSS styles are inherited and some are not
  - **Text-related** and **list-related** properties are **inherited**: **color**, **font-size**, **font-family**, **line-height**, **text-align**, **list-style**, etc.
  - **Box-related** and **positioning** styles are **not inherited**: **width**, **height**, **border**, **margin**, **padding**, **position**, **float**, etc
  - **<a>** elements do not inherit color and text-decoration


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Style Sheets Syntax
- Stylesheets consist of **rules**, **selectors**, **declarations**, **properties** and **values**
- **Selectors** are separated by commas
- **Declarations** are separated by semicolons
- **Properties** and **values** are separated by colons

```cs
h1,h2,h3 { color: green; font-weight: bold; }
```

<img class="slide-image" src="\imgs\pic15.png" style="top:68%; left:29.24%; width:50.69%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Common Selectors
## Select the Elements to Apply a Style
<img class="slide-image" src="\imgs\pic16.png" style="top:50%; left:24.15%; width:61.00%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Selectors
- Selectors determine which element the rules apply to:
  - All elements of specific type (**tag**)
  - Those that match a specific attribute (**id**, **class**)
  - Elements may be matched depending on how they are nested in the document tree (HTML)
- _Examples_:

```cs
.header a { color: green }
```


```cs
#menu>li { padding-top: 8px }
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 32px;' } -->
# Primary Selectors
- Three primary kinds of selectors:
  - By tag (type selector):
  - By element id:
  - By element class name (only for HTML):

```cs
h1 { font-family: verdana,sans-serif; }
```


```cs
#element_id { color: #ff0000; }
```


```cs
.myClass {border: 1px solid red}
```
- Selectors can be combined with commas:

```cs
h1, .link, #top-link {font-weight: bold}
```

- 	This will match **&lt;h1&gt;** **tags**, elements with **class** **link**, and the element with **id** **top-link**


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size:40px' } -->
# Nested Selectors
- Match relative to element placement:

```cs
p a {text-decoration: underline}
```

- This will match all **&lt;a&gt;** tags that are inside of **&lt;p&gt;**
- ***** – universal selector (avoid or use with care!):

```cs
p * {color: black}
```

- This will match all descendants of **&lt;p&gt;** element
- **+** selector – used to match “next sibling”:

```cs
img + .link {float:right}
```

- 	This will match all siblings with class name **link** that appear immediately after **&lt;img&gt;** tag

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px' } -->
<!-- # Nested Selectors -->
- **&gt;** selector – matches direct child nodes:

```cs
p > .error {font-size: 8px}
```
- 	This will match all elements with class **error**, direct children of **&lt;p&gt;** tag

- **.class1.class2** (no space!)

```cs
p.post-text.special {font-weight: bold}
```

  - Matches elements with both (all) classes applied at the same time

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Common Selectors
## [Demo]()
<img class="slide-image" src="\imgs\pic17.png" style="top:50%; left:33.51%; width:41.60%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Importing CSS Into HTML
## How to Use CSS with HTML?
<img class="slide-image" src="\imgs\pic19.png" style="top:40%; left:6.67%; width:28.98%; z-index:-1" />
<img class="slide-image" src="\imgs\pic20.png" style="top:49.92%; left:44.91%; width:52.89%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Importing CSS Into HTML
- **CSS** (presentation) can be imported in **HTML** (content) in three ways:
  - **Inline**: the CSS rules in the **style** attribute
    - No selectors are needed
  - **Embedded**: in the **&lt;head&gt;** in a **&lt;style&gt;** tag
  - **External**: CSS rules in separate file (best)
    - Usually a file with **.css** extension
    - Linked via **&lt;link** **rel="stylesheet"** **href="…"&gt;** tag
    - Via**@import** directive in embedded CSS block


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- # Linking HTML and CSS -->
- Using **external CSS files** is highly recommended
  - Simplifies the HTML document
  - Improves page load speed (CSS file is cached)
<img class="slide-image" src="\imgs\pic21.png" style="top:44.96%; left:17.78%; width:20.58%; z-index:-1" />
<img class="slide-image" src="\imgs\pic22.png" style="top:44.96%; left:70.78%; width:20.58%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Inline Styles: _Example_

```cs
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Inline Styles</title>
</head>
<body>
  <p>Here is some text</p>
<!--Separate multiple styles with a semicolon-->
  <p style="font-size: 20pt">Here is some
    more text</p>
  <p style="font-size: 20pt;color:
    #0000FF" >Even more text</p>
</body>
</html>
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Inline Styles: _Example_

```cs
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Inline Styles</title>
</head>
<body>
  <p>Here is some text</p>
<!--Separate multiple styles with a semicolon-->
  <p style="font-size: 20pt">Here is some
    more text</p>
  <p style="font-size: 20pt;color:
    #0000FF" >Even more text</p>
</body>
</html>
```

<img class="slide-image" src="\imgs\pic23.png" style="top:34.38%; left:75%; width:34.82%; z-index:0" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Embedded Styles
- Embedded in the HTML in the **&lt;style&gt;** tag:
  - The **&lt;style&gt;** tag is placed in the **&lt;head&gt;** section of the document
  - **type** attribute specifies the MIME type
    - MIME describes the format of the content
    - Other MIME types include **text/html**, **image/gif**, **text/javascript** …
    - Not required in HTML5
- Used for document-specific styles

```cs
<style type="text/css">
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Embedded Styles: _Example_

```cs
<!DOCTYPE html>
<html>
<head>
  <title>Style Sheets</title>
  <style type="text/css">
    em {background-color:#8000FF; color:white}
    h1 {font-family:Arial, sans-serif}
    p  {font-size:18pt}
    .blue {color:blue}
  </style>
<head>
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # Embedded Styles: _Example_ -->

```cs
…
<body>
  <header>
      <h1 class="blue">A Heading</h1>  </header>  <article>
      <p>Here is some text. Here is some text.     
      Here is some text. Here is some text. Here
      is some text.</p>      
     <h1>Another Heading</h1>        
     <p class="blue">Here is some more text.
     Here is some more text.</p>
     <p class="blue">Here is some <em>more</em>
     text. Here is some more text.</p>  </article>
</body>
</html>
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- # Embedded Styles: _Example_ -->

```cs
…
<body>
  <header>
      <h1 class="blue">A Heading</h1>  </header>  <article>
      <p>Here is some text. Here is some text.     
      Here is some text. Here is some text. Here
      is some text.</p>      
     <h1>Another Heading</h1>        
     <p class="blue">Here is some more text.
     Here is some more text.</p>
     <p class="blue">Here is some <em>more</em>
     text. Here is some more text.</p>  </article>
</body>
</html>
```

<img class="slide-image" src="\imgs\pic24.png" style="top:40%; left:80%; width:30%; z-index:0" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# External CSS Styles
- External linking
  - Separate pages can all use a shared style sheet
  - Only modify a single file to change the styles across your entire Web site (see www.csszengarden.com)
- **link** tag (with a **rel** attribute)
  - Specifies a relationship between current document and another document
  - **link** elements should be in the **<head>**

```cs
<link rel="stylesheet" type="text/css"
  href="styles.css">
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # External CSS Styles -->
- **@import**
  - Another way to link external CSS files
  - _Example_:
  - Ancient browsers do not recognize **@import**
  - Use **@import** in an external CSS file to workaround the IE CSS file limit of 31 files
  - 	

```cs
<style type="text/css">
  @import url("styles.css");  /* same as */
  @import "styles.css";
</style>
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# External Styles: _Example_

```cs
/* CSS Document */

a 	  { text-decoration: none }

a:hover { text-decoration: underline;
          color: red;
          background-color: #CCFFCC }

li em   { color: red;
          font-weight: bold }

ul	  { margin-left: 2cm }

ul ul	  { text-decoration: underline;
          margin-left: .5cm }
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # External Styles: _Example_ -->

```cs
<!DOCTYPE html>
<html>
<head>
  <title>Importing style sheets</title>
  <link type="text/css" rel="stylesheet"
    href="styles.css"  />
</head>
<body>
  <h1>Shopping list for <em>Monday</em>:</h1>
  <li>Milk</li>
  …
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # External Styles: _Example_ -->

```cs
  …
  <li>Bread
    <ul>
      <li>White bread</li>
      <li>Rye bread</li>
      <li>Whole wheat bread</li>
    </ul>
  </li>
  <li>Rice</li>
  <li>Potatoes</li>
  <li>Pizza <em>with mushrooms</em></li>
</ul>
<a href="http://food.com" title="grocery
  store">Go to the Grocery store</a>
</body>
</html>
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- # External Styles: _Example_ -->

```cs
  …
  <li>Bread
    <ul>
      <li>White bread</li>
      <li>Rye bread</li>
      <li>Whole wheat bread</li>
    </ul>
  </li>
  <li>Rice</li>
  <li>Potatoes</li>
  <li>Pizza <em>with mushrooms</em></li>
</ul>
<a href="http://food.com" title="grocery
  store">Go to the Grocery store</a>
</body>
</html>
```

<img class="slide-image" src="\imgs\pic25.png" style="top:16.75%; left:70%; width:35%; z-index:0" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Attribute Selectors
## Picking Elements with Certain Attributes
<img class="slide-image" src="\imgs\pic26.png" style="top:50%; left:33.68%; width:30%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# Attribute Selectors
- **[ ]** selects elements based on attributes
  - Element with a given attributeSelects **&lt;a&gt;** elements with **title**
  - Elements with a concrete attribute value
  - Selects **&lt;input&gt;** elements with **type=text**
  - Elements whose attribute values contain a word
  - Selects **&lt;a&gt;** elements whose title attribute value contains **logo**

```cs
a[title] {color:black}
```


```cs
input[type=text] { font-family:Consolas}
```


```cs
a[title*=logo] {border: none}
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Attribute Selectors
## [Demo]()
<img class="slide-image" src="\imgs\pic27.png" style="top:50%; left:36%; width:30%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Pseudo Selectors
## Relative to Element Content or State
<img class="slide-image" src="\imgs\pic29.png" style="top:50%; left:28.07%; width:54.45%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Common Pseudo Selectors
- Pseudo-classes define state
  - **:hover**, **:visited**, **:active** , **:lang**
- Pseudo-elements define element "parts" or are used to generate content
  - **:first-line** , **:before**, **:after**

```cs
a:hover { color: red; }
p:first-line { text-transform: uppercase; }
.title:before { content: "»"; }
.title:after { content: "«"; }
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Common Pseudo Selectors
## [Demo]()
<img class="slide-image" src="\imgs\pic30.png" style="top:40%; left:23.39%; width:60.83%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Structural Pseudo-classes
- **:root**
  - The root of the document
- **E:nth-child(n)**
  - An **E** element, the n-th child of its parent
- **E:nth-last-child(n)**
  - An **E** element, the n-th child of its parent, counting from the last on
- **E:nth-of-type(n)**
  - An **E** element, the n-th sibling of its type


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # Structural Pseudo-classes -->
- **E:nth-last-of-type(n)**
  - An **E** element, the n-th sibling of its type, counting from the last one
- **E:last-child**
  - An **E** element, last child of its parent
- **E:first-of-type**
  - An **E** element, first sibling of its type
- **E:last-of-type**
  - An **E** element, last sibling of its type


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # Structural Pseudo-classes -->
- **E:only-child**
  - An **E** element, only child of its parent
- **E:only-of-type**
  - An **E** element, only sibling of its type
- **E:empty**
  - An **E** element that has no children (including text nodes)
- More detailed descriptions:
- http://www.w3.org/TR/css3-selectors/#structural-pseudos


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Structural Selectors
## [Demo]()
<img class="slide-image" src="\imgs\pic31.png" style="top:40%; left:31.11%; width:47.16%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# The UI Element StatesPseudo-Classes
- **E:enabled**
  - A user interface element **E** which is enabled
- **E:disabled**
  - A user interface element **E** which is disabled
- **E:checked**
  - A user interface element **E** which is checked (for instance a radio-button or checkbox)
  - Currently supported only in Opera and IE10 !


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# UI Selectors
## [Demo]()
<img class="slide-image" src="\imgs\pic32.png" style="top:50%; left:38%; width:26.34%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Other CSS 3 Selectors
- **E:target**
  - An **E** element being the target of the referring URI
- **E:not(s)**
  - An **E** element that does not match simple selector
- **E~ F**
  - An **F** element preceded by an **E** element


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Other CSS 3 Selectors
## [Demo]()
<img class="slide-image" src="\imgs\pic33.png" style="top:50%; left:35%; width:30%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# CSS Values
## Types, Ranges, Units
<img class="slide-image" src="\imgs\pic34.png" style="top:50%; left:8.70%; width:25.12%; z-index:-1" />
<img class="slide-image" src="\imgs\pic35.png" style="top:50%; left:82.23%; width:22.39%; z-index:-1" />
<img class="slide-image" src="\imgs\pic36.png" style="top:50%; left:42.60%; width:30.30%; z-index:-1" />



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# CSS Values
- All values in CSS are strings
  - They can represent values that are not strings
  - I.e. **14px** means size 14 pixels
- Colors are set in a red-green-blue format (RGB)
  - Both in hex and decimal

```cs
li.nav-item {
  color: #44f1e1}
```


```cs
li.nav-item {
  color: rgb(68, 241, 255)}
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Size Values
- When setting a size (width, height, font-size…) the values are given as numbers
  - Multiple formats / metrics may be used
  - Pixels, ems, e.g. **12px** , **1.4em**
  - Points, inches, centimeters, millimeters
    - E.g. **10pt** , **1in**, **1cm**, **1mm**
  - Percentages, e.g. **50%**
    - Of the size of the container/font size
  - Zero can be used with no unit: **border: 0;**


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Size Values
## [Demo]()
<img class="slide-image" src="\imgs\pic39.png" style="top:54.16%; left:52.40%; width:31.85%; z-index:-1" />
<img class="slide-image" src="\imgs\pic40.png" style="top:37.02%; left:25.67%; width:36.36%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Color Values
- Colors in CSS can be represented in few ways
  - Using red-green-blue
    - Or red-green-blue-alpha
  - Using hue-saturation-light
    - Or hue-saturation-light-alpha

```cs
color: #f1a2ff
color: rgb(241, 162, 255)
color: rgba(241, 162, 255, 0.1)
```

<div class="fragment balloon" style="top:60%; left:62.59%; width:37.74%">The opacity values are from 0.0 to 1.0</div>

```cs
color: hsl(291, 85%, 89%);
color: hsl(291, 85%, 89%, 0.1);
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# RGB Colors
- RGB colors are defined with values for red, green and blue intensity
- Syntax:
  - **#44fa36** – values are in hex
  - **rgb(&lt;red&gt;, &lt;green&gt;, &lt;blue&gt;)** – decimal values
- The range for **red**, **green** and **blue** is between integers **0** and **255**

```cs
color: #07f2b3
  <!– or -->
color: rgb (7, 242, 179)
```

<img class="slide-image" src="\imgs\pic41.png" style="top:20.28%; left:85.03%; width:15.98%; z-index:-1" />
<img class="slide-image" src="\imgs\pic42.png" style="top:62.77%; left:88.91%; width:15.85%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# RGBA Colors
- Standard RGB colors with an opacity value for the color (alpha channel)
- Syntax: **rgba(&lt;red&gt;, &lt;green&gt;, &lt;blue&gt;, &lt;alpha&gt;)**
- The range for **red**, **green** and **blue** is between integers **0** and **255**
- The range for the alpha channel is between **0.0** and **1.0**
- _Example_: **rgba(255, 0, 0, 0.5)**
<img class="slide-image" src="\imgs\pic43.png" style="top:20.28%; left:85.03%; width:15.98%; z-index:-1" />
<img class="slide-image" src="\imgs\pic44.png" style="top:62.92%; left:88.91%; width:15.85%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# HSL Colors
- Hue is a degree on the color wheel
  - **0** (or **360**) is red, **120** is green, **240** is blue
- Saturation is a percentage value
  - **100%** is the full color
- Lightness is also a percentage
  - **0%** is dark (black)
  - **100%** is light (white)
  - **50%** is the average
<img class="slide-image" src="\imgs\pic45.png" style="top:49.81%; left:72.98%; width:30.85%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# HSLA Colors
- HSLA allows a fourth value, which sets the Opacity (via the Alpha channel) of the element
- As RGBA is to RGB, HSLA is to HSL
- Supported in IE9+, Firefox 3+, Chrome, Safari, and in Opera 10+
- _Example_:
  - **hsla(0,** **100%,** **50%,** **0.5)**
  - Result:
<img class="slide-image" src="\imgs\pic46.png" style="top:42.31%; left:69.24%; width:35.26%; z-index:-1" />
<img class="slide-image" src="\imgs\pic47.png" style="top:61.14%; left:28.07%; width:25.56%; z-index:-1" />


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Color Values
## [Demo]()
<img class="slide-image" src="\imgs\pic48.png" style="top:50%; left:33%; width:34.38%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Default Browser Styles
## Why Things Look Different on Different Browsers?
<img class="slide-image" src="\imgs\pic49.png" style="top:60%; left:33%; width:35%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Default Browser Styles
- Browsers have predefined CSS styles
  - Used when there is no CSS information or any other style information in the document
- **Caution**: default styles differ in browsers
  - E.g. **margins**, **paddings**and **font sizes** differ most often
  - Usually developers reset them

```cs
* { margin: 0; padding: 0; }
```


```cs
body, h1, p, ul, li { margin: 0; padding: 0; }
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # CSS Cascade (Preceden -->
- There are browser, user and author stylesheets with "**normal**" and "**important**" declarations
  - Browser styles (least priority)
  - Normal user styles
  - Normal author styles (external, in head, inline)
  - Important author styles
  - Important user styles (max priority)

```cs
a { color: red !important ; }
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# CSS Specificity
- CSS specificity is used to determine the precedence (priority) of the CSS style declarations with the same origin
  - Simple calculation: <br />**#id = 100**, **.class = 10**, **:pseudo = 10**, **[attr] = 10**, **tag = 1**, *** = 0**
  - Same number of points? Order matters!
  - See also:
    - http://www.smashingmagazine.com/2007/07/27/css-specificity-things-you-should-know/
    - http://css.maxdesign.com.au/selectutorial/advanced_conflict.htm


<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# CSS Rules Precedence
## [Demo]()
<img class="slide-image" src="\imgs\pic50.png" style="top:6%; left:8.97%; width:88.88%; z-index:-1" />
<img class="slide-image" src="\imgs\pic51.png" style="top:50.69%; left:7.49%; width:22.04%; z-index:-1" />
<img class="slide-image" src="\imgs\pic52.png" style="top:47.40%; left:80.27%; width:24.24%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# CSS References
- The CSS documentation at WebPlatform.org:
  - http://docs.webplatform.org/wiki/css
- CSS documentation at Mozilla
  - https://developer.mozilla.org/en-US/docs/CSS
- CSS3 tutorial
  - http://www.w3schools.com/css3/
- A list of all CSS 2.1 properties is available at http://www.w3.org/TR/CSS2/propidx.html


<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# CSS Overview
## Questions?


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Free Trainings @ Telerik Academy
- "Web Design with HTML 5, CSS 3 and JavaScript" course @ Telerik Academy
    - [html5course.telerik.com](html5course.telerik.com)
  - Telerik Software Academy
    - [academy.telerik.com](academy.telerik.com)
  - Telerik Academy @ Facebook
    - [facebook.com/TelerikAcademy](facebook.com/TelerikAcademy)
  - Telerik Software Academy Forums
    - forums.academy.telerik.com
<img class="slide-image" src="\imgs\pic53.png" style="top:58.18%; left:90.52%; width:16.97%; z-index:-1" />
<img class="slide-image" src="\imgs\pic54.png" style="top:34.35%; left:68.14%; width:36.30%; z-index:-1" />
<img class="slide-image" src="\imgs\pic55.png" style="top:48.92%; left:75.91%; width:10.85%; z-index:-1" />
<img class="slide-image" src="\imgs\pic56.png" style="top:11.88%; left:91.56%; width:14.23%; z-index:-1" />
