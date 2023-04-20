# Introduction

To do anything in HTML we need a tag for it 

what is tag?

It is used to create different html elements. The text between left angular bracket (<) and right angular (>) is called as tag. 

syntax:

```python
<tag-name>
```

example: suppose we need to create a paragraph, so that we need paragraph html element ,now this element can be created by making use of <p> tag.

There are different types of tags:

1. Paired tags
2. non-paired tags
1. Paired tags:

The tags which have opening and closing tags are called paired tags.

syntax:

```html
<tag-name>
</tag-name>
```

example:

```html
<html>...</html>
<body>...</body>
```

1. non-paired tags

The tag that have only opening but no separate closing tag is called non-paired tags

syntax:

```html
<tag-name>
or
<tag-name/>
```

As we already know that HTML is used to create web pages, so how actually a web page is created?

To create a web page we need to follow the below given steps

1. Launch any text editor of your choice ie notepad, v s code, sublime text etc
2. write the below given code in the opened text editor
3. save the file with .html extension
4. Right click on the saved file and open with any of the browser
5. If any update required on the page, we need to open it with notepad(text editor), do the required changes and again save it.
6. Go to the web page and refresh it the changes will be replicated there .

From above discussion we came to know every webpage contains four critical components.

1. <html>
2. <head>
3. <title>
4. <body>

**HTML Basic Elements:**
1. <br> tag (line break)

Here br stands for break. It is used to break a line shift to next line . It is non-paired tag.

Syntax

```html
<br>
```

example:

```html
<html>
	<head>
		<title>Basic HTML Elements</title>
	</head>
	<body>
		Welcome to sneha and mathrushree's class...<br> We are web developers.
	</body>
</html>
```

1. &nbsp;

Non-breaking space

It is used to add non-breaking space between the characters and words.

It is an entity or special character of HTML.

Syntax

```html
&nbsp; -> creates one non-breaking space
&nbsp;&npsb; -> creates two non-breaking space
```

**Working with presentational tags:**

The presentational tags are popularly also known as formated tags.

Some important formated tags which are used frequently are given below.

```python
1.) bold    --> <b>......................</b> , <strong>...................</strong>
2.) italic  --> <i>......................</i> , <em>.......................</em>
3.) stricking effect --> <s> ..................</s> , 
4.) superscript --> <sup>.......................</sup>
5.) subscript -->   <sub>.......................</sub>
6.) blockquote ---> <blocquote>..................</blockquote>
7.) small   ---->   <small>......................</small>
8.) big     ---->   <big>........................</big>
9.) teletype ---->   <tt>.........................</tt>
	10.) <q>   ---->  <q>............................</q>
11.) <center>   -------> <center>...................</center>
```

example

```python
<htm>
    <head>
        <title>Formatted Tags</title>
    </head>
    <body>
        <b>It is in bold formate</b><br>
        <strong>It is also in bold formate</strong><br>
        <i>It is an italic formate</i><br>
        <em>It is also in italic formate</em><br>
        <s>It is removed content form the page</s><br>
        <strike>It is removed content</strike><br>
        <del>It is removed contents</del><br>
        <u>It is undelined content on the page.</u><br>
        It is the power of (100)<sup>2</sup><br>
        It is the base of (100)<sub>2</sub><br>
        <blockquote>It is always special to use blocquote.</blockquote><br>
        <small>small font is here.</small><br>
        <big>Big font comes into the picture</big><br>
        <tt>It is in teletype format</tt><br>
        <q>It is in quotes formate</q><br>
        <center>Page center</center>

    </body>
</htm>
```

**Attributes and Parameters:**

**Attributes:**

An attribute is used to add some extra meaning to the given tag.

It is popularly also known as properties.

important points about attribute:

1. It is always specified in the start tag.
2. Its values are enclosed either in single or double quotes
3. Attributes are special features of tags.
4. Each and every tag have it’s own attributes etc.

**Parameters:**

The values assigned to the attributes are called the parameters.

sytax:

```html
<tag-name attribute = "parameter">  ............. </tag-name>
or
<tag-name attribute = "parameter" />
```

Example:

```html
<body bgcolor = 'pink'>................</body> 
```

**Working with the body tag:**

body tag is the very important part of every html document, actually whatever we see on the web page is body of that page only. 

It is a major element which contains text, hyperlinks, special characters, tables, frames, forms etc.

It is a paired tag

syntax

```html
<body>............</body>
```

Some of the important body tag attributes and parameters

| Attributes | Parameters |
| --- | --- |
| bgcolor | color name/ hexadecimal color code |
| background | image path |
| text | color name / hexa decimal no |

example:

```html
<htm>
    <head>
        <title>Formatted Tags</title>
    </head>
    <body bgcolor="pink" text="blue">
        <b>It is in bold formate</b><br>
        <strong>It is also in bold formate</strong><br>
        <i>It is an italic formate</i><br>
        <em>It is also in italic formate</em><br>
        <s>It is removed content form the page</s><br>
        <strike>It is removed content</strike><br>
        <del>It is removed contents</del><br>
        <u>It is undelined content on the page.</u><br>
        It is the power of (100)<sup>2</sup><br>
        It is the base of (100)<sub>2</sub><br>
        <blockquote>It is always special to use blocquote.</blockquote><br>
        <small>small font is here.</small><br>
        <big>Big font comes into the picture</big><br>
        <tt>It is in teletype format</tt><br>
        <q>It is in quotes formate</q><br>
        <center>Page center</center>

    </body>
</htm>
```

example-2

```html
<htm>
    <head>
        <title>Formatted Tags</title>
    </head>
    <body background="background.jpg" text="blue">
        <b>It is in bold formate</b><br>
        <strong>It is also in bold formate</strong><br>
        <i>It is an italic formate</i><br>
        <em>It is also in italic formate</em><br>
        <s>It is removed content form the page</s><br>
        <strike>It is removed content</strike><br>
        <del>It is removed contents</del><br>
        <u>It is undelined content on the page.</u><br>
        It is the power of (100)<sup>2</sup><br>
        It is the base of (100)<sub>2</sub><br>
        <blockquote>It is always special to use blocquote.</blockquote><br>
        <small>small font is here.</small><br>
        <big>Big font comes into the picture</big><br>
        <tt>It is in teletype format</tt><br>
        <q>It is in quotes formate</q><br>
        <center>Page center</center>

    </body>
</htm>
```

**paragraph tag:**

It is used to create a paragraph . It is a paired tag.

syntax:

```html
<p>...............</p>
```

attributes

| attribute | parameter |
| --- | --- |
| align | left,right,center,justify |
|  |  |

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Paragraph</title>
</head>
<body>
    <p>I am a Paragraph one</p>
    <p>I am a pragraph two</p>
    <p>I am a paragraph three</p>
    <p>I am a paragraph four.</p>
</body>
</html>
```

Let’s see how paragraph works with different values of align attributes

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Paragraph</title>
</head>
<body>
    <p align="left">I am a Paragraph one</p>
    <p align="right">I am a pragraph two</p>
    <p align="center">I am a paragraph three</p>
    <p align="justify">I am a paragraph four.</p>
</body>
</html>
```

**Font tag:**

It is used to display formatted tag it is a paired tag.

Syntax:

```html
<font> ........</font>
```

font Attribtutes and parameters

| Attributes | Parameters |
| --- | --- |
| color | any color name or hexadecimal code |
| size | 1 to 7 |
| face | arial,tamhoma,....etc |

example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Fonts</title>
</head>
<body>
    <font color="pink" size="5" face="tahoma">Welcome to the fomatted text...</font>
</body>
</html>
```

**Heading in html**

It is used to create heading of our contents

There are six different heading tags in html, all are paired tag.

```html
<h1>..............................</h1> very important
<h2>..............................</h2>
<h3>...............................</h3>
<h4>................................</h4>
<h5>.................................</h5>
<h6>.................................</h6>  least important
```

example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Headings</title>
</head>
<body>
    <h1>I am most important heading</h1>
    <h2>I am second most important heading</h2>
    <h3>I am third most important heading</h3>
    <h4>I am fourth most important heading</h4>
    <h5>I am fifth most important heading</h5>
    <h6>I am least important heading</h6>
</body>
</html>
```

Attributes

| attribute | parameters |
| --- | --- |
| align | left,right,center |
|  |  |

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Headings</title>
</head>
<body>
    <h1 align="center">I am most important heading</h1>
    <h2 align="left">I am second most important heading</h2>
    <h3 align="right">I am third most important heading</h3>
    <h4>I am fourth most important heading</h4>
    <h5>I am fifth most important heading</h5>
    <h6>I am least important heading</h6>
</body>
</html>
```

Horizontal Rule(<hr>)

We can create a horizontal line in a html page by using <hr> tag, which is a non-paired tag.

syntax:

```html
<hr/> or <hr>
```

Different attributes for hr tag

| attributes |  parameters |
| --- | --- |
| color | any color or respective hexadecimal code |
| size | pixel  |
| width | % or pixel |
| align | left, right, center |
| noshade | noshade |

Note: If we put noshade then color attribute must be removed.

example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Horizontal Rule</title>
</head>
<body>
    <hr color="blue" size="2px" width="100px" align="left">
    <h1>HTML</h1>
    <hr color="red" size="4px" width="200px">
    <h2>CSS</h2>
    <hr color="green" size="6px" width="300px" align="right">
    <h3>JavaScript</h3>
    <hr size="8px" width="400px" align="center" noshade="noshade">
</body>
</html>
```

NOte:

1. The default width of the horizontal rule is 100%.
2. Default alignment of the hr is center
3. noshade attribute will be applied only when we are not specifying the color attribute.

**marquee tag:**

Using this tag we can create a scrolling text or scrolling image from left to right, right to left, top to bottom and bottom to up.

It is a paired tag.

syntax

```html
<marquee>.................</marquee>
```

example

```html
<!DOCTYPE html>
<html lang="en">
<head>

    <title>Marquee </title>
</head>
<body>
    <h2>Sale going on!!!!</h2>
    <marquee><strong>buy@500</strong></marquee>
</body>
</html>
```

Different attributes of marquee tag

| attributes | parameters |
| --- | --- |
| behaviour | “slide”- start and stop as soon as text touches the margin |
|  | “scroll” - start completely and off one side (default) |
|  | “alternate”- text bounce as soon as touches both the side margin. |
| bg color | color or respective hexadecimal color code |
| direction | “left”-  left to right |
|  | “right”- right to left |
|  | “up” - bottom to top |
|  | "down” - top to bottom |
| width | “size-px” - specifies width in marquee |
| height | “size-px” -specifies height in marquee |
| loop | “number” - loop continues in limited time |
| scrollamount | “number” - specifies speed to scrollon the text |

```html
<!DOCTYPE html>
<html lang="en">
<head>

    <title>Marquee </title>
</head>
<body>
    <h2>Sale going on!!!!</h2>
    <marquee behaviour="scroll">buy@500</marquee>
    <marquee behavior="slide" >Slide 600</marquee>
    <marquee behavior="alternate" >alternate</marquee>
</body>
</html>
```

example-2

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Marquee with attributes</title>
</head>
<body>
    <marquee behavior="scroll" bgcolor="orange">scrolling marqueee</marquee>
    <marquee behavior="slide">sliding marquee</marquee>
    <marquee behavior="alternate" bgcolor="lightgreen" width="150px" height="400px" direction='down'>Alternate marquee</marquee>
</body>
</html>
```

example-3: marquee with more attributes

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Marquee with attributes</title>
</head>
<body>
    <marquee behavior="scroll" bgcolor="orange" scrollamount="10">scroll with control</marquee>
    <marquee behavior="slide" loop="5" scrollamount="25">slide with control</marquee>
    <marquee behavior="alternate" scrollamount="50">alternate with control</marquee>
</body>
</html>
```

example-4 : marquee with javaScript events

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Marquee with JavaScript Events</title>
</head>
<body>
    <marquee behavior="scroll" bgcolor="orange" scrollamount="10">scroll with control</marquee>
    <marquee behavior="slide" loop="5" scrollamount="25" onmousedown="this.stop()" onmouseup="this.start()">slide with control</marquee>
    <marquee behavior="alternate" scrollamount="50" onmouseover="this.stop()" onmouseout="this.start()">alternate with control</marquee>
</body>
</html>
```

In above example we have used JS events with marquee tag as shown below

1. onmouseover = “this.stop()”
2. onmousedown=”this.stop()”
3. onmouseup = “this.start()”
4. onmouseout=”this.start()”

pre tag:

pre tag stands for pre formated text . IT displays unfomated text on the we page including spaces, line breaks, tabs and enters. It is a paired tag.

Syntax:

```html
<pre>....................</pre>
```

example: H       T        M            L

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Pre tag</title>
</head>
<body>
    <pre>
        H         T           M            L
    </pre>
    
</body>
</html>
```

img tag :

It is used to insert images on the web page. It is a non-paired tag.

Syntax:

```html
<img attribute="parameters" />
```

Different Attributes and Parameters for img is given below

| Attributes | Parameters |
| --- | --- |
| src | image path |
| border | border value generally in px |
| height | px or % |
| width | px or % |
| align | left,right, top, middle, bottom |
| alt | any text about that image |
| title | any text |

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Image tag</title>
</head>
<body>
    <img src="data:image/jpeg;base64,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" width="200px" height="200px" alt="sorry image doesn't exist"
    title="morning image" border="2px" />
    <img src="good morning guys" width="200px" height="200px" alt="sorry image doesn't exist"
    title="morning image" border="2px" />
    
</body>
</html>
```

**HTML Links**

Links are used to navigate easily from one webpage to other webpages or websites etc.

In HTML links are classified into two types

1. Internal links
2. External links

1. Internal links: Linking within the page and within the website is called as internal linking.
2. External links: Linking to external files like other documents, other websites or the other web pages are called external linking.

How links are created?

Links are created by using the `anchor tag` <a>....</a>. 

It is a paired tag.

Syntax:

```html
<a href="">..................</a>
```

Anchor tag attributes and parameters

| Attributes | Parameter |
| --- | --- |
| href | url(uniform resource location) |
| name | any name |
| target  | _blank, _parent etc |

Note: 

**Text links** : Text links allows programmers to create text that acts as a link, so that when it is clicked on by the user, it will transfer them to another web page

example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>LInks</title>
</head>
<body>
   <a href="http://engineeringcoders.com">engineeringcoders</a>
   <a href="http://google.com">search here</a> 
</body>
</html>
```

Target Attribute of anchor tag:

This attribute is used to display a page or website in a specific location.

example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>LInks</title>
</head>
<body>
   <a href="http://engineeringcoders.com">engineeringcoders</a>
   <a href="http://google.com">search here</a> 
   <a href="http://engineeringcoders.com" target="_blank">engineeringcoders</a>
   <a href="http://google.com" target="_parent">search here</a> 
</body>
</html>
```

**Picture links:**

A picture link allows the programmer to create a picture that act as a link so that when it is clicked by the user it transfer them to another page or site.

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <title>LInks</title>
</head>
<body>
   <a href="http://engineeringcoders.com"><img src="https://media.geeksforgeeks.org/wp-content/uploads/20191205185435/Untitled-drawing-61.png" width="300px" height="300px" alt="html image"></a>
   <a href="http://google.com">search here</a> 
   <a href="http://engineeringcoders.com" target="_blank">engineeringcoders</a>
   <a href="http://google.com" target="_parent">search here</a> 
</body>
</html>
```

**Local Links:**

These links allows programmer to connect to client system resources.

example

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <title>LInks</title>
</head>
<body>
   <a href="file :///D:\Software Training Classes\MERN-730\classes\class-6\images\demo.jpg">Local link</a>
   
</body>
</html>
```

**HTML Tables**

Tables are used to represent our data in a tabular format. The best way to split a page with the help of tables. It is a paired tag.

Syntax:

```html
<table>...</table>
```

Table rows:

Horizontal links represents as row .

To create a row inside a table we make use of <tr> ...</tr> tag. It is a paired tag

Syntax:

```html
<table>
	<tr>..</tr>
</table>
```

Cells/columns:

Each row in a table consist of a number of cells. Each cells defined by a tag. The tag looks like <td>..</td>.

the insertion of rows and columns are called as cells.

Syntax:

```html
<table>
	<tr>
		<td>column-1</td>
		<td>column-2</td>
	</tr>
</table>
```

Table heading

To represent table heading we use the <th>..</th> tag 

syntax:

```html
<table>
	<tr>
		<th>heading-1</th>
		<th>heading-2</th>
	<tr>
	<tr>
		<td>column-1</td>
		<td>column-2</td>
	</tr>
</table>
```

**Table tag attributes and Parameters:**

| Attributes | Parameters |
| --- | --- |
| border | pixels |
| border-color | any color / color code(hexa) |
| bgcolor | any color/color code (hex) |
| background | image path |
| height | pixels or % |
| width | pixels or % |
| align | left, right, center |
| valign | top, middle, bottom |
| cellspacing | pixels |
| cellpadding | pixels |
| rowspan | number |
| colspan | number |

example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>LInks</title>
</head>
<body>
   <table border="1px" border-color="blue" bgcolor="yellow" background="images/demo.jpg">
    <tr>
        <th>Std No</th>
        <th>Std Name</th>
    </tr> 
    <tr>
        <td>100</td>
        <td>Mathrushree</td>
    </tr>
    <tr>
        <td>200</td>
        <td>Sneha</td>
    </tr>
   </table>
   
</body>
</html>
```

Table attributes at cell level

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>LInks</title>
</head>
<body>
   <table border="1px" border-color="blue" bgcolor="yellow" background="images/demo.jpg">
    <tr>
        <th>Std No</th>
        <th>Std Name</th>
    </tr> 
    <tr>
        <td>100</td>
        <td>Mathrushree</td>
    </tr>
    <tr>
        <td>200</td>
        <td>Sneha</td>
    </tr>
   </table>

   <!-- table attributes at cell level -->
   <table border="1px" border-color="red">
       <tr>
           <th>Std No</th>
           <th>Std Name</th>
       </tr>
       <tr>
           <td>100</td>
           <td bgcolor="lightgreen" background="/images/demo.jpg">Sneha</td>
       </tr>
       <tr>
           <td>200</td>
           <td bgcolor="lightblue" background="/images/demo.jpg">Mathrushree</td>
       </tr>
   </table>
   
</body>
</html>
```

Table tag with width and height property

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>LInks</title>
</head>
<body>
   <table border="1px" border-color="blue" bgcolor="yellow" background="images/demo.jpg">
    <tr>
        <th>Std No</th>
        <th>Std Name</th>
    </tr> 
    <tr>
        <td>100</td>
        <td>Mathrushree</td>
    </tr>
    <tr>
        <td>200</td>
        <td>Sneha</td>
    </tr>
   </table>

   <!-- table attributes at cell level -->
   <table border="1px" border-color="red">
       <tr>
           <th>Std No</th>
           <th>Std Name</th>
       </tr>
       <tr>
           <td>100</td>
           <td bgcolor="lightgreen" background="/images/demo.jpg">Sneha</td>
       </tr>
       <tr>
           <td>200</td>
           <td bgcolor="lightblue" background="/images/demo.jpg">Mathrushree</td>
       </tr>
   </table>

   <!-- Table with widht and height property -->
    <table border="1px" border-color="red" width="250px" height="200px">
        <tr>
            <th>Std No</th>
            <th>Std Name</th>
        </tr>
        <tr>
            <td>100</td>
            <td bgcolor="lightgreen" background="/images/demo.jpg" width="100px" height="100px">Sneha</td>
        </tr>
        <tr>
            <td>200</td>
            <td bgcolor="lightblue" background="/images/demo.jpg">Mathrushree</td>
        </tr>
    </table>
   
</body>
</html>
```

**Rules Attribute:**

It supports the following list of values

1. rows
2. cols
3. all
4. none 

Example:

```python
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Table rules attributes</title>
</head>
<body>
    <table rules="none" border="1px">
        <tr>
            <th>Std No.</th>
            <th>Std Name</th>
        </tr>
        <tr>
            <td>101</td>
            <td>Sneha</td>
        </tr>
        <tr>
            <td>102</td>
            <td>Mathrushree</td>
        </tr>
    </table>
    <table rules="row" border="1px">
        <tr>
            <th>Std No.</th>
            <th>Std Name</th>
        </tr>
        <tr>
            <td>101</td>
            <td>Sneha</td>
        </tr>
        <tr>
            <td>102</td>
            <td>Mathrushree</td>
        </tr>
    </table>
    <table rules="cols" border="1px">
        <tr>
            <th>Std No.</th>
            <th>Std Name</th>
        </tr>
        <tr>
            <td>101</td>
            <td>Sneha</td>
        </tr>
        <tr>
            <td>102</td>
            <td>Mathrushree</td>
        </tr>
    </table>
</body>
</html>
```

Cell Spacing:- 

This attribute controls the distance between cell:

example:

```html
 <table cellspacing="x">
```

Cell padding:

IT controls the distance between the text in the cell and the edge of the cell.

syntax:

```html
<table cellpadding="x">
```

example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Table rules attributes</title>
</head>
<body>
    <h2>Table with cellpadding and cellspacing</h2>
    <table  border="1px" cellspacing="10px" cellpadding="10px">
        <tr>
            <th>Std No.</th>
            <th>Std Name</th>
        </tr>
        <tr>
            <td>101</td>
            <td>Sneha</td>
        </tr>
        <tr>
            <td>102</td>
            <td>Mathrushree</td>
        </tr>
    </table>

    <h2>Table without cellpadding and cellspacing</h2>
    <table rules="row" border="1px">
        <tr>
            <th>Std No.</th>
            <th>Std Name</th>
        </tr>
        <tr>
            <td>101</td>
            <td>Sneha</td>
        </tr>
        <tr>
            <td>102</td>
            <td>Mathrushree</td>
        </tr>
    </table>
    <table rules="cols" border="1px">
        <tr>
            <th>Std No.</th>
            <th>Std Name</th>
        </tr>
        <tr>
            <td>101</td>
            <td>Sneha</td>
        </tr>
        <tr>
            <td>102</td>
            <td>Mathrushree</td>
        </tr>
    </table>
</body>
</html>
```

**Table tag with entities:**

Entities are special characters, these characters are developed for special meaning in HTML. 

If we remove the text within the cell, cell will be disappeared on the web page that time we should implement non breaking space for all browsers compatibility.

Syntax of an entity:

It should start with & symbols

It should end with ; symbol.

```html
1. non-breaking space - &nbsp;
```

example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Table rules attributes</title>
</head>
<body>
    <h2>Table with cellpadding and cellspacing</h2>
    <table  border="1px" cellspacing="10px" cellpadding="10px">
        <tr>
            <th>Std No.</th>
            <th>Std Name</th>
        </tr>
        <tr>
            <td>101</td>
            <td>Sneha</td>
        </tr>
        <tr>
            <td>102</td>
            <td>Mathrushree</td>
        </tr>
    </table>

    <h2>Table without cellpadding and cellspacing</h2>
    <table rules="row" border="1px">
        <tr>
            <th>Std No.</th>
            <th>Std Name</th>
        </tr>
        <tr>
            <td>101</td>
            <td>Sneha</td>
        </tr>
        <tr>
            <td>102</td>
            <td>Mathrushree</td>
        </tr>
    </table>

    <h2>Table with entities</h2>
    <table  border="1px">
        <tr>
            <th>Std No.</th>
            <th>Std Name</th>
        </tr>
        <tr>
            <td>101</td>
            <td>Sneha</td>
        </tr>
        <tr>
            <td>102</td>
            <td>Amrutha &nbsp; &nbsp; Potta</td>
        </tr>
    </table>
</body>
</html>
```

**Table- colspan and rowspan**:

Using the attributes colspan and rowspan we can extend columns and rows across the multiple other columns and rows

1. column span(colspan):

It extends cells on a horizontal row( left to right)

Syntax: 

```html
<td colspan="x">
```

example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Table rules attributes</title>
</head>
<body>
    <h2>Table with cellpadding and cellspacing</h2>
    <table  border="1px" cellspacing="10px" cellpadding="10px">
        <tr>
            <th>Std No.</th>
            <th>Std Name</th>
        </tr>
        <tr>
            <td>101</td>
            <td>Sneha</td>
        </tr>
        <tr>
            <td>102</td>
            <td>Mathrushree</td>
        </tr>
    </table>

    <h2>Table without cellpadding and cellspacing</h2>
    <table rules="row" border="1px">
        <tr>
            <th>Std No.</th>
            <th>Std Name</th>
        </tr>
        <tr>
            <td>101</td>
            <td>Sneha</td>
        </tr>
        <tr>
            <td>102</td>
            <td>Mathrushree</td>
        </tr>
    </table>

    <h2>Table with entities</h2>
    <table  border="1px">
        <tr>
            <th>Std No.</th>
            <th>Std Name</th>
        </tr>
        <tr>
            <td>101</td>
            <td>Sneha</td>
        </tr>
        <tr>
            
            <td colspan=3 align="center">V</td>
        </tr>
    </table>
</body>
</html>
```

![table-colspan.PNG](Introduction%202d4f3e764daa41c0a7b8ff7133d463f5/table-colspan.png)

**rowspan:**

It extends rows on a vertical row up and down.

syntax:

```html
<td rowspan=x>
```

example:

```html
<!DOCTYPE html>
<html>
	<head>
		<title>HTML rowspan Attribute</title>
	</head>

	<body style = "text-align:center">

		
		<h2>HTML rowspan Attribute</h2>

		<table border="1px">
			<tr>
				<th>Name</th>
				<th>Age</th>
			</tr>
			<tr>
				<td>Sneha</td>
				<!-- This cell will take up space on
					two rows -->
				<td rowspan="2">24</td>
			</tr>
			<tr>
				<td>Mathrushree</td>
			</tr>
		</table>
		
	</body>
</html>
```

Table data alignments:

To align the data inside the table we can use the following 2 ways:

1. Horizontal alignment
2. Vertical alignment

1. Horizontal aligment:
We can align the text horizontally in 3 ways ie left(default) , center and right.

1. Vertical alignment: 

We can align the text vertically in 3 ways:

1. top
2. middle
3. bottom.

Working with HTML frames:

Frames are used to embed multiple html files in a single browser window.

<frameset> tag:

Using this tag we can divide the webpage as a multiple frames. In each frame we can display another website. Frameset tag is a paired tag.

Syntax:

```jsx
<frameset>................</frameset>
```

Attributes and respective parameters: 

| Attributes | Parameters |
| --- | --- |
| rows | px, % |
| cols | px, % |
| border | px |
| bordercolor | any color name/hexadecimal  |

<frame> tag:

This tag is used to called external webpages. It contains src property to specify the path of external webpage.

Using frames we can place and view multiple files in a single window.

It is a non-paired tag.

syntax:

```jsx
<frame />
```

Attributes and parameters

| attributes | Parameters |
| --- | --- |
| src | file path, external resources |
| name | any name |
| scrolling | yes, no, default |

example:

```jsx

```

**HTML Forms**

Forms are used to create dynamic website. By using forms end user is able to interact directly with application. It is a paired tag.

syntax: 

```jsx
<form> ................</form>
```

Attributes and Paramters

| Attributes | Parameters |
| --- | --- |
| name | any name |
| method |  get, post |
| action | url(uniform resource locator) |

form tags:

form supports the following list of tag controls

| tag | Description |
| --- | --- |
| <form> | it defines a form for user input |
| <input> | defines an input field data |
| <button> | It defines push button. |
| <textarea> | It defines a text area( a multiline text input box) |
| <label> | It defines a label to the description. |
| <legend> | It defines a caption name write into fieldset |
| <select> | It defines a drop-down select list box |
| <option> | It defines an option value in the drop down box. |

Types of form fields:

Form fields are classified into the two types:

1. Input fields
2. Select fields
1. Input fields:

Form supports various input fields. Some of the major input fields are shown below

| Fieldname | keyword | Syntax |
| --- | --- | --- |
| textbox | text | <input type=”text”> |
| password box | password | <input type=”password”> |
| checkbox | checkbox | <input type=”checkbox”> |
| radio buttons | radio | <input type=”radio” > |
| submit button | submit | <input type=”submit”> |
| reset button | reset | <input type=”reset”> |
| text area  | textarea | <input type=”textarea”> |

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Registration Form</title>
</head>
<body>
    <form >
        <label>User Name:</label><br>
        <input type="text"><br>
        <label >Password:</label><br>
        <input type="password"><br>
        <input type="submit">
    </form>
</body>
</html>
```

Attributes and Parameters of form input fields:

| Attributes | Parameters |
| --- | --- |
| name | any name |
| value | any value |
| size | px |
| maxlength | number |
| rows | number |
| cols | number |
| readonly | true, false |
| disabled | disabled |
| checked | checked |
| multiple | true/false. |

Drawbacks of HTML4 :

1. It doesn’t supports graphics .
2. Poor in video/audio supports.
3. It needs external support to run flash, media controls.
4. Very few input controls are available .
5. It needs to use external language like JavaScript to validate controls.
6. HTML4 doesn’t supports 2d and 3d animations.

Due to the above drawbacks further advancement was done in HTML and HTML5 was introduced, which contains various new features and also it have removed some of the old features.

Some of the elements which are deprecated further to be used in HTML5

1. <acronym>
2. <applet>
3. <basefont>
4. <big>
5. <center>
6. <dir>
7. <font>
8. <frame>
9. <frameset>
10. <noframes>
11. <s>
12. <strike>
13. <tt>
14. <u>
15. <xmp>

etc 

Features of HTML5:

It is the latest version developed by w3c(world wide web consortium) and WHATWG. HTML5 has the below enlisted features

1. HTML5 symantic elements
2. HTML inline elements
3. Advanced forms
4. Advanced form input types
5. Latest form attributes
6. Updated input attributes
7. New form elements 
8. HTML5 multimedia.
9. HTML5 Web RTC(Real time communication)
10. HTML5 graphics( 2d and 3d)
11. HTML5 canvas
12. HTML5 SVG( Scalable  Vector Graphics)
13. Math ML( Mathematical Markup language.)
14. HTML5 Geolocation.
15. HTML5 drag and drop.
16. HTML5 web storage.
17. Server sent events.
18. HTML5 web workers.
19. HTML5 application cache.
20. HTML5 speech input.
21. good performance and integration.

Demo html5 program

```python
<!-- Version Information -->
<!DOCTYPE html>
<!-- the document will use english India language -->
<html lang="en-IN">
    <head>
        <title>HTML 5</title>
        <link href="https://cdn.pixabay.com/photo/2017/08/05/11/16/logo-2582748_1280.png" rel="icon" type="image/icon">
        <!-- meta element -->
        <!-- meta catergories -->
        <!-- 1. meta charset: generally utf-8 
             2. meta keywords: keywords related to search engine like google, yahoo, mozilla etc
             3. meta description: It defines description of our page
             4. meta title: If defines title of the meta content.
             5. meta author. It defines the autor of the web page.
        -->
        <meta charset="utf-8" />
        <meta name="keywords" content="HTML5 keywords list" />
        <meta name="description" content="HTML5 is latest version of the HTML used in the Web developement." />
        <meta name="title" content="Introduction to the HTML5"/>
        <meta name="author" content="MERN Developers"/>
        <!-- JavaScript which needs to run before loading content of the page -->
        <script type="text/javascript" language="javascript"></script>
    </head>
    <body>
        
    </body>
    
</html>
```

HTML4 Page Layout:

In html4 page layouts are as follows:

```python
<html>
    <head>
        <title>HTML4 Page Layout</title>
    </head>
    <body>
        <div id="header"></div>
        <div id="nav"></div>
        <div id="section"></div><div id="aside"></div>
        <div id="article"></div>
        <div id="footer"></div>
    </body>
</html>
```

HTML5 page layout:

HTML5 supports symantics, with the help of semantics we can design updated layouts. So HTML5 will provide more detailed document sturcture.

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>Page Layout using HMTL5</title>
    </head>
    <body>
        <header>Page Header</header>
        <nav>Navigation Bar</nav>
        <section>
            <header>Section Header</header>
            <article>
                <p>This is demo article paragraph.</p>
            </article>
            <footer>Section Footer</footer>
        </section>
        <aside>SideBar</aside>
        <footer>Page Footer</footer>
    </body>

</html>
```

HTML5 semantics: HTML5 supports some new elements for bettter structure which are given below.

1. <section>
2. <article>
3. <header>
4. <footer>
5. <hgroup>
6. <aside>
7. <command>
8. <details>
9. <summary>
10. <figure>
11. <figcaption>
12. <nav>
13. <wbr>
14. <bdi>
15. <bdo>
16. <ruby>
17. <rt>
18. <rp>

All the elements can be classified into different types of semantics as given below:

Different types of semantics:

1. General semantics
2. Arabic semantics
3. Chinese semantics

1. General semantics:

a. section: It defines section in a document such as chapters, headers, footers any other section of the dcoument. 

It is paired tag. with syntax:

```html
<section>......</section>
```

Attributes: No element specific 

b. header: It is used to display sub-headings, version information, navigational controls etc.

IT is a  paired tag.

Syntax

```html
<header>..............<header>
```

Note: A <header> tag cannot be placed within a <footer>.

Attribute: NO element specific attributes.

c. footer: It is used to define footer of an html document or section. IT is a paired tag

Syntax:

```html
<footer>....</footer>
```

Attributes: No element specific attributes.

d. article: It is used to represent an article, It is an independent content on the web [page.](http://page.It) It is a paired tag.

Syntax: 

```html
<article>...........</article>
```

**Architecture of semantics:**

![semantics.png](Introduction%202d4f3e764daa41c0a7b8ff7133d463f5/semantics.png)

Example:

```python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>The semantics of HTML5</title>
    <meta name="keywords" content="List of required keywords for page.">
    <meta name="description" content="List of required page description">
    <meta name="title" content="Required title for the meta content">
    <meta name="author" content="Kirti">
    <style>
        /* Our style comes here */
    </style>
    <script>
        // All the scripts which needed to load before the content comes here
    </script>
</head>
<body>
    <section>
        <header>The HTML5</header>
        <article>
            <header>Introduction to HTML5</header>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit recusandae unde quisquam in, dolor libero sapiente, omnis facere, molestiae modi reiciendis quaerat. Nam rem vitae deleniti distinctio architecto ducimus ex?</p>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Consequatur, impedit. Autem perspiciatis ducimus dolor explicabo, sit quas quam natus nobis non blanditiis accusantium rerum eligendi, vero dolore, labore soluta vitae.</p>
            <footer>All copyright reserved &copy;</footer>
        </article>
        <footer>Content rights protected &reg;</footer>
    </section>
</body>
</html>
```

**<hgroup>:** 

IT is used to group a set of one or more headings h1 to h6 elements. It is a paired tag.

syntax:

```python
<hgroup>..............</hgroup>
```

Attribute: Element specific attributes are none.

example:

```python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">

    <title>heading group</title>
</head>
<body>
    <hgroup>
        <h1>Power of HTML5</h1>
        <h2>Introduction to the Web portal.</h2>
    </hgroup>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Repudiandae quaerat debitis, officiis iste accusantium culpa aperiam porro, non deserunt ipsam quas repellendus aut similique ad qui temporibus. Excepturi, aperiam labore?</p>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam eaque maiores fugit neque tempore necessitatibus illo, nostrum corporis sed doloremque, repudiandae, expedita quia unde quam ex quo! Eaque, eum nobis.</p>
</body>
</html>
```

**<aside>:**

It is used to represent content that is related to surrounding content within an article or web page which can still stand alone in its own right.

It is a paired tag.

example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Aside</title>
</head>
<body>
    <aside>HTML5 is new Hypertext Markup Language.</aside>
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Tenetur minus aspernatur amet saepe quo eum modi beatae nostrum vel ipsa ex aperiam aliquam soluta, optio quaerat delectus itaque sit laboriosam?</p>
    
</body>
</html>
```

![aside.PNG](Introduction%202d4f3e764daa41c0a7b8ff7133d463f5/aside.png)

Aside with image:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Aside with image</title>
</head>
<body>
    <aside style="font-size: larger; font-style: italic; color: blue; float: left; width: 120px;"><img src="https://i.pinimg.com/564x/eb/dd/03/ebdd03c44b9c6f0fc64256284c5c4986.jpg" alt="morning-wish-image" width="100px" height="100px"></aside>
    <p align="justify">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Tenetur minus aspernatur amet saepe quo eum modi beatae nostrum vel ipsa ex aperiam aliquam soluta, optio quaerat delectus itaque sit laboriosam?</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium, voluptates veritatis. Harum architecto voluptates expedita omnis placeat magni voluptatem nemo animi reprehenderit? Temporibus cumque dolorum numquam officiis, incidunt consequuntur exercitationem.</p>
</body>
</html>
```

output:

![aside-with-image.PNG](Introduction%202d4f3e764daa41c0a7b8ff7133d463f5/aside-with-image.png)

**<command>**: It defines a command that the user can invoke. It is a paired tag.

sytax:

```html
<command>........</command>
```

**<details>**: IT is used to create an interative widget that the user can open and close. It is a paired tag.

Syntax:

```jsx
<details>............</details>
```

Attributes

| Attribute | Value | Description |
| --- | --- | --- |
| open | open | specifies that the details should be visible (open) to the user. |
|  |  |  |

**<summary>**: It defines the visible heading for the <details> element. The heading can be clicked to view/hide the details. It is a paired tag.

Syntax:

```jsx
<details>
	<summary>.........</summary>
</details>
```

Note: The <summary> tag is currently only supported in chrome & opera.

Note: The <summary> element should be the first child of <details> element.

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Widget</title>
</head>
<body>
    <details open="open">
        <summary>power of HTML5</summary>
        <p>file system </p>
        <p>Geoloation</p>
        <p>Semantics</p>
    </details>

    <!-- second widget -->
    <h2>Improved widget</h2>
    <details>
        <summary style="color:red">Power of HTML5</summary>
        <ul type="square" style="color: green; font-family: tahoma;">
            <li>File System</li>
            <li>Geoloation</li>
            <li>Semantics</li>
        </ul>
    </details>
</body>
</html>
```

<figure>: It is used to apply a unit of element like images and group of text. It is a paired tag.

syntax:

```jsx
<figure>....</figure>
```

Attribute: No element specific attribute are there.

<figcaption>: It defines a caption for figure element. This element represents a caption or a legend for a figure. It is a paired tag.

Syntax:

```jsx
<figure>
	<figcaption>...<figcaption>
</figure>
```

Attribute: Element specific attribute are None.

example;

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Figure Tags</title>
</head>
<body>
    <figure>
        <img src="https://media.geeksforgeeks.org/wp-content/uploads/20191205185435/Untitled-drawing-61.png" alt="html-pic">
        <figcaption>It is html5 logo from W3C and WHATWANG</figcaption>
    </figure>
</body>
</html>
```

**<nav>**: It is used to declare navigational section of HTML document. It is a paired tag.

Syntax:

```jsx
<nav>..........</nav>
```

Attributes: Element specific attribute is None.

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Navigation tag</title>
</head>
<body>
    <nav>
        <a href="https://www.google.com">Google</a>
        <a href="https://engineeringcoders.com">Blog</a>
    </nav>
</body>
</html>
```

**<wbr>**: It is used to word break opportunity. It is a non-paired tag.

Syntax: 

```jsx
<wbr>
```

Attribute: Element specific attributes are None.

eample;

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Navigation tag</title>
</head>
<body>
    <nav>
        <a href="https://www.google.com">Google</a>
        <a href="https://engineeringcoders.com">Blog</a>
    </nav>
    <p>To learn HTML5 you must be familiar with HTML <wbr> CSS <wbr>JS...</p>
</body>
</html>
```

**<bdo>**: It is used to overright the current text direction. It can be useful when displaying hebrew and other languages. It is a paired tag.

```jsx
<dbo>......</bdo>
```

Attributes

| Attribute | value | Description |
| --- | --- | --- |
| dir | ltr | Specifies the text direction |
|  | rtl | Specifies the text direction |

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>bdo tag</title>
</head>
<body>
    <bdo dir="rtl">HTML is new hypertext markup language.</bdo>
</body>
</html>
```

**<bdi>**: bidirectional isolation.

This can be useful when displaying right to left text. It is paired tag.

Syntax:

```jsx
<bdi>...</bdi>
```

Attribute: Element specific attribute are none

**HTML5 Inline Elements**

HTML5 supports the following inline elements

1. <mark>
2. <meter>
3. <progress>
4. <time>

**1.<mark>:** It is used for indicating text as marked or highlighted for reference purpose. It is a paired tag.

syntax:

```jsx
<mark>........</mark>
```

Attributes: Element specific attributes are none.

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Inline Elments</title>
</head>
<body>
    <p>
        <mark>HTML5</mark> is new Hypertext markup language for mobile apps...!.
        <mark style="background-color: lightblue;">HTML5</mark> is new Hypertext markup language for mobile apps...!.
    </p>
</body>
</html>
```

**2. meter:** It defines a scalar measurement within a known range. This is also known as guage. It is a paired tag.

Syntax:

```jsx
<meter>.......</meter>
```

Attributes

| Attribute | value | Description |
| --- | --- | --- |
| form | form_id | specify one or more forms. |
| high | number | specifies the range that considered to be high |
| low  | numer | specifies the range that is considered to be low |
| max | number | speccifies the maximum value of the range. |
| min | number | specifies the minimum value of the range. |
| optimum | number | specifies what value is the optimum value for the guage. |
| value | number | specifies the current value for the guage. |

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Inline Elments</title>
</head>
<body>
    <p>
        <mark>HTML5</mark> is new Hypertext markup language for mobile apps...!.
        <mark style="background-color: lightblue;">HTML5</mark> is new Hypertext markup language for mobile apps...!.
    </p>
    <meter value="2" max="10">
        <p style="color: red;">OOPs your browser not supporting the meter tag.</p>
    </meter> <br>
    <meter value="9" max="10">
        <p style="color: red;">meter tag is here</p>
    </meter>
</body>
</html>
```

NOte:

1. If value is higher than high then the guage will be yellow.(when low is available)
2. When value is lower than low than if optimum is lower than low then guage is green.
3. If value is more than high then optimum is red(when max attribute is available) 

**3. <progress>**

It is used to represent progress of a task. It is a paired tag.

Syntax: 

```jsx
 <progress>.........</progress>
```

Attributes

| Attribute | value | Description |
| --- | --- | --- |
| max | number | specifies how much work the task required in total. |
| value | number | specifies how much of the task has been completed |

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Inline Elments</title>
</head>
<body>
    <p>
        <mark>HTML5</mark> is new Hypertext markup language for mobile apps...!.
        <mark style="background-color: lightblue;">HTML5</mark> is new Hypertext markup language for mobile apps...!.
    </p>
    <meter value="2" max="10">
        <p style="color: red;">OOPs your browser not supporting the meter tag.</p>
    </meter> <br>
    <meter value="9" max="10">
        <p style="color: red;">meter tag is here</p>
    </meter>
    <br>
    <h2>exam performance</h2>
    <p>He got a <meter low="60" high="80" max="100" value="100"></meter> in the exam.</p>
    <p>He got a <meter  high="80" max="100" value="84"></meter> in the exam.</p>
    <p>He got a <meter max="100" min="10" value="50"></meter> in the exam.</p>
    <!-- progress bar -->
    <progress value="5" max="10">
        <p style="color: red;">I am a progress bar</p>
    </progress>
</body>
</html>
```

**4. <time>:**

This element is used to presenting dates and times in machine readable formats.. It is a paired tag.

Syntax:

```jsx
<time>........</time>
```

Attributes:

| attribute | value | Description |
| --- | --- | --- |
| datatime | datetime | Gives the datetime being specified |

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Inline Elments</title>
</head>
<body>
    <p>
        <mark>HTML5</mark> is new Hypertext markup language for mobile apps...!.
        <mark style="background-color: lightblue;">HTML5</mark> is new Hypertext markup language for mobile apps...!.
    </p>
    <meter value="2" max="10">
        <p style="color: red;">OOPs your browser not supporting the meter tag.</p>
    </meter> <br>
    <meter value="9" max="10">
        <p style="color: red;">meter tag is here</p>
    </meter>
    <br>
    <h2>exam performance</h2>
    <p>He got a <meter low="60" high="80" max="100" value="100"></meter> in the exam.</p>
    <p>He got a <meter  high="80" max="100" value="84"></meter> in the exam.</p>
    <p>He got a <meter max="100" min="10" value="50"></meter> in the exam.</p>
    <!-- progress bar -->
    <progress value="5" max="10">
        <p style="color: red;">I am a progress bar</p>
    </progress>
    <!-- time tag -->
    <p>We arrived at <time>7:30</time></p>
</body>
</html>
```

### Working with HTML4 forms

→Form is a container it can hold other controls. It is a paired tag.

Syntax:

```python
<form>..........</form>
```

Attributes

| Attribute | Parameter |
| --- | --- |
| name | any name for your form |
| method | GET,POST |
| acction | url(unifrom resource loactor) |

> 
> 

## Form tags

| Tag | Desction |
| --- | --- |
| <form> | Defines a form for user input |
| <input> | Defines an input field data |
| <button> | Defines a push button |
| <textarea> | Defines a text area |
| <label> | Defines a label to the description |
| <fieldset> | Defines a border to the input data. |
| <legend> | Defines a caption name written into fieldset |
| <select> | Defines a caption name written into fieldset |
| <option> | Defines an option value in dropdown box. |

> Types of forms Fields:
> 
> 
> Form fields are classified into two types
> 
> 1. Input Form Fields
> 2. Select Form Fields
1. Input Form Field:

These Fields are used to fetch input from the users. The below is the list of input form fileds

| Field Name | Keyword | Syntax |
| --- | --- | --- |
| text box | text | <input type=”text> |
| password box | password | <input type=”password”> |
| checkbox | checkbox | <input type=”checkbox”> |
| radio button | radio | <input type=”radio”> |
| reset button | reset | <input type=”reset” |
| submit button | submit | <input type=”submit”> |
| text area  | textarea | <input type=”textarea”> |

Example:

form-input.html

```python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Form Input Fields</title>
</head>
<body>
    <form>
        <label>User Name:</label><br/>
        <input type="text"><br/>
        <label >Password:</label><br>
        <input type="password"><br>
        <input type="submit" value="Login">
    </form>
</body>
</html>
```

### Input Field Attributes

There are different attributes of input field as shown in below table

| Attribute | Parameters |
| --- | --- |
| name | any name |
| value | any value |
| size | pixels |
| maxlength | number |
| row | number |
| cols | number |
| readonly | true,fasle |
| disabled | disabled |
| checked | checked |
| multiple | true, false |

example:

```python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Form Input Fields</title>
</head>
<body>
    <form>
        <label>User Name:</label><br/>
        <input type="text" name="user_name" value="Enter your name" size="6px" maxlength="10" readonly="true"><br/>
        <label >Password:</label><br>
        <input type="password" name="user_name" value="Enter your password"><br>
        <input type="submit" value="Login" name="submit" disabled="disabled">
    </form>
</body>
</html>
```

### How to create a text area inside a form

```python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Registeration Form</title>
</head>
<body>
    <form>
        <label>User Name:</label><br/>
        <input type="text" name="user_name" value="Enter your name" size="6px" maxlength="10"><br/>
        <label >Password:</label><br>
        <input type="password" name="user_name" value="Enter your password"><br>
        <label for="address">Address:</label><br>
        <textarea rows="5" cols="25" name="address" id="addr"></textarea><br>
        <input type="submit" value="Login" name="submit" >
    </form>
</body>
</html>
```

### How to create a combobox in html

```python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Registeration Form</title>
</head>
<body>
    <form>
        <label>User Name:</label><br/>
        <input type="text" name="user_name" value="Enter your name" size="6px" maxlength="10"><br/>
        <label >Password:</label><br>
        <input type="password" name="user_name" value="Enter your password"><br>
        <label for="courses">Courses</label>
        <select>
            <option>Select any item</option>
            <option value="html5">HTML5</option>
            <option value="CSs">CSS</option>
            <option value="JS">JavaScript</option>
            <option value="React">React</option>
        </select>
        <label for="address">Address:</label><br>
        <textarea rows="5" cols="25" name="address" id="addr"></textarea><br>
        <input type="submit" value="Login" name="submit" >
    </form>
</body>
</html>
```

### How to create a listbox

```python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Registeration Form</title>
</head>
<body>
    <form>
        <label>User Name:</label><br/>
        <input type="text" name="user_name" value="Enter your name" size="6px" maxlength="10"><br/>
        <label >Password:</label><br>
        <input type="password" name="user_name" value="Enter your password"><br>
        <label for="courses">Courses</label>
        <select>
            <option>Select any item</option>
            <option value="html5">HTML5</option>
            <option value="CSs">CSS</option>
            <option value="JS">JavaScript</option>
            <option value="React">React</option>
        </select><br>
        <label for="hobbeies">Hobbies</label>
        <select multiple="multiple">
            <option>Select any option</option>
            <option>Reading</option>
            <option>Writing</option>
            <option>Singing</option>
            <option>Playing Cricket</option>
        </select>
        <label for="address">Address:</label><br>
        <textarea rows="5" cols="25" name="address" id="addr"></textarea><br>
        <input type="submit" value="Login" name="submit" >
    </form>
</body>
</html>
```

### How to create a radio button

```python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Registeration Form</title>
</head>
<body>
    <form>
        <label>User Name:</label><br/>
        <input type="text" name="user_name" value="Enter your name" size="6px" maxlength="10"><br/>
        <label >Password:</label><br>
        <input type="password" name="user_name" value="Enter your password"><br>
        <label for="courses">Courses</label>
        <select>
            <option>Select any item</option>
            <option value="html5">HTML5</option>
            <option value="CSs">CSS</option>
            <option value="JS">JavaScript</option>
            <option value="React">React</option>
        </select><br>
        <label for="hobbeies">Hobbies</label>
        <select multiple="multiple">
            <option>Select any option</option>
            <option>Reading</option>
            <option>Writing</option>
            <option>Singing</option>
            <option>Playing Cricket</option>
        </select><br>
        <label for="gender">Gender:</label>
        <input type="radio" name="gender" value="M">Male
        <input type="radio" name="gender" value="F">Female<br>
        <label for="address">Address:</label><br>
        <textarea rows="5" cols="25" name="address" id="addr"></textarea><br>
        <input type="submit" value="Login" name="submit" >
    </form>
</body>
</html>
```

### How to create Checkbox

```python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Registeration Form</title>
</head>
<body>
    <form>
        <label>User Name:</label><br/>
        <input type="text" name="user_name" value="Enter your name" size="6px" maxlength="10"><br/>
        <label >Password:</label><br>
        <input type="password" name="user_name" value="Enter your password"><br>
        <label for="courses">Courses</label>
        <select>
            <option>Select any item</option>
            <option value="html5">HTML5</option>
            <option value="CSs">CSS</option>
            <option value="JS">JavaScript</option>
            <option value="React">React</option>
        </select><br>
        <label for="hobbeies">Hobbies</label>
        <select multiple="multiple">
            <option>Select any option</option>
            <option>Reading</option>
            <option>Writing</option>
            <option>Singing</option>
            <option>Playing Cricket</option>
        </select><br>
        <label for="gender">Gender:</label>
        <input type="radio" name="gender" value="M">Male
        <input type="radio" name="gender" value="F">Female<br>
        <label for="browser">Your favourite web browser:</label><br>
        <input type="checkbox" name="browser" value="chrome">Google chrome
        <input type="checkbox" name="browser" value="Edge">MS Edge
        <input type="checkbox" name="browser" value="Safari">Safari
        <input type="checkbox" name="browser" value="Mozilla">FireFox<br>

        <label for="address">Address:</label><br>
        <textarea rows="5" cols="25" name="address" id="addr"></textarea><br>
        <input type="submit" value="Login" name="submit" >
    </form>
</body>
</html>
```

How to create Fieldset ?

Fieldset is defined as a group of form elements as being logically related.

The browser draws a box around the set of fields to indicate that they are related.

It is a paired tag.

Syntax:

```html
<fieldset>............</fieldset>
```

example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>FieldSet</title>
</head>
<body>
    <p>What is your Web browser?</p>
    <form>
        <fieldset>
            <input type="radio" name="browser" value="Edge">Microsoft Edge |
            <input type="checkbox" name="browser"> Google Chrome.
        </fieldset>
    </form>
</body>
</html>
```

What is legend in HTML5?

<legend> is a tag used with fieldset to give a title to each set of fields. It is a paired tag.

It is used inside the <fieldset> tag

Syntax: 

```html
<fieldset>
	<legend>........</legend>
</fieldset>
```

example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>FieldSet</title>
</head>
<body>
    <p>What is your Web browser?</p>
    <form>
        <fieldset>
            <legend>Favourite Web Browser</legend>
            <input type="radio" name="browser" value="Edge">Microsoft Edge |
            <input type="checkbox" name="browser"> Google Chrome.
        </fieldset>
    </form>
</body>
</html>
```

### HTTP:

HTTP is a protocol(set of rules), it is designed to enable communications between clients and server.

![Http-protocol.png](Introduction%202d4f3e764daa41c0a7b8ff7133d463f5/Http-protocol.png)

HTTP provides following two methods to access the data  from the server 

1. get method.
2. post method

1. get method: 

In this method we don’t have security for our data and only limited data can be sent to the server page. 

It is carries the raw data between client-server. It is used to send the data from the client to the server through the url. 

This is the default method of form.

Syntax:

```html
<form action='action.html' method="get">

</form>
```

example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>FieldSet</title>
</head>
<body>
    <p>What is your Web browser?</p>
    <form>
        <fieldset>
            <legend>Favourite Web Browser</legend>
            <input type="radio" name="browser" value="Edge">Microsoft Edge |
            <input type="checkbox" name="browser"> Google Chrome.
        </fieldset>
    </form>
</body>
</html>
```

→Get method satisfies following points:

1. Get method request can be catched through the url.
2. Get request remains in the browser.
3. Get request can be bookmarked.
4. Get request should never be used when dealing sensitive data.
5. Get request have some length restrictions.

**action attribute:**

This attribute is used to specify the url of the server page to which we want to sent our data..

Syntax:

```html
<form name='myForm' action='action.html' >
</form>
```

1. Post method:

In Post method we have security for our data and we can send bulk of data as well to the server page. It transfers encrypted data from client to the server.

Syntax:

```html
<form action="action.html" method="POST">
<form>
```

Example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>HTTP GET Form</title>
</head>
<body>
    <h1>HTTP POST method Form</h1>
    <form action="action.html" method="post">
        <input type="text" name="user">
        <br/>
        <input type="password" name="psw">
        <br/>
        <input type="submit" value="sign-in">
    </form>
</body>
</html>
```

**Working with Advanced Forms:**

HTML5 supports the following advanced form control, these are latest input types in web 2.0.

```html
1. color ( color chooser)
2. date  (popup calender)
3. datetime ( datetime chosser)
4. datetime-local (datetime chooser)
5. email (email entry)
6. month (month chooser)
7. number (spinner)
8. range (slider)
9. search (search query input)
10. tel ( telephone input)
11. time (time selector)
12. url (URL entry)
13. week (week chooser)
```

Note: All major browser supports all the new input types. If they are not supported, will behave as regular text input.

### Date Pickers

The different date picker elements are:

1. date
2. datetime
3. datetime-local
4. month
5. time
6. week
1. input type date: It allows the user to select date in real time applications.

It is very usefull for ticket booking or taking appointments, ordering food items etc.

Syntax: 

```html
<input type='date-picker-element'>
```

example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Modern Form</title>
</head>
<body>
    <h1>Modern Form</h1>
    <form action="action.html" name="myForm" id="form">
        <label for="dt" style="color: blue;">Select valid Date..</label>
        <input type="date" name="dt"><br>
        <input type="submit" value="next page" />
    </form>
</body>
</html>
```

1. datetime: This input type allows the user to select date and time with time zone.

syntax:

```html
<input type="datetime" />
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Modern Form</title>
</head>
<body>
    <h1>Modern Form</h1>
    <form action="action.html" name="myForm" id="form">
        <label for="dt" style="color: blue;">Select valid Date..</label>
        <input type="date" name="dt"><br>
        <!-- date time -->
        <h2>Date with time </h2>
        <label style="color: green;">Select date & time</label>
        <input type="datetime-local"><br>
        <input type="submit" value="next page" />
    </form>
</body>
</html>
```

**General Form Controls:**

1. color
2. email
3. number
4. range
5. search
6. tel
7. url

1. Color:

This input type allows the user to display color picker.

syntax:

```jsx
<input type="color" >
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Fron submitted</title>
</head>
<body>
    <h1>Form data submitted.</h1>
</body>
</html>
```

1. email: This input type allows user to enter valid email address.

syntax: 

```jsx
<input type="email" name="email">
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Form Controls</title>
</head>
<body>
    <form action="control.html" name="myForm">
        <label for="email" style="color: blue;">Enter email:</label><br>
        <input type="email" name="email" placeholder="Enter your email"><br>
        <label for="clr" style="color: blue;">Select any color:</label><br>
        <input type="color" name="clr"><br>
        <input type="submit" name="submit" value="Next Page">
    </form>
</body>
</html>
```

1. Number:

This input type allows to display numerical spinners.

Syntax:

```jsx
<input type="number" name="number">
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Form Controls</title>
</head>
<body>
    <form action="control.html" name="myForm">
        <label for="email" style="color: blue;">Enter email:</label><br>
        <input type="email" name="email" placeholder="Enter your email"><br>
        <label for="number" style="color: blue;">Select any number:</label>
        <input type="number" name="number" value="0" min="5" max="100" step="5"><br>
        <label for="clr" style="color: blue;">Select any color:</label><br>
        <input type="color" name="clr"><br>
        <input type="submit" name="submit" value="Next Page">
    </form>
</body>
</html>
```

Attributes of number input type:

| Attribute | value |
| --- | --- |
| max | specifies the maximum value allowed |
| min | specifies the minimum value allowed |
| step | specifies the legal number intervals. |
| value | specifies the default value. |
1. range: This input type allows the user to display slider .

syntax:

```jsx
<input type="range" max="maximum-value-allowed" min="minimum-value-allowed" 
step="legal-number-intervals" value="default-value">
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Form Controls</title>
</head>
<body>
    <form action="control.html" name="myForm">
        <label for="email" style="color: blue;">Enter email:</label><br>
        <input type="email" name="email" placeholder="Enter your email"><br>
        <label for="number" style="color: blue;">Select any number:</label>
        <input type="number" name="number" value="0" min="5" max="100" step="5"><br>
        <label for="clr" style="color: blue;">Select any color:</label><br>
        <label for="range" style="color: blue;">mark yourself:</label>
        <input type="range" max="100" min="5" step="2" value="0" name="range"><br>
        <input type="color" name="clr"><br>
        <input type="submit" name="submit" value="Next Page">
    </form>
</body>
</html>
```

1. search: In HTML we can define textbox as search box instead of a normal textbox.

syntax:

```jsx
<input type="search" name="search-bar">
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Form Controls</title>
</head>
<body>
    <form action="control.html" name="myForm">
        <label for="email" style="color: blue;">Enter email:</label><br>
        <input type="email" name="email" placeholder="Enter your email"><br>
        <label for="number" style="color: blue;">Select any number:</label>
        <input type="number" name="number" value="0" min="5" max="100" step="5"><br>
        <label for="clr" style="color: blue;">Select any color:</label><br>
        <label for="range" style="color: blue;">mark yourself:</label>
        <input type="range" max="100" min="5" step="2" value="0" name="range"><br>
        <label for="search-bar" style="color: blue;">Search Here></label>
        <input type="search" name="search-bar"><br>
        <input type="color" name="clr"><br>
        <input type="submit" name="submit" value="Next Page">
    </form>
</body>
</html>
```

1. tel: This input type accepts only phone numbers it doesn’t confirms any specific pattern.

```jsx
<input type="tel" name="tel-num">
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Form Controls</title>
</head>
<body>
    <form action="control.html" name="myForm">
        <label for="email" style="color: blue;">Enter email:</label><br>
        <input type="email" name="email" placeholder="Enter your email"><br>
        <label for="number" style="color: blue;">Select any number:</label>
        <input type="number" name="number" value="0" min="5" max="100" step="5"><br>
        <label for="clr" style="color: blue;">Select any color:</label><br>
        <label for="range" style="color: blue;">mark yourself:</label>
        <input type="range" max="100" min="5" step="2" value="0" name="range"><br>
        <label for="tel-num">Enter Telephone:</label>
        <input type="tel" name="tel-num" ><br>
        <label for="search-bar" style="color: blue;">Search Here></label>
        <input type="search" name="search-bar"><br>

        <input type="color" name="clr"><br>
        <input type="submit" name="submit" value="Next Page">
    </form>
</body>
</html>
```

1. url: IT is used to validate url address. It is very usefull for mobile applications.

Syntax:

```jsx
<input type="url" name="url">
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Form Controls</title>
</head>
<body>
    <form action="control.html" name="myForm">
        <label for="email" style="color: blue;">Enter email:</label><br>
        <input type="email" name="email" placeholder="Enter your email"><br>
        <label for="number" style="color: blue;">Select any number:</label>
        <input type="number" name="number" value="0" min="5" max="100" step="5"><br>
        <label for="clr" style="color: blue;">Select any color:</label><br>
        <label for="range" style="color: blue;">mark yourself:</label>
        <input type="range" max="100" min="5" step="2" value="0" name="range"><br>
        <label for="tel-num">Enter Telephone:</label>
        <input type="tel" name="tel-num" ><br>
        <label for="search-bar" style="color: blue;">Search Here></label>
        <input type="search" name="search-bar"><br>
        <label for="url" style="color: blue;">Enter the website: </label>
        <input type="url" name="url">

        <input type="color" name="clr"><br>
        <input type="submit" name="submit" value="Next Page">
    </form>
</body>
</html>
```

**HTML5 form attributes:**

The below is the list of new form attributes introduced in HTML5

1. autocomplete
2. novalidate

1. autocomplete: It specifies whether a form or input field should have autocomplete on or off. When autocomplete is on the browser automatically completes values based on values that the users have entered before.

Note: By default autocomplete is on

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>HTML5 new Attributes</title>
</head>
<body>
    <form action="demo.html" autocomplete="off">
        First Name: <br>
        <input type="text" name="fname" /><br>
        Email: <br>
        <input type="email" name="email"><br>
        <input type="submit" name="submit" value="submit">
    </form>
</body>
</html>
```

1. novalidate: IT is a boolean attribute. When present, specifies that the form data(input) should not be validated when submitted.

syntax:

```jsx
<form novalidate="novalidate">
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>HTML5 new Attributes</title>
</head>
<body>
    <form action="demo.html" autocomplete="off" novalidate="novalidate">
        First Name: <br>
        <input type="text" name="fname" /><br>
        Email: <br>
        <input type="email" name="email" required="required"><br>
        <input type="submit" name="submit" value="submit">
    </form>
</body>
</html>
```

**HTML5 Input attributes:**

In HTML5 input contains the following list of new attributes:

1. placeholder(Text fields with temporary entry).
2. autofocus.
3. required(textfield with required values [non empty])
4. autocomplete
5. form
6. form action
7. from enctype
8. form method
9. form novalidate
10. form target
11. height and width
12. list
13. min and max
14. multiple
15. pattern
16. step
17. spellcheck
18. contenteditable
19. accesskey

Task : create a form by using the above attributes .

**HTML5 new form elements:**

Some of the new elements supported by the HTML5 are :

1. <datalist>
2. <keygen>
3. <output>

1. <datalist>: It is used to list a set of data to be used in a list of options like autocomplete feature used in forms. It enables us to provide a list of predefined options to the users as they input data. It is a paired tag.

syntax: 

```jsx
<datalist>.............</datalist>
```

attribute:

| attribute | value |
| --- | --- |
| data | specifies a xml file that can be used to prefill the data list |
|  |  |

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>HTML5 new Attributes</title>
</head>
<body>
    <h3>Enter your favourite color:</h3><br>
    <input type="text" name="favcolor" list="colors">
    <datalist id="colors">
        <option value="Green">
        <option value="blue">
        <option value="maroon">
    </datalist>
</body>
</html>
```

1. <keygen>: This element generates the keys to authenticate users. The purpose of the <keygen> element is to provide a secure way to authenticate user. The keygen tag is used as key generator for a form. The private key is stored in browser and public key is sent to the server, when the form is click or submitted. IT is a non paired tag.

syntax:

```jsx
<keygen />
```

Attributes:

| attrbutes  | values | Description |
| --- | --- | --- |
| autofocus | autofocus | <keygen> element should automatically get focus when the page loads. |
| challenge | challenge | <keygen> should be challenged when page is submitted. |
| disabled | disabled | specifies that a <keygen> element should be disabled. |
| name | name | defines the name for the <keygen> element. |

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>HTML5 new Attributes</title>
</head>
<body>
    <h3>Enter your favourite color:</h3><br>
    <input type="text" name="favcolor" list="colors">
    <datalist id="colors">
        <option value="Green">
        <option value="blue">
        <option value="maroon">
    </datalist><br>
    <hr>
    <form action="demo.html">
        <h2>Keygen element example:</h2>
        Encryption key: <br>
        <keygen name="encrypt" challenge="challenge"><br>
        <input type="submit" value="generate">
    </form>
</body>
</html>
```

1. <output>:

IT is used to display the result of arithmetical calculation, It is a paired tag.

syntax: 

```jsx
<output>...............</output>
```

Attributes:

| attribute name | value | description |
| --- | --- | --- |
| for | element-id | specifies the relation between the result of the calculation. |
| form | form_id | specifies one or more forms the output belongs to |
| name | name | specifies the name for the output element |
| range | range slider  | number + your range  |

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>HTML5 new Elements</title>
</head>
<body>
    <h3>Enter your favourite color:</h3><br>
    <input type="text" name="favcolor" list="colors">
    <datalist id="colors">
        <option value="Green">
        <option value="blue">
        <option value="maroon">
    </datalist><br>
    <hr>
    <form action="demo.html">
        <h2>Keygen element example:</h2>
        Encryption key: <br>
        <keygen name="encrypt" challenge="challenge"><br>
        <input type="submit" value="generate">
    </form>
    <hr>
    <h3>output element</h3>
    <form action="demo.html" oninput="x.value=parseInt(a.value) + parseInt(b.value)">
    Range:
    <input type="range" name="a" value="50">number + <input type="number" name="b" value="50" >=
    <output name="x" for ="a b"></output>
    </form>
</body>
</html>
```

**parseInt() global function**:

The parseInt() function  parses the string and returns an Integer:

Syntax: 

```jsx
parseInt(string)
```

note: the parementer of the pareInt should be a string.

**Working with HTML5 multimedia:**

Multimedia comes in many different formats in web environment, modern webpages having pictures, music, sound, videos, records, films, animations etc.

**Multimedia video formats:**

The  following video formats are frequently used in web environments:

1. AVI(.avi) → (Audio Video Interleave) was developed by microsoft.
2. WMV(.wmv) → (windows media video) was developed by microsoft.
3. MPEG(.mpg or .mpeg) → (Moving picture expert group) 
4. Flash (.swf or .flv) → It was developed by the micromedia.
5. MP4(.mp4, .mpeg-4) → It is latest format for internet.

**Multimedia audio formats:**

The following audio formats are frequently used in web environments.

1. MIDI(.mid or .midi) → Music Instrument digital Interface.
2. MP3(.mp3)→ MP3 files are actually the sound part of the MPEG file.
3. wav(.wav)→ WAVE(more known as WAV) was developed by microsoft and IBM.
4. WMA(.wma)→ Window Media Audio.
5. ogg(.ogg) →

**HTML audio tag:**

IT is used to specify audio on an HTML document. It enables audio playback without plugins, The audio can be controlled with native or customized controls.

Audio files can be prefetched or downloaded on demand. 

It is a paired tag.

syntax:

```jsx
<audio>.....</audio>
```

Note: Any text between <audio>...</audio> will be displayed in browsers that do not support audio.

Attributes:

| attribute | value | description |
| --- | --- | --- |
| autoplay | autoplay | specifies that the audio will start playing |
| controls | controls | specifies that the audio controls should be displayed |
| 100p | 100p | specifies that the audio will start over again. |
| src | path of audio | specifies that the audio will start over again. |
| muted | muted | specifies that the audio will be muted |

example:

```jsx
**<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Multimedia</title>
</head>
<body>
    <audio src="https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_700KB.mp3" controls="controls" 100p="3" autoplay="autoplay">oops!! your broswer doesn't support audio</audio>
</body>
</html>**
```

**HTML5 audio Tag with JS controls**

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Multimedia JS controls.</title>
</head>
<body>
    <h2 style="color: blue;">HTML5 audio tag with JS Controls:</h2>
    <audio src="https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_700KB.mp3" id="myAudio">audo is not supported by your browser</audio>
    <div>
        <button onclick="document.getElementById('myAudio').play()">Play Audio</button>
        <button onclick="document.getElementById('myAudio').pause()">Pause Audio</button>
        <button onclick="document.getElementById('myAudio').volume+=0.1">increase volume</button>
        <button onclick="document.getElementById('myAudio').volume-=0.1">increase volume</button>
    </div>
</body>
</html>
```

**HTML video tag:**

IT is used to specify video on HTML document. It is a paired tag.

syntax: 

```jsx
<video>...</video>
```

Note: any text between the <video>..</video> tags will be displayed in browsers that do not support the video.

Attributes:

| attribute | value | Description |
| --- | --- | --- |
| autoplay | autoplay | specifies that the video will start playing |
| controls | controls | specifies that the video controls should be displayed |
| src | url path | specifies the url of the video file |
| width | pixels | sets the width of the video file |
| height | pixels | sets the height of the video file |
| loop | loop | specifies that the video will start again |
| muted | muted | specifies the audio output of the video should be muted. |
| poster | url | specifies an image to be shown while the video is downloading or until the user hits the play button. |
| preload | auto, metadata, none | specifies it and how author thinks the video should be loaded when the page loads |

example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Multimedia Video Elemenet.</title>
</head>
<body>
    <video src="sample_video.mp4" controls="controls" autoplay="autoplay" loop="2" width="500px" poster="data:image/jpeg;base64,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" preload="auto"><p style="color:red">oops your browser not supporting video update and try later.</p></video>
</body>
</html>
```

**Video Element with JS controls:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Multimedia Video JS controls.</title>
</head>
<body>
    <h2 style="color: blue;">HTML5 video tag with JS Controls:</h2>
    <video src="sample_video.mp4" id="myVideo" width="700px">video is not supported by your browser</video>
    <div>
        <button onclick="document.getElementById('myVideo').play()">Play Audio</button>
        <button onclick="document.getElementById('myVideo').pause()">Pause Audio</button>
        <button onclick="document.getElementById('myVideo').volume+=0.1">increase volume</button>
        <button onclick="document.getElementById('myVideo').volume-=0.1">decrease volume</button>
    </div>
</body>
</html>
```

**HTML5 track Element:**

It specifies text tracks for media elements. 

This element is used to specify subtitles, caption files or other files containing text that should be visible when the media is playing. 

It is a non paired tag.

syntax:

```html
<track src="" />
```

Note: It is not supported by any of the major browsers.

WebVTT: It is a format for displaying timed text tracks with the <track> element.

The primary purpose of WebVTT files is to add subtitles to a <video> .

WebTT is a text based format. 

A WebTT file must be encoded in UTF-8 format.

HOW to create WebVTT file?

1.) open any text editor.

2.) enter the below text inside it

```html
1] 00:00:00:500 -> 00:00:002.000
The web is always changing
2] 00:00:02.500 -> 00:00:04.300
the way we access it is changing
```

3.) save the file with .vtt extension at any location

example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Track Elemenet.</title>
</head>
<body>
    <video src="sample_video.mp4" controls="controls" autoplay="autoplay" loop="2" width="500px" poster="data:image/jpeg;base64,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" preload="auto">
        <track src="web.vtt" kind="subtitles" srclang="en" label="English" />
        <p style="color:red">oops your browser not supporting video update and try later.</p>
    </video>
</body>
</html>
```