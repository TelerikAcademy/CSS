<!-- section start -->
<!-- attr: { id:'', class:'slide-title', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Stylus Overview
## Expressive, dynamic, robust CSS

<!-- section start -->
<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Table of Contents
- [Preprocessors Overview](#overview)
  - [Preprocessors for CSS (Stylus, Sass/SCSS, LESS)](#css-preprocessors)
- [Stylus basics](#basics)
  - [Stylus syntax](#syntax)
  - [Selectors and selector nesting](#selectors)
- [Setup and usage](#setup-and-usage)
  - [Installing Node.js](#installing-node)
  - [Installing Stylus package](#installing-stylus)
  - [Using Stylus in Editors](#using-stylus)


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Table of Contents
- [Stylus features:](#features)
  - [Variables](#variables)
  - [Interpolation](#interpolation)
  - [Property lookups](#lookups)
  - [Functions](#functions)
    - [Using built-in functions](#functions)
    - [Creating functions](#creating-functions)
  - [Creating and using mixins](#mixins)
  - [Selector Inheritance](#selector-inheritance)
  - [Stylus Scripting](#scripting)
  - [Libraries and linking other files](#libraries-and-linking)




<!-- section start -->
<!-- attr: { id:'overview', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# <a id="overview"></a>Preprocessors Overview
## What is a Preprocessor?
<img class="slide-image" src="\imgs\pic00.png" style="top:52%; left:25%; width:50%; z-index:-1" />


<!-- attr: { id:'css-preprocessors', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# <a id="css-preprocessors"></a>Preprocessors Overview
- A preprocessor is a program that processes its input data to produce output that is used as input to another program
  - Sass, Less, Stylus are preprocessors for CSS
  - CoffeeScript, TypeScript are preprocessors for JavaScript
  - Jade, Ejs are preprocessors for HTML




<!-- section start -->
<!-- attr: { id:'basics', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- # <a id="basics"></a>Stylus Basics
## What is Stylus? -->

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# What is Stylus?
- Stylus is a preprocessor for CSS
  - All Stylus code is compiled to pure CSS
  - Extends CSS, without breaking it
    - Adds a lot of syntactic sugar
    - Adds a "dynamic" functionality
    - Removes "not-necessary" code


<!-- attr: { id:'syntax', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 38px;' } -->
# <a id="syntax"></a>Stylus Syntax
- The Stylus syntax is clean and easy
  - Removes all not-necessary symbols
    - Semicolons, curly brackets, etc…
  - Significant whitespace is what matters
    - Indentation marks the scope

```css
/* CSS */
#root{
  display: block;
  width: 960px;
  margin: 0 auto;
  border: 1px solid black;
}
```

```styl
/* stylus */
#root
  display block
  width 960px
  margin 0 auto
  border 1px solid black
```

<!-- attr: { id:'selectors', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# <a id="selectors"></a>Selectors in Stylus
- Stylus selectors are absolutely the same as in regular CSS
  - Every CSS code is valid Stylus code!
  - **.class**, **#id**, **tagName**

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# Selectors in Stylus
- Yet, Stylus supports nesting of selectors:

```stylus
<!-- Stylus -->
.hlist
  list-style-type none
  .list-item
    float left
    border-right 1px solid #ccc
    &:last-of-type
      border-right none
```

```css
<!-- CSS -->
.hlist {
  list-style-type: none;
}
.hlist .list-item {
  float: left;
  border-right: 1px solid #ccc;
}
.hlist .list-item:last-of-type {
  border-right: none;
}
```

<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # Stylus: Setup and Usage
## Setting up Node.js, Stylus and coding environment -->

<!-- attr: { id:'setup-and-usage', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# <a id="setup-and-usage"></a>Stylus: Setup and Usage
- To use Stylus:
  - Install **Node.js**
  - Install **Stylus package** for **Node.js**
  - Install a **plugin** for your editor


<!-- attr: { id:'installing-node', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# <a id="installing-node"></a>Installing Node.js
- Visit the Node.js website: https://nodejs.org/
- Install it
- Make sure **Node.js is added to PATH**
- Node.js is installed on the machine and can be used through the CMD/Terminal


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- # Adding Node.js to Path on Windows -->
- Go to "Computer" -> "Properties"
<img class="slide-image" src="\imgs\pic01.png" style="top:28%; left:12.38%; width:75%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- # Adding Node.js to Path on Windows -->
- Go to "Advanced system settings"
<img class="slide-image" src="\imgs\pic02.png" style="top:28%; left:14.44%; width:75%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- # Adding Node.js to Path on Windows -->
- Go to "Advanced"  -> "Environment             Variables"
<img class="slide-image" src="\imgs\pic03.png" style="top:28%; left:14%; width:75%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- # Adding Node.js to Path on Windows -->
- Go to "System                  Variables"  -> "Path"  -> "Edit"
<img class="slide-image" src="\imgs\pic04.png" style="top:28%; left:14%; width:75%; z-index:-1" />


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- # Adding Node.js to Path on Windows -->
- Add to the end:
<img class="slide-image" src="\imgs\pic05.png" style="top:28%; left:14%; width:75%; z-index:-1" />




<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Adding Node.js to Path on Linux and OS X
- Open `~/.bashrc` with `admin sudo`
- Find the **Node.js** path
  - Usually it is `/usr/bin/node`
- Add the **Node.js** path to `~/.bashrc`
- You have **Node.js** in the **PATH**


<!-- attr: { id:'installing-stylus', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# <a id="installing-stylus"></a>Installing Stylus
- Install **Node.js**
  - Make sure **Node.js** is in **PATH**
- Open CMD/Terminal
- Run the following line:
  - `npm install -g stylus`
  - this will install **Stylus** globally on the machine


<!-- attr: { id:'using-stylus', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# <a id="using-stylus"></a>Using Stylus
- Stylus code must be compiled to CSS
- There are a few ways to achieve that:
  - Using the Node.js Terminal/CMD
    - [Stylus command line docs](http://stylus-lang.com/docs/executable.html)
  - Or use plugins for your favorite editor:
    - Sublime  Text 2/3
    - Atom.io
    - Visual Studio
    - Visual Studio Code
    - Brackets
    - WebStorm


<!-- section start -->
<!-- attr: { id:'features', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- # <a id="features"></a>Stylus Features
## Variables, Functions, Mixins, Variables, etc… -->

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Stylus Features
- Stylus supports:
  - Variables
  - Interpolation
  - Property look-up
  - Functions and mixins
  - Selector inheritance
  - Conditionals and Iteration
  - Many more


<!-- attr: { id:'variables', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# <a id="variables"></a>Stylus Features: Variables
- Variables in Stylus are defined easy:
  - As a regular property/value pair, but using **"="** (equals sign) instead of **":"** (colons)
  - Can be used to store **colors**, **size**, etc…
- Usable to set default background-color, font-color, font-size, etc…

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# Stylus Features: Variables
```cs
<!-- Stylus -->
link-color= #ffffff;
v-link-color= #646363;
a
  color link-color
  &:visited
    color @v-link-color
```


```css
<!-- CSS -->
a {
  color: #fff;
}
a:visited {
  color: #646363;
}
```



<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Stylus Features: Variables
## [Demo]()

<!-- attr: { id:'interpolation', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# <a id="interpolation"></a>Stylus Features: Interpolation
- Interpolation means inserting variable value as a property/selector name
  - Interpolation is performed using **{…}**
- Stylus

```styl
side = 'top'
number = 5
.box-{number}
    border-{side} 1px solid black
```
- CSS

```css
.box-5 {
  border-top: 1px solid #000;
}
```

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Stylus Features: Interpolation
## [Demo]()

<!-- attr: { id:'lookups', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# <a id="lookups"></a>Stylus Features: Property Look-up
- Stylus supports property look-up
  - i.e. check the values of a property
- Stylus

```styl
.box
    width 100px
    height (@width/2)
    border-radius max(@width, @height)
```
- CSS

```css
.box {
  width: 100px;
  height: 50px;
  border-radius: 100px;
}
```

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Stylus Features: Property Look-up
## [Demo]()

<!-- attr: { id:'functions', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# <a id="functions"></a>Stylus Features: Built-in Functions
- Stylus has a set of predefined functions for:
  - Working with colors:

```styl
color= /* some color */
dark(color) /* returns "true", if "color" is dark */
light(color) /* returns "true" if "color" is light */
```


```cs
color: darken(#123456, 10%) /* returns #102f4d */
color: lighten(#123456, 15%) /* returns #1d5288 */
```

- Find all built-in functions in Stylus at https://learnboost.github.io/stylus/docs/bifs.html

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Stylus Features: Built-in Functions
- Working with lists:

```styl
props = (padding 5px) (display block)
push(props, (float left))
```

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Stylus Features: Built-In Functions
## [Demo]()

<!-- attr: { id:'creating-functions', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# <a id="creating-functions"></a>Stylus Features: Functions
- Stylus supports definition of developer functions:

```styl
sum(items)
    sum = 0px
    for val in items
        sum = sum + val
    sum /* return sum */
```

- Used as a regular function

```css
font-size: sum(14px 28px 45px)
height: sum(@width  + 150px)
```

<!-- attr: { id:'mixins', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# <a id="mixins"></a>Stylus Features: Mixins
- Both mixins and functions are defined in the same manner
  - Yet they are applied in different ways
    - Functions return a value, mixins generate CSS


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# Stylus Features: Mixins
- Stylus

```styl
vendor(prop, args)
    -webkit-{prop} args
    -moz-{prop} args
    {prop} args
.button
  vendor('opacity', 0.5)
  vendor('border-radius', 15px)
```
- CSS

```styl
.button {
  -webkit-opacity: 0.5;
  -moz-opacity: 0.5;
  opacity: 0.5;
  -webkit-border-radius: 15px;
  -moz-border-radius: 15px;
  border-radius: 15px;
}
```



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # Mixins -->
- How to define mixins?
  - Use **mixin-name**
  - Then the styles are normal Stylus
  - How to use the mixin?
    - Place use **mixin-name ormixin-name()**

```styl
clearfix
  zoom 1
  &:after
    /* code for clearfix */
```


```styl
ul#main-nav{
  clearfix()
}
```

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Stylus Features: Mixins
## [Demo]()

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Stylus Features: Mixins with Arguments
- Mixins can also be defined with parameters
  - i.e. for gradient-background
- Use the arguments like a C#/JS/C++ methods

```styl
box(border= none, bg= rgba(0, 0, 0, 0.7), size= 200px)
    width size
    height size
    border border
    background bg
    border-radius 15px

.rect
  display inline-block
  box '1px solid black' rgba(123, 0, 0, 0.6) 100px
```

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# @extend or Mixins?
- Why both `mixins` and `@extend`?
  - `Mixins` have parameters and generate different code, based on the parameters
  - `@extend` provides a way to minify the number of classes on an element
    - Instead of adding `.clearfix` to all elements that clear, add it to the selector that the elements already have

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Stylus Features: Mixins with Arguments
## [Demo]()

<!-- attr: { id:'selector-inheritance', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# <a id="selector-inheritance"></a>Selector Inheritance
- Selectors in Stylus can be inherited using @extend
  - Meaning add a selector to a previously defined selectors list:

- Stylus

```cs
.clearfix
  zoom 1
  &:after
    /* code for clearfix */
.list-item
  float left
  padding 5px 15px
  &:last-of-type
    border-right: none
    @extend .clearfix
```
- _Contuinue..._

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# Selector Inheritance
- CSS

```cs
.clearfix,
.list-item:last-of-type {
  zoom: 1;
}
.clearfix:after,
.list-item:last-of-type:after {
  /* code for clearfix */
}
.list-item { /* … */ }
.list-item:last-of-type { /* … */ }
```

<!-- attr: { id:'', class:'slide-section demo', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Stylus Features: Selector Inheritance
## [Demo]()


<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # Stylus: Scripting, Libraries and Importing -->

<!-- attr: { id:'scripting', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# <a id="scripting"></a>Stylus Scripting
- Stylus supports elementary scripting
  - Something like JavaScript, but not quite
  - Conditionals:

```styl
body
  if theme is 'dark'
    background #333
    color #ccc    
  else if theme is 'light'
    background #ccc
    color #333
  else
    error('unknown theme!')

```

_Continue..._

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Stylus Scripting

- Conditionals:

```cs
for i in (1...15)
    .item-{i}
        if i%2
            c= yellowgreen
            bc= #ccc
        else
            c= lightblue
            bc= #333
        color c
        background-color bc
```

<!-- attr: { id:'libraries-and-linking', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px;' } -->
# <a id="libraries-and-linking"></a>Creating Libraries and Importing Stylus files
- Like CSS, **Stylus** has a **@import** directive
  - The CSS loads another CSS file
  - In CSS, **@import** loads a CSS file with an additional HTTP request
  - In Stylus, **@import** just loads the code from the file inside our file

```cs
.clearfix
  /* … */
linear-gradient(stops)
  /* … */
```

```cs
@import 'utils.styl'

body
  linear-gradient #333 #fff  
```

<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<!-- # Stylus Overview
## Questions? -->


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
    
<!-- <img class="slide-image" showInPresentation="true" src="\imgs\pic08.png" style="top:58.18%; left:90.52%; width:16.97%; z-index:-1" /> -->
<!-- <img class="slide-image" showInPresentation="true" src="\imgs\pic09.png" style="top:34.35%; left:68.14%; width:36.30%; z-index:-1" /> -->
<!-- <img class="slide-image" showInPresentation="true" src="\imgs\pic10.png" style="top:48.92%; left:75.91%; width:10.85%; z-index:-1" /> -->
<!-- <img class="slide-image" showInPresentation="true" src="\imgs\pic11.png" style="top:11.88%; left:91.56%; width:14.23%; z-index:-1" /> -->
