<!-- section start -->
<!-- attr: { id:'', class:'slide-title', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# LESS
## The Dynamic Stylesheet Language
<img class="slide-image" src="\imgs\pic00.png" style="top:56.82%; left:56.18%; width:46.29%; z-index:-1" />
<div class="signature">
	<p class="signature-course"></p>
	<p class="signature-initiative"></p>
	<a href="" class="signature-link"></a>
</div>




<!-- section start -->
<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Table of Contents
- LESS Overview
- Working with LESS
- Using LESS
  - On the Client
  - On the Server
- LESS Features
  - Selector nesting
  - Mixins and Functions
  - Variables and Interpolation
  - Many More
<img class="slide-image" src="\imgs\pic03.png" style="top:29.78%; left:64.70%; width:38.94%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# LESS Overview
## What is LESS?

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# LESS Overview
- Extension to CSS - http://lesscss.org/
  - Write "less" code – compile to normal CSS
  - Can be parsed both Client and Server side
    - Using a LESS parser written in JavaScript
- LESS Features include
  - Variables
  - Mixins
  - Color editing functions
  - Selector nesting and more
<img class="slide-image" src="\imgs\pic05.png" style="top:47.31%; left:73.44%; width:30.03%; z-index:-1" />




<!-- section start -->
<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# Using LESS on the Client
- LESS can be parsed on the client (browser)
  - Include a JavaScript file, that does the parsing

```html
<link rel="stylesheet/less" type="text/css" href="styles.less"/ >
< script src="less.js">< /script> //after the less link
```

- Steps:
  - Write your LESS
  -  Using Visual Studio, you should add a mime type for the LESS in web.config

```xml
<configuration> <system.webServer> <staticContent>
  <mimeMap fileExtension=".less" mimeType="text/css" />   
</staticContent> </system.webServer> </configuration>
```

  - You are ready to go

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # Using LESS on the Client -->
- How client-side LESS works?
  - The JavaScript performs a AJAX GET request to LESS file
  - Then it parses all the LESS code into pure CSS
  - The CSS is appended to the HEAD of the page
- Using client-side LESS is **slow**
  - All the parsing is done by the client
  - i.e. spend some of the browser resources for kinda pointless parsing
  - Imagine a 2000-lines-long LESS file…




<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Parsing LESS on the Server
- LESS can be parsed on the server in many ways
  - Using the client approach and copy the parsed CSS
    - Not good enough, lots of copy-pastying
  - Using node.js to do the parsing
    - Better solution - the parsing is automated
  - Using VS plugin - Web Essentials
    - Live parses the LESS to pure CSS


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# How To Use Node.js
- Install Node from https://nodejs.org/
- Open Command Prompt and write

```cs
npm install less -g
```

- Navigate to the folder with the .less file
- Write down the following

```cs
$ lessc {less file} {output CSS file}
```

- You can also minify the result

```cs
$ lessc –x {less file} {output CSS file}
```

<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# LESS Features
## Selector Nesting, Mixins, Variables, etc…


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size:36px;' } -->
# Selector Nesting
- LESS introduces selector nesting

```less
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

- Parses to

```less
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


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # Selector Nesting -->
- All selectors inside a selector are translated to nested selectors
- Selectors can also reference themselves inside their selector using the symbol **&** (**AND**)

```css
…
 a{
   &:hover{…}
 }
…
```

```css
…
 a{…}
 a:hover{…}
…
```

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Selector Nesting
## [Demo]()
<img class="slide-image" src="\imgs\pic07.png" style="top:52%; left:33.68%; width:32%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# LESS Variables
- LESS also has variables
  - Using the @ (at) symbol
  - Can be used to store colors, size, etc…
- Usable to set default background-color, font-color, font-size, etc…

```css
@link-color: #ffffff;
@v-link-color: #646363;
a {
  color: @link-color;
  &:visited {
    color: @v-link-color;
}
```


```css
body a {
  color: white; }
  body a:visited {
    color: #646363; }
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Variables
## [Demo]()
<img class="slide-image" src="\imgs\pic08.png" style="top:52%; left:30%; width:40%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Interpolation
- LESS variables can be inserted as CSS properties
  - Using **@{…}**

```css
@border-side:top;
@border-color:blue;
@border-style:ridge;
@border-width:15px;
…
border-@{border-side} :
  $border-width $border-style $border-color;
```

```css
border-top : 15px ridge blue
```

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Interpolation
## [Demo]()
<img class="slide-image" src="\imgs\pic09.png" style="top:52%; left:34%; width:31.63%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# Extend
- The **:extend** pseudo selector can be used to extend a selector
- More here: http://lesscss.org/features/#extend-feature

```css
nav ul {
  &:extend(.inline);
  background: blue;
}
.inline {
  color: red;
}
```

```css
nav ul {
  background: blue;
}
.inline,
nav ul {
  color: red;
}
```

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Extend
## [Demo]()
<img class="slide-image" src="\imgs\pic10.png" style="top:52%; left:30%; width:40%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Functions
- LESS support predefined functions
  - For stuff with colors
  - For sizes (percentages)
  - Find all the functions at http://lesscss.org/functions/

```css
@color: #ffffff;
background-color:lighten(@color, 10%);
color:darken(@color, 15%);
percentage(0.5); //returns 50%
```

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Functions
## [Demo]()

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Mixins
- Mixins are kind of developer defined functions
  - The developer can make them for clear LESS
- Two kind of mixins
  - Parameterless
    - Get a default styles every time
  - With parameters
    - Get style based on some parameters
    - Gradient, borders, etc…


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # Mixins -->
- How to define mixins?
  - Use **.mixin-name**
  - Then the styles are normal LESS
  - How to use the mixin?
    - Place use **.mixin-name**

```css
.clearfix{
  zoom:1;
  &:after{
    display:block; content:"";
    height:0; clear:both; } }
```


```css
ul#main-nav{
  .clearfix;
}
```

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Basic Mixins
## [Demo]()
<img class="slide-image" src="\imgs\pic12.png" style="top:52%; left:26%; width:49.70%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Mixins with Arguments
- Mixins can also be defined with parameters
  - i.e. for gradient-background
- Use the arguments like a C# method

```css
.opacity(@value){
  …
}

//arguments can take default values
.box(@border:none,@bg:rgba(0,0,0,0.7),@size:200px) {
  …
}
…
  div.box-div{
    .box;  //using the mixin with default parameter values
    .opacity(0.5);  //using the mixin with 0.5 value
  }
…
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Mixins with Arguments
## [Demo]()
<img class="slide-image" src="\imgs\pic13.png" style="top:52%; left:35%; width:30%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Pattern-matching Mixins
- Mixins can define different behavior, depending on its parameters

```css
.color(dark,@color){
  color:@darken(@color);
}
.color(light,@color){
  color:@lighten(@color);
}
//called no matter which of the above is called
@color(@_,@color){
  border: 1px solid @color;
}
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Pattern-matching Mixins
## [Demo]()

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Mixin "Return" Values
- Mixins can have **"return"** values because of the variable scope

```css
.average(@x, @y) {
  @average: ((@x + @y) / 2);
}

div {
  .average(16px, 50px); // "call" the mixin
  padding: @average;    // use its "return" value
}

/* Compiles to */
div {
  padding: 33px;
}
```

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Mixin "Return" Values
## [Demo]()


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Importing Other Files
- You can import other files wherever you want
  - In our main file
  - In our "other-styles.less" file
  - Results in

```css
.foo { background: #900; }
@import "other-styles.less";
```


```css
<!-- other-styles.less -->
.foobar { background: #900; }
```


```cs
.foo { background: #900; }
.foobar { background: #900; }
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Importing Other Files
## [Demo]()
<img class="slide-image" src="\imgs\pic16.png" style="top:42.40%; left:55.52%; width:28.21%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Conditional Mixins
- Also called "Mixin Guards"
  - Using **"when"** keyword can specify conditions on which the mixin will be called
  - Operators are **>**, **>=**,**=**, **=<**, **<**

```css
.mixin (@a) when (lightness(@a) >= 50%) {
  background-color: black;
}
.mixin (@a) when (lightness(@a) < 50%) {
  background-color: white;
}
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Conditional Mixins
## [Demo]()

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Loops
- Because of **"Mixin Guards"** you can create loop/iterations structure

```css
.loop(@counter) when (@counter > 0) {
  .loop((@counter - 1));    // next iteration
  width: (10px * @counter); // code for each iteration
}

div {
  .loop(5); // launch the loop
}
```

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Loops
## [Demo]()
<img class="slide-image" src="\imgs\pic18.png" style="top:52%; left:32%; width:35%; z-index:-1" />


<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# LESS
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
<img class="slide-image" src="\imgs\pic19.png" style="top:58.18%; left:90.52%; width:16.97%; z-index:-1" />
<img class="slide-image" src="\imgs\pic20.png" style="top:34.35%; left:68.14%; width:36.30%; z-index:-1" />
<img class="slide-image" src="\imgs\pic21.png" style="top:48.92%; left:75.91%; width:10.85%; z-index:-1" />
<img class="slide-image" src="\imgs\pic22.png" style="top:11.88%; left:91.56%; width:14.23%; z-index:-1" />
