# Sass
Sass stands for `Systematically Awesome Style Sheets`.

It is a CSS pre-processor. It is an extension of CSS that is used to add power and elegance to the basic language. It facilitates you to add variables, nested rules, mixins, inline imports, inheritance and more, all with fully CSS-compatible syntax.

Sass is more stable and powerful CSS extension language that describes style of document cleanly and structurally. It is very useful to handle large style sheets by keeping them well organized and running quickly small style sheets.


## Features of Sass:

* Sass is fully CSS-compatible.
* It is more stable, powerful and elegant than CSS.
* It is based on JavaScript and is superset of CSS.
* It has its own syntax and compiles to readable CSS.
* It is an open-source pre processor that is interpreted into CSS.
* It supports language extensions such as variables, nesting, and mixins.
* It provides many useful functions for manipulating colors and other values.
* It provides many advanced features like control directives for libraries.
* It provides well-formatted, customizable output.

## SASS: Installation and Execution:

You have to install Ruby for executing the SASS files.

### Install Ruby:

To install Ruby, you have to follow the steps given below:
Go to the link `https://www.ruby-lang.org/en/downloads/ `,you will see a page like this.

![Install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/install1.PNG)

Download the ruby stable version and run the .exe file.

![Install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/install2.PNG)

Select the language.

![Install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/language.PNG)

Accept the term and conditions.

![Install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/terms.PNG)

Select the checkboxes. It will add ruby executable path automatically.
 
Click the install button.

![Install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/install3.PNG)

![Install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/finalinstall.PNG)

Installation complete. Now go to the start menu and open the command prompt with ruby.
Enter the following line: gem install sass

![Install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/command.PNG)

## SASS Example:

We can simply create SASS and SCSS example. To do so, use the following steps:
Create a HTML file having the following code:
### See this example:

### HTML code:  
```
<html>  
<head>   
   <title> Import example of sass</title>  
   <link rel="stylesheet" href="style.css"/>  
</head>   
<body>   
   <h1>Simple Sass Example</h1>   
   <h3>Welcome to JavaTpoint</h3>   
   <p>A solution of all technology.</p>   
</body>    
</html>
```

### Style.scss:
```
h1{
Color: #AF80ED;
}

h3{
Color: #DE5E85;
```

Now create a file named "style.scss". It is similar to CSS file. The only one difference is that it is saved with ".scss" extension. Put the both file inside the root folder.

Now, execute the following code: sass `--watch style.scss:style.css`

![Install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/syntax.PNG)

It will create a new CSS file named "style.css" inside the root folder automatically. Whenever you change the SCSS file, the style.css file will changed automatically.
The style.css file has the following code:

### Style.css:
```
h1{
Color: #AF80ED;
}

h3{
Color: #DE5E85;
```

Now execute the HTML file. It will read the CSS file and the output would be like this:

### Output:

![Install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/output.PNG)

### Architecture:

![Install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/archi.PNG)

### BASE FOLDER:
The base folder holds what we might call the boilerplate code for the project. In there, you might find the reset file, some typographic rules, and probably a stylesheet defining some standard styles for commonly used HTML elements (that I like to call _base.scss)
```
_base.scss
_reset.scss
_typography.scss
```


### LAYOUT FOLDER:
The layout/ folder contains everything that takes part in laying out the site or application. This folder could have stylesheets for the main parts of the site (header, footer, navigation, sidebar…), the grid system or even CSS styles for all the forms.
```
 _grid.scss
 _header.scss
 _footer.scss
 _sidebar.scss
 _forms.scss
 _navigation.scss
 ```


### COMPONENTS FOLDER:
For smaller components, there is the components/ folder. While layout/ is macro (defining the global wireframe), components/ is more focused on widgets. It contains all kind of specific modules like a slider, a loader, a widget, and basically anything along those lines. There are usually a lot of files in components/ since the whole site/application should be mostly composed of tiny modules.
```
_media.scss
_carousel.scss
_thumbnails.scss
```


### PAGES FOLDER:
If you have page-specific styles, it is better to put them in a pages/ folder, in a file named after the page. For instance, it’s not uncommon to have very specific styles for the home page hence the need for a _home.scss file in pages/.
```
_home.scss
_contact.scss
```


### THEMES FOLDER:
On large sites and applications, it is not unusual to have different themes. There are certainly different ways of dealing with themes but I personally like having them all in a themes/ folder.
```
_theme.scss
_admin.scss
```


### ABSTRACTS FOLDER:
The abstracts/ folder gathers all Sass tools and helpers used across the project. Every global variable, function, mixin and placeholder should be put in here.
The rule of thumb for this folder is that it should not output a single line of CSS when compiled on its own. These are nothing but Sass helpers.
```
_variables.scss
_mixins.scss
_functions.scss
_placeholders.scss
```
When working on a very large project with a lot of abstract utilities, it might be interesting to group them by topic rather than type, for instance typography (_typography.scss), theming (_theming.scss), etc. Each file contains all the related helpers: variables, functions, mixins and placeholders. Doing so can make the code easier to browse and maintain, especially when files are getting very long.


### VENDORS FOLDER:
And last but not least, most projects will have a vendors/ folder containing all the CSS files from external libraries and frameworks – Normalize, Bootstrap, jQueryUI, FancyCarouselSliderjQueryPowered, and so on. Putting those aside in the same folder is a good way to say “Hey, this is not from me, not my code, not my responsibility”.
```
_normalize.scss
_bootstrap.scss
_jquery-ui.scss
_select2.scss
```
If you have to override a section of any vendor, I recommend you have an 8th folder called vendors-extensions/ in which you may have files named exactly after the vendors they overwrite.

For instance, vendors-extensions/_bootstrap.scss is a file containing all CSS rules intended to re-declare some of Bootstrap’s default CSS. This is to avoid editing the vendor files themselves, which is generally not a good idea.


### MAIN FILE:
The main file (usually labelled main.scss) should be the only Sass file from the whole code base not to begin with an underscore. This file should not contain anything but `@import` and comments.

Files should be imported according to the folder they live in, one after the other in the following order:
```
abstracts/
vendors/
base/
layout/
components/
pages/
themes/
```

In order to preserve readability, the main file should respect these guidelines:
one file per `@import`;
one @import per line;
no new line between two imports from the same folder;
a new line after the last import from a folder;
file extensions and leading underscores omitted.

![Install](https://github.com/CharmiTrambadiya/Documents/blob/master/images/import.PNG)

### Variables:
Sass variables are used to store information that can be reused throughout the stylesheet when you need. You can store things like colors, font stacks, or any CSS value according to your future reusability.

The `$` symbol is used to make something a variable. See the syntax.

###### SCSS Syntax:
```
$title-font: normal 24px 'Open Sans', sans-serif;
$color-red: #F44336;

h1.title {
  font: $title-font;
  color: $color-red;
}

div.container {
  color: $color-red;
  background: #fff;
  width: 100%;
}
```

######  CSS OUTPUT:
```
h1.title {
  font: normal 24px "Open Sans",    sans-serif;
  color: #F44336;
}

div.container {
  color: #F44336;
  background: #fff;
  width: 100%;
}
```


### Mixins:
A mixin allows you to create reusable chunks of CSS. Being able to do this will help you to avoid writing repetitive code. For example:

###### SCSS Syntax:
```
@mixin square($size, $color) {
  width: $size;
  height: $size;
  background-color: $color;
}

.small-blue-square {
  @include square(20px, blue);
}

.big-red-square {
  @include square(300px, red);
}
```

######  CSS OUTPUT:
```
.small-blue-square {
  width: 20px;
  height: 20px;
  background-color: blue;
}

.big-red-square {
  width: 300px;
  height: 300px;
  background-color: red;
}
```

Another efficient way to use mixins is when a property requires prefixes to work in all browsers.

###### SCSS Syntax:
```
@mixin transform-tilt() {
  $tilt: rotate(15deg);

  -webkit-transform: $tilt; /* Ch <36, Saf 5.1+, iOS, An =<4.4.4 */
      -ms-transform: $tilt; /* IE 9 */
          transform: $tilt; /* IE 10, Fx 16+, Op 12.1+ */
}

.frame:hover {
  @include transform-tilt;
}
```

######  CSS OUTPUT:
```
.frame:hover {
  -webkit-transform: rotate(15deg);  /* Ch <36, Saf 5.1+, iOS, An =<4.4.4 */
  -ms-transform: rotate(15deg);  /* IE 9 */
  transform: rotate(15deg);  /* IE 10, Fx 16+, Op 12.1+ */
  ```

### Extends:
The `@extend` feature of Sass allows classes to share a set of properties with one another. In complicated CSS where many classes are put together, duplication of properties may occurs. The `@extend` features makes your code less and facilitates.

###### SCSS Syntax:
```
.message {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}
.success {
  @extend .message;
  border-color: green;
}
.error {
  @extend .message;
  border-color: red;
}
.warning {
  @extend .message;
  border-color: yellow;
}
```

######  CSS OUTPUT:
```
.message, .success, .error, .warning {
  border: 1px solid #cccccc;
  padding: 10px;
  color: #333;
}
.success {
  border-color: green;
}
.error {
  border-color: red;
}
.warning {
  border-color: yellow;
}
```

### Placeholder:
The point of a placeholder selector is that we are creating a set of rules that we never intend to be outputted into CSS except for later reference as an extend within other elements. We define our placeholder selectors through the use of a percent symbol `(%)` to denote that this selector will only ever be used as a reusable piece of code.

###### SCSS Syntax:
```
%list-style {
list-style: none;
padding: 0; }
.list-group {
@extend %list-style;
margin: 20px  20px; }
```

######  CSS OUTPUT:
```
.list-group {
list-style: none;
padding: 0; }
.list-group {
margin: 20px  20px; }
```

This is much more effective and avoids the risks of over-extending our Sass.

So in this chapter, we’ve seen the ways in which Sass can be used to avoid repetition in our CSS. We can use variables to take control of values we want to reuse throughout our styles. We can nest our Sass to define context and through the parent selector, we can keep our Sass files lean and efficient. Through extends, we can start to create reusable, modular styles and with the placeholder selector, we can begin to think about avoiding code bloat.

### Nesting:

HTML follows a strict nesting structure whereas in CSS it's usually total chaos. With Sass nesting you can organize your stylesheet in a way that resembles the HTML more closely, thus reducing the chance of CSS conflicts.

###### SCSS Syntax:
```
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```

######  CSS OUTPUT:
```
nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
nav li {
  display: inline-block;
}
nav a {
  display: block;
  padding: 6px 12px;
  text-decoration: none;
}
```

### Operators:

One of the nice features of Sass is that we can start to perform simple maths functions. Addition `(+)`, multiplication `(*)`, division `(/)` and subtraction `(-)` are all ways we can control and modify numbers within our Sass. We just need to make sure that we contain any mathematic operations within brackets.

###### SCSS Syntax:
```
.container {
  width: 100%;
}

article[role="main"] {
  float: left;
  width: 600px / 960px * 100%;
}

aside[role="complementary"] {
  float: right;
  width: 300px / 960px * 100%;
  ```

  ######  CSS OUTPUT:
  ```
  .container {
  width: 100%;
}

article[role="main"] {
  float: left;
  width: 62.5%;
}

aside[role="complementary"] {
  float: right;
  width: 31.25%;
}
```

### Functions:
A function is like a mixin but instead of returning code blocks, it can only be used to return values. As a nonsensical function.

```
@function squared($number) {
  @return ($number * $number);
 }
```

The`@return`command is specifying the value or string we want to return from our function.

One of the great things with Sass is that we can apply mathematics to variables featuring unit values. For example,

###### SCSS Syntax:
```
@function double($number) {
  @return ($number + $number);
}
.text {width: double(10px); }
```

######  CSS OUTPUT:
```
.text {width: 20px; }
```

As with mixins, we can declare as few or as many arguments as we want for our functions and also set default values:

###### SCSS Syntax:
```
@function line-height($font-size, $line-height: 1.5) {
  @return ($font-size * $line-height);
}
.text {line-height: line-height (18px); }
```

######  CSS OUTPUT:
```
.text {line-height: 27px; }
```

### Conditional Statements:

### if():
This is a little different in that it is not a control directive but a built in function in Sass. Not the same as the `@if directive`, `if()` allows you to test for a condition and return one of two possible values. The condition we test for is either true or false.

###### SCSS Syntax:
```
@mixin test($condition) {
    $color: if($condition, blue, red);
    color:$color
}

.firstClass {
    @include test(true);
}

.secondClass {
    @include test(false);
}
```

######  CSS OUTPUT:
```
.firstClass {color: blue;}
.secondClass {color: red;}
```

### @if:
The `@if` directive takes an expression and returns styles if it results in anything other than false or null.

###### SCSS Syntax:
```
@mixin txt($weight) {
    color: white;
    @if $weight == bold { font-weight: bold;}
}

.txt1 {
    @include txt(none);
}

.txt2 {
    @include txt(bold);
}
```

######  CSS OUTPUT:
```
.txt1 {
    color: white;
}

.txt2 {
    color: white;
    font-weight: bold;
}
```

We can expand on the @if directive with multiple @else if statements and one final @else. This way we can test for multiple conditions.

###### SCSS Syntax:
```
@mixin txt($weight) {
    color: white;
    @if $weight == bold { font-weight: bold;}
    @else if $weight == light { font-weight: 100;}
    @else if $weight == heavy { font-weight: 900;}
    @else { font-weight: normal;}
    }

.txt1 {
    @include txt(bold);
}

.txt2 {
    @include txt(light);
}

.txt3 {
    @include txt(heavy);
}

.txt4 {
 @include txt(none);
}

.txt5 {
    @include txt(normal)
}
```

######  CSS OUTPUT:
```
.txt1 {
    color: white;
    font-weight: bold;
}

.txt2 {
    color: white;
    font-weight: 100;
}

.txt3 {
    color: white;
    font-weight: 900;
}

.txt4 {
    color: white;
    font-weight: normal;
}

.txt5 {
    color: white;
    font-weight: normal;
}
```

###  @for:
The `@for` directive lets you output styles in a loop. The directive can be used either as a start through end or start to end. The difference is that start through end includes the ending number while start to end does not include the end number. The `@for` statement uses a variable to track the loop against the ranges. If we want to count down instead of up we would make our start number larger than our end number.

###### SCSS Syntax:
```
@for $i from 1 through 4 {
.p#{$i} { padding-left : $i * 10px;border:none; }
```

######  CSS OUTPUT:
```
.container .p1 {
padding-left: 10px;
 border: none; }
.container .p2 {
 padding-left: 20px;
 border: none; }
.container .p3 {
 padding-left: 30px;
 border: none; }
.container .p4 {
 padding-left: 40px;
 border: none; }
 ```

As you can see on each pass of the loop a style was created with the value of the variable added to the class name. We also did a calculation based on the variable to generate the proper width.

### @each:
The `@each` directive uses a list or map instead of starting and ending values. On each pass of the loop the variable gets assigned a value from the list or map.

###### Example:1
###### SCSS Syntax:
```
@each $usr in bob, john, bill, mike {
    .#{$usr}-avatar {
        background-image: url('/img/#{$usr}.png');
     }
}
```

######  CSS OUTPUT:
```
.bob-avatar {
    background-image: url("/img/bob.png");
}

.john-avatar {
    background-image: url("/img/john.png");
}

.bill-avatar {
    background-image: url("/img/bill.png");
}

.mike-avatar {
    background-image: url("/img/mike.png");
}
```

###### Example:2
###### SCSS Syntax:
```
@each $color in pink, violet, yellow, blue {
    .p_#{$color} {
      background-color: #{$color};
    }
  }
}
```

######  CSS OUTPUT:
```
.container .p_pink {
  background-color: pink;
 }
.container .p_violet {
  background-color: violet;
 }
.container .p_yellow {
  background-color: yellow;
 }
.container .p_blue {
  background-color: blue;
 }
 ```

### @while:
The `@while`directive outputs styles until the statement is false. Similar to the @for directive, the `@while` directive allows us more flexibility in our loops. I can rewrite the @for directive from above as a `@while` loop.

###### SCSS Syntax:
```
$i: 100;
@while $i > 0 {
  .paddding-#{$i} { padding-left: 1px * $i; }
  $i: $i - 20;
}
```

######  CSS OUTPUT:
```
.paddding-100 {
  padding-left: 100px; 
}
.paddding-80 {
  padding-left: 80px; 
}
.paddding-60 {
  padding-left: 60px; 
}
.paddding-40 {
  padding-left: 40px; 
}
.paddding-20 {
  padding-left: 20px; 
}
```

## Related Link:

* http://sass-lang.com/documentation/file.SASS_REFERENCE.html
* https://www.javatpoint.com/sass-tutorial
