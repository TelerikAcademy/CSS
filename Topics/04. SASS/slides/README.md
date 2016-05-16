<!-- section start -->
<!-- attr: { class:'slide-title', showInPresentation:true, hasScriptWrapper:true } -->
# SASS
## Syntactically Awesome Stylesheets

<div class="signature">
	<p class="signature-course">CSS Styling</p>
	<p class="signature-initiative">Telerik Software Academy</p>
	<a href="telerikacademy" class="signature-link">telerikacademy.com</a>
</div>

<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic00.png" style="top:23.12%; left:0%; width:22.15%; z-index:-1; border-radius: 15px" /> -->
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic01.png" style="top:49.51%; left:49.43%; width:53.92%; z-index:-1; border-radius: 15px" /> -->


<!-- section start -->
# Table of Contents
- [SASS Overview](#)
- [Working with SASS](#)
  - [Using Ruby Console](#)
  - [Using Visual Studio Plugins](#)
- [SASS Features](#)
  - [Nesting](#)
  - [Variables](#)
  - [Mixins](#)
  - [Selector Inheritance](#)
  - [Operators](#)




<!-- section start -->
<!-- attr: { class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
# SASS Overview
## What is SASS?

<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic02.png" style="top:55%; left:30%; width:40%; z-index:-1; border-radius: 15px" /> -->

<!-- attr: { showInPresentation:true } -->
# SASS Overview
- **Syntactically Awesome Stylesheets** is an extension of CSS
  - Makes coding CSS much easier and organized
  - **Translates to pure CSS** on the server
    - i.e. no slowdown on the client
- SASS introduces many techniques to power the CSS coding
  - Variables, Functions, Mixins, Inheritance, Operators, etc




<!-- section start -->
<!-- attr: { class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
# Working with SASS
## Ok... but How?

<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic03.png" style="top:55%; left:35%; width:30%; z-index:-1; border-radius: 15px" /> -->

<!-- attr: { showInPresentation:true } -->
# Coding SASS Using Ruby
- Using Ruby and Ruby console
  - Install Ruby - [Installer](http://rubyinstaller.org/downloads/)
  - Use ruby gem installer to install SASS
  ```cmd
  gem install sass
  ```
  - Set Ruby to listen for changes on the SASS file
  ```cmd
  sass --watch sassfile.scss:outputfile.css
  ```
  - This will autocompile SASS to CSS on any changes
  - Open the SASS file with **any** text editor
  - You get the translated CSS

<!-- attr: { class:'slide-section demo', showInPresentation:true } -->
<!-- # Coding SASS Using Ruby 
## [Demo]() -->


<!-- attr: { showInPresentation:true } -->
# Coding SASS in Visual Studio
- VS has many plugins to support SASS
  - Web Workbench
  - Web Essentials (soon)
- How to install plugins?
  - Find the plugin [here](http://visualstudiogallery.msdn.microsoft.com)
  - Open VS -> Tools -> Extensions and Updates -> find the plugin
- Create SCSS file and do your SASS


<!-- attr: { class:'slide-section demo', showInPresentation:true } -->
<!-- # SASS in Visual Studio
## [Demo]() -->




<!-- section start -->
<!-- attr: { class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
# SASS Features
## Selector Nesting, Mixins, Variables, Operators etc…

<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic08.png" style="top:65%; left:25%; width:50%; z-index:-1; border-radius: 15px" /> -->

<!-- attr: { showInPresentation:true } -->
# Selector Nesting

- SASS features selector nesting

```sass
body {
    font: normal 16px arial;
    color: #fff;
    background-color: #011b63;
    h1 {
        font-size: 2.3em;
        font-weight: bold;
    }
}
```

<!-- attr: { showInPresentation:true } -->
# Selector Nesting

- The resulting CSS

```css
body {
  font: normal 16px arial;
  color: #fff;
  background-color: #011b63;
}
body h1 {
  font-size: 2.3em;
  font-weight: bold;
}
```

<!-- attr: { showInPresentation:true } -->
# Selector Nesting
- All selectors inside a selector are translated to nested selectors

```sass
/* SASS */
body {
  font-size: 25px;
  h1 {
    font-style: italic;
  }
}
```

```css
/* CSS */
body {
  font-size: 25px;
}
body h1{
  font-style: italic;
}
```

<!-- attr: { showInPresentation:true } -->
# Selector Nesting

- Selectors can also reference themselves inside their selector using the symbol `&`
- The following SASS code:

```sass
a {
    color: black;
    &:hover {
        color: lightblue;
    }
}
```
- translates to the following css code:

```css
 a {
   color: black;
 }
 a:hover {
   color: lightblue;
 }
```

<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Selector Nesting
## [Demo]() -->

<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic09.png" style="top:55%; left:35%; width:30%; z-index:-1" /> -->

<!-- attr: { showInPresentation:true, style:'font-size: 0.8em' } -->
# SASS Variables
- SASS also has variables
  - Using the $ (dolar) symbol
  - Can be used to store colors, size, etc…
- Usable to set default background-color, font-color, font-size, etc…

```sass
$link-color: #ffffff;
$v-link-color: #646363;
a {
  color: $link-color;
  &:visited {
    color: $v-link-color;
}
```


```css
body a {
  color: white; }
  body a:visited {
    color: #646363; }
```


<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Variables
## [Demo]() -->

<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic10.png" style="top:55%; left:35%; width:30%; z-index:-1; border-radius: 15px" /> -->


# Interpolation
- SASS variables can be inserted as CSS properties
  - Like C# 6 string interpolation
  - Using `#{}`

```sass
$border-side:top;
$border-color:blue;
$border-style:ridge;
$border-width:15px;

border-#{$border-side} :
  $border-width $border-style $border-color;
```


```css
border-top : 15px ridge blue
```

<!-- attr: { showInPresentation:true, style:'font-size: 0.8em' } -->
# Mixins
- Mixins are kind of developer defined functions
  - The developer can make them for clear SASS
- Two kind of mixins
  - Parameterless
    - Get a default styles every time
  - With parameters
    - Get style based on some parameters
    - Gradient, borders, etc…

<!-- attr: { showInPresentation:true, style:'font-size: 0.8em' } -->
# Defining Mixins
- How to define mixins?
  - Use **@****mixin** **mixin****-name**
  - Then the styles are normal SASS
  - How to use the mixin?
    - Place use **@include****mixin****-name**

```cs
@mixin clearfix{
  zoom:1;
  &:after{
    display:block; content:"";
    height:0; clear:both; } }
```


```cs
ul#main-nav{
  @include clearfix;
}
```


<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Basic Mixins
## [Demo]() -->

<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic11.png" style="top:55%; left:30%; width:40%; z-index:-1;border-radius:15px" /> -->

<!-- attr: { showInPresentation:true, style:'font-size: 0.9em' } -->
# Mixins with Arguments
- Mixins can also be defined with parameters
  - i.e. for gradient-background
- Put the arguments like a C# or JavaScript method

```sass
@mixin opacity($value){
  opacity: $value;
  filter: alpha(opacity = ($value*100));
  zoom: 1;
}
//arguments can take default values
@mixin box($border: none,$bg: rgba(0,0,0,0.7),$size: 200px) {
  width: $size; height: $size;
  border: $border;
  background: $bg;
  padding: 15px;
}
```


<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Mixins with Arguments
## [Demo]() -->

<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic12.png" style="top:55%; left:30%; width:40%; z-index:-1; border-radius: 15px" /> -->

<!-- attr: { showInPresentation:true, style:'font-size: 0.7em' } -->
# Selector Inheritance
- SASS enables the inheritance of selector
  - i.e. in a selector, get the properties of another selector
  - Use **@extend**

```sass
.clearfix {
  zoom: 1;
  &:after {
    display: block; height: 0;
    content: ""; clear: both;
  }
}
div{
  @extend .clearfix;}
```


```css
.clearfix, body div {
  zoom: 1; 
}
.clearfix:after, body div:after {
  display: block;
  height: 0;
  content: "";
  clear: both; 
}
```


<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Selector Inheritance
## [Demo]() -->




<!-- section start -->
<!-- attr: { class:'slide-section', showInPresentation:true, hasScriptWrapper:true } -->
# Importing SASS
<!-- <img class="slide-image" showInPresentation="true" src="imgs/pic14.png" style="top:45%; left:32.5%; width:35%; z-index:-1; border-radius: 15px" /> -->


# Importing SASS Files
- SASS files can be imported in other SASS files
  - Like CSS files can be imported in CSS files
  - Use the `@import` directive
- SASS defines partials
  - i.e. SASS files that are meant to be imported
  - Just use prefix `_` (underscope)

```cs
@import 'gradients.scss'
//can use the items from gradients.scss
```


<!-- attr: { class:'slide-section demo', showInPresentation:true, hasScriptWrapper:true } -->
<!-- # Importing SASS
## [Demo]() -->

<!-- attr: { class:'slide-section', showInPresentation:true } -->
<!-- # SASS
## Questions? -->

<!-- attr: { showInPresentation:true, hasScriptWrapper:true, style:'font-size: 0.95em' } -->
# Free Trainings @ Telerik Academy
- "Web Design with HTML 5, CSS 3 and JavaScript" course @ Telerik Academy
    - [css course](http://academy.telerik.com/student-courses/web-design-and-ui/css-styling/about)
  - Telerik Software Academy
    - [academy.telerik.com](academy.telerik.com)
  - Telerik Academy @ Facebook
    - [facebook.com/TelerikAcademy](facebook.com/TelerikAcademy)
  - Telerik Software Academy Forums
    - forums.academy.telerik.com