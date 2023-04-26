# CSS [ Cascading Style Sheet]

CSS is a simple design  language to make our web pages more presentable.

Let’s try to understand each of the CSS

Cascading: IT represents inherit.

Style: This represents attributes and properties.

Sheets: IT represents the .css files.

Some of the important features of CSS are:

1. Easy to manage.
2. Global change.
3. saves a lot of time
4. Inline style sheets
5. Internal style sheets
6. External style sheets
7. good performance
8. Multi device compatibility.
9. Global web standards

Why CSS?

CSS is required because of the following reasons:

1. It is collection of style sheet mechanism.
2. IT is used to add more effect’s in the HTML elements.
3. We can embed css in html, javaScript, php, ASP etc
4. Use same style on multiple pages.

CSS versioning

```jsx
1. CSS 1.0  [1996]
2. CSS 2.0  [1998]
3. CSS 3.0  [2014]
```

CSS Syntax structure

As per W3C standard CSS has the following  structure

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS structure</title>
    <style>
        selector{
            propertyName1 : "value",
            propertyName2 : "value"
        }
    </style>
</head>
<body>
    <!-- body goes here -->
</body>
</html>
```

For example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Internal CSS</title>
    <style>
        div{
            background-color: #FFFFF0;
            text-decoration: underline;
            font-family: Arial, Helvetica, sans-serif;
        }
    </style>
</head>
<body>
    <div>Welcome to cascading style sheet... !</div>
    <div>Welcome to HTML with CSS course.</div>
</body>
</html>
```

CSS comments:

→ Comments are non executable statements/non ignore statements.

→ Using these comment notations we can declare customized statements or user defined statements in the web environment or in the style sheet .

→ In CSS every comment begins with “/*” and ends with “*/”.`

Example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Internal CSS</title>
    <style>
        div{
            /* setting the background color for better look. */
            background-color: #FFFFF0;
            text-decoration: underline;
            font-family: Arial, Helvetica, sans-serif;
        }
    </style>
</head>
<body>
    <div>Welcome to cascading style sheet... !</div>
    <div>Welcome to HTML with CSS course.</div>
</body>
</html>
```

CSS Basic Syntax in Detail:
The basic syntax of CSS is made up of three parts

1. selector.
2. property
3. value.

![CSS-SYNTAX.png](CSS%20%5B%20Cascading%20Style%20Sheet%5D%206c50436f28714828b8d38e9d0762d1bd/CSS-SYNTAX.png)

Types of stylesheets:

In CSS stylesheets are classified into the following three types:

1. Inline Style CSS.
2. Internal | embeded style sheet.
3. External style CSS

1. **Inline Style CSS:**

If we specify styles inside the tag in the body part of html page, then it is known as inline style CSS.

These styles are able to apply CSS only for that particular line.

 

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Inline CSS</title>
</head>
<body>
    <div style="color:red">Welcome to cascading style sheet... !</div>
    <div style="color: blue; background-color: lightgreen;">Welcome to HTML with CSS course.</div>
</body>
</html>
```

1. Internal Style Sheets: 

These are popularly knows as embeded style sheet also.

If we specify the styles in our html file itself then they are called internal styles.

These styles cannot be used in other files. 

Syntax:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Internal CSS</title>
    <style>
        /* Your styles code goes here */
    </style>
</head>
<body>
    <!-- Your body goes here -->
</body>
</html>
```

Example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Internal CSS</title>
    <style>
        div{
            /* setting the background color for better look. */
            background-color: #FFFFF0;
            text-decoration: underline;
            font-family: Arial, Helvetica, sans-serif;
        }
    </style>
</head>
<body>
    <div>Welcome to cascading style sheet... !</div>
    <div>Welcome to HTML with CSS course.</div>
</body>
</html>
```

1. External Style Sheets:

If we declare the styles outside of our html file in a separate file with .css extension, then they are called as external stylesheets.

These styles can be reusable on more than one html file.

Syntax:

In html we need to include the external stylesheet defined by use by using the below syntax:

```jsx
<html>
	<head>
		<title>External CSS Use</title>
		<link rel="stylesheet" href="styles.css" >
	</head>
	<body>
	</body>
</html>
```

How to implement external styles sheet

Follow the below steps to apply the external style sheets.

1. create a styles.css file [here name of the file can be anything, we need to only ensure that it should have .css extension]

styles.css

```jsx
div{
    color: #FFFFF0;
    font-size: 25px;
    text-decoration: underline;
    font-weight: bold;
}
```

1. Create a html page  ie external-css.html which is using the styles.css file

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>External CSS</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div>Welcome to the External CSS.</div>
</body>
</html>
```

Working with css selectors:

selectors means styles reusability. In CSS there are different types of selectors as listed below:

1. Tag/element selector/Type selector
2. ID selector
3. class selector
4. grouping selector
5. Universal selector
6. Descendent selector
7. Customized selector

1. Tag selector/element selector:

These are popularly known as type selectors it matches every instances of the element type in the document tree.

syntax:

```jsx
tagName{
	css propertie1: value;
	css property2: value;
	css prperty3: value;	
}
```

Example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS selectors</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        h1{
            color: #ad8fff;
            background-color: cornsilk;
        }
    </style>
</head>
<body>
    <h1>Those are different types of CSS selectors</h1>
    <div>
        <ul>
            <li>Tag selector</li>
            <li>ID selector</li>
            <li>Class selector</li>
            <li>Group selector</li>
            <li>Desendent selector</li>
        </ul>
    </div>
    <h1>Note: We can apply CSS using internal , external or inline CSS.</h1>
</body>
</html>
```

1. ID selectors:

It is used to specify styles for a single, unique element.

the id selectors uses the id attribute of the html element, and is defined with a “#”.

Syntax:

```jsx
#id-attribute-name{
 property1:value;
 property2: vlaue;
}

or 
tagName#id-attribute-name{
	 property1:value;
	 property2: vlaue;
}
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS selectors</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        h1{
            color: #ad8fff;
            background-color: cornsilk;
        }
        h1#note{
            background-color: cyan;
        }
    </style>
</head>
<body>
    <h1>Those are different types of CSS selectors</h1>
    <div>
        <ul>
            <li>Tag selector</li>
            <li>ID selector</li>
            <li>Class selector</li>
            <li>Group selector</li>
            <li>Desendent selector</li>
        </ul>
    </div>
    <h1 id="note">Note: We can apply CSS using internal , external or inline CSS.</h1>
</body>
</html>
```

1. Grouping selectors:

We can group selectors using comma sepearator

example:

```jsx
h1{
	same_property:same_value
}
h2{
	same_property:same_value
}
h3{
	same_property:same_value
}

or
h1,h2,h3{
	same_property:same_value
}

```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS selectors</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        h1{
            color: #ad8fff;
            background-color: cornsilk;
        }
        h1#note, p{
            background-color: cyan;
        }
    </style>
</head>
<body>
    <h1>Those are different types of CSS selectors</h1>
    <div>
        <ul>
            <li>Tag selector</li>
            <li>ID selector</li>
            <li>Class selector</li>
            <li>Group selector</li>
            <li>Desendent selector</li>
        </ul>
    </div>
    
    <h1 id="note">Note: We can apply CSS using internal , external or inline CSS.</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequatur culpa pariatur, eum quaerat delectus maxime aspernatur et exercitationem totam sunt. Alias illum optio porro iste ab. Sunt nobis libero debitis?</p>
</body>
</html>
```

1. class selectors

It is used to select a style for a group of elements with the same class attribute value.

The class selector uses the HTML class attribute, and defined with a “.” (period) in css.

syntax:

```jsx
.className{
	property: value;
	property2: vlaue;
}

```

example:

class-selector.html

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Class selector</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="div">
        <h1>HTML & CSS</h1>
        <h2>Why HTML is important</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis eligendi est, minus sunt laudantium odit dolorem
            incidunt, in ut placeat voluptate atque consequuntur eveniet animi fuga illum quaerat iure nemo?</p>
        <h2>Why CSS is important.</h2>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quos qui molestiae eius maiores recusandae voluptates
            voluptatem. Odit suscipit temporibus, a iste accusantium corporis odio, inventore nobis, iusto accusamus dicta
            porro.</p>
    </div>
    <div>
        <h1>Introduction to JavaScript</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt neque dolorem rerum maxime nobis praesentium cum quis modi vel impedit magni fuga iure rem, nam hic exercitationem? At, ea impedit.</p>
        <h2>Features of JavaScript:</h2>
        <ul>
            <li>It is a Scripting Language.</li>
            <li>It is object based language.</li>
            <li>IT is signle threaded.</li>
            <li>It supports multiparadigm concepts.</li>
        </ul>
    </div>
</body>
</html>
```

styles.css

```jsx
.div{
    color: blue;
    font-size: 20px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
```

ID and class selector grouping

On the same html page

styles.css

```jsx
.div{
    color: blue;
    font-size: 20px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

/* Id and class grouping */
div.div, #first-para{
    background-color: cornsilk;
}
```

**Class selector with javascript**

On the same html page as specified above we will be writting some javascript.

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Class selector</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="div">
        <h1>HTML & CSS</h1>
        <h2>Why HTML is important</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis eligendi est, minus sunt laudantium odit dolorem
            incidunt, in ut placeat voluptate atque consequuntur eveniet animi fuga illum quaerat iure nemo?</p>
        <h2>Why CSS is important.</h2>
        <p >Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quos qui molestiae eius maiores recusandae voluptates
            voluptatem. Odit suscipit temporibus, a iste accusantium corporis odio, inventore nobis, iusto accusamus dicta
            porro.</p>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Inventore excepturi natus totam vero, odit libero voluptatem molestias ut neque voluptates, enim facere suscipit harum illum quam saepe minima voluptate tempore!</p>
    </div>
    <div>
        <h1>Introduction to JavaScript</h1>
        <p id="first-para">Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt neque dolorem rerum maxime nobis praesentium cum quis modi vel impedit magni fuga iure rem, nam hic exercitationem? At, ea impedit.</p>
        <h2>Features of JavaScript:</h2>
        <ul>
            <li>It is a Scripting Language.</li>
            <li>It is object based language.</li>
            <li>IT is signle threaded.</li>
            <li>It supports multiparadigm concepts.</li>
        </ul>
        <h3>Click on the button to chage the paragraph content.</h3>
        <button onClick="myParaValue()">Change para</button>
    </div>
    <script src="change-element.js"></script>
</body>
</html>
```

styles.css

```jsx
.div{
    color: blue;
    font-size: 20px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

/* Id and class grouping */
div.div, #first-para{
    background-color: cornsilk;
}
```

change-element.js

```jsx
function myParaValue(){
    document.getElementById("first-para").innerHTML = "I am being access by the Javascript";
}
```

Working with CSS units or measurements:

CSS supports a number of measurement including absolute and relative units. Some of the important measurement units are:

1. em
2. ex
3. px
4. in
5. cm
6. mm

1. em: 

It is a unit of measurement in the field of typography. It is developed based on “m”

syntax: 

```jsx
 em;
```

1. ex: It is another measurement developed based on lower case ‘x’.

Syntax:

```jsx
ex;
```

1. px : It defines a measurement in screen pixels.

Syntax:

```jsx
px;

```

1. in: It defines a measurement in inchess.

Syntax:

```jsx
in;
```

1. cm: it defines a measurement in centimeters.

Syntax:

```jsx
cm;
```

1. pt: It defines a measurement in points

```jsx
pt
```

1. pc: It defines measurement in picas.

Syntax:

```jsx
pc;
```

1. % : It defines measurement in Percentage of its parent element.

```jsx
%
```

Task: create a webpage making use of all different types of measurement units.

**CSS Background property:**

CSS supports the following list of background properties:

1. background-color:
2. background-image
3. background-repeat
4. background-attachement
5. background-position.

1. background-color:

It is used to set the background color of an element.

Syntax:

```jsx
css-selectory{
	background-color: colorName/color code /Hexa code;
	or
	background: colorName/color code / Hexa code;
}
```

example:

background.html

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS Background Properties</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div>Working with CSS background Properties.</div>
</body>
</html>
```

style.css

```jsx
div{
    background-color: blanchedalmond;
}
```

1. Background-image: IT is used to set the background image of an element.

syntax:

```jsx
css-selector{
	background-image:url('imagepath')
	or
	background:url('imagepath')
```

example:

background.html

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS Background Properties</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div>Working with CSS background Properties.</div>
    <div class="content">
        <h1>Different CSS background properties are given below</h1>
        <ul>
            <li>background-color</li>
            <li>background-image</li>
            <li>background-repeat</li>
            <li>background-attachment</li>
            <li>background-position</li>
        </ul>
    </div>
</body>
</html>
```

styles.css

```jsx
div{
    background-color: blanchedalmond;
}

div.content{
    background-image: url('data:image/jpeg;base64,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');
    
}
```

1. background-repeat: It is used to control the repetition of an image in the background.

syntax: 

```jsx
css-selector{
	background-repeat: no-repeat;
	or
	background: no-repeat
}
```

Different background-repeat property values

| values | description |
| --- | --- |
| repeat | The background image will be repeated both vertically and horizontally |
| repeat-x | The background image will be repeated only horizontally. |
| repeat-y | The background image will be repeated only vertically |
| no-repeat | The background image will not be repeated |

example:

background.html

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS Background Properties</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div>Working with CSS background Properties.</div>
    <div class="content">
        <h1>Different CSS background properties are given below</h1>
        <ul>
            <li>background-color</li>
            <li>background-image</li>
            <li>background-repeat</li>
            <li>background-attachment</li>
            <li>background-position</li>
        </ul>
    </div>
</body>
</html>
```

style.css

```jsx
**div{
    background-color: blanchedalmond;
}

div.content{
    background-image: url('data:image/jpeg;base64,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');
    background-repeat: no-repeat;
}**
```

1. background-attachment:

It is used to control scrolling of an image in the background.

sytax:

```jsx
css-selector{
	background-attachment: fixed;
	background: fixed;
}
```

1. background-position:

It is used to control position of an image in the background.

syntax:

```jsx
css-selector{
	background-position: center;
or 
	background: center;
}
```

example:

background.html

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS Background Properties</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div>Working with CSS background Properties.</div>
    <div class="content">
        <h1>Different CSS background properties are given below</h1>
        <ul>
            <li>background-color</li>
            <li>background-image</li>
            <li>background-repeat</li>
            <li>background-attachment</li>
            <li>background-position</li>
        </ul>
    </div>
</body>
</html>
```

style.css

```jsx
div{
    background-color: blanchedalmond;
}

div.content{
    background-image: url('data:image/jpeg;base64,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');
    background-repeat: no-repeat;
    /* background-attachment: fixed; */
    background-position: center;
}
```

**CSS Font Family**

CSS supports following list of font properties:

1. The font-family property which is used to change the face of a font.
2. the font-style property which is used to make a font italic or oblique.
3. The font-varient property which is used to create a small-caps effect.
4. The font-weight property which is used to display bold or light a font appears.
5. The font-size property which is used to increase or decrease the size of a font.

example:

background.html

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS Background Properties</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div>Working with CSS background Properties.</div>
    <div class="content">
        <h1>Different CSS background properties are given below</h1>
        <ul>
            <li>background-color</li>
            <li>background-image</li>
            <li>background-repeat</li>
            <li>background-attachment</li>
            <li>background-position</li>
        </ul>
    </div>
</body>
</html>
```

style.css

```jsx
div{
    background-color: blanchedalmond;
}

div.content{
    background-image: url('data:image/jpeg;base64,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');
    background-repeat: no-repeat;
    /* background-attachment: fixed; */
    background-position: center;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 10px;
    font-style: oblique;
    font-weight: bolder;
    font-variant: small-caps;
}
```

## CSS Text Properties:

CSS supports the following list of text properties:

1. color
2. direction
3. text-decoration
4. text-indent
5. text-align
1. color: By using this property we can change the text color.

syntax:

```jsx
css-selector{
	color:blue;
}
```

Example:

background.html

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS Background Properties</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div>Working with CSS background Properties.</div>
    <div class="content">
        <h1>Different CSS background properties are given below</h1>
        <ul>
            <li>background-color</li>
            <li>background-image</li>
            <li>background-repeat</li>
            <li>background-attachment</li>
            <li>background-position</li>
        </ul>
    </div>
    <div class="text-properties">
        <h1>The different text properties are:</h1>
        <ul>
            <li>color</li>
            <li>direction</li>
            <li>text-decoration</li>
            <li>text-indent</li>
            <li>text-align</li>
        </ul>
    </div>
</body>
</html>
```

style.css

```jsx
div{
    background-color: blanchedalmond;
}

div.content{
    background-image: url('data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxASEhUQEhIVFRUVFRUVFRUVFRUPDxUVFRUWFhUVFRUYHSggGBolGxUVITEhJSkrLi4uFx8zODMtNygtLisBCgoKDg0OFxAQGCsdHR0tLS0tLS0tLS0tLSstLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLTctLS0tN//AABEIAIkBbwMBIgACEQEDEQH/xAAbAAACAwEBAQAAAAAAAAAAAAABAgADBAUGB//EADUQAAIBAgQDBQYGAwEBAAAAAAABAgMRBBIhUQUxQRNhkaHRFVJTcZLwFCJigaKxBkLB8TL/xAAYAQEBAQEBAAAAAAAAAAAAAAABAAIDBP/EAB0RAQEBAAIDAQEAAAAAAAAAAAABEQISAyFREzH/2gAMAwEAAhEDEQA/APeEFTJmMOA3IK2C5YzqwiFTIR0xAXISEhAXJGuFihUgSBRGwXJCG4rZCRrkTAiXIrVK4WUpjZyw6suC4tyXLFprguAhDRIRAuSCTBckmLcQYhTWxEYq8nbn5anOxXG4K6irvTX/AF5JmpxtZvKR1pSSMOK4nThfW7tdW116HBxfEKk3e9l0S5cjHmOk8f1i+T462J41NpqKsuj/ANuZzHN9WJfw6ga7zpJI522mzWBnBIqchCzOK5lbYDQPnA5CoiRIbkGUQ2XVlpwpLjW5EWXXuDsspQhco6Lcb8pdllezuS4gLnkx6dPcIqYSRkxrlVwqRYjphTEuC5YmhPQViJkzBhtMTMJcFxZ1cpBsVRkNKdgw79NcFxe0Jcka5LiSkS5DTtkuKmV1cRCLtKUU+9pEl6kPmOFiuPU451F3aX5dLpvk/A5WL/yOq3+Rpfsnp6m547R3exnNJXbst3ojPW4hSje8lyv/AF6nhK/Eakr5pN3te/crIzus9zpPDR3e3nx+kt/u3r5FNT/IY6Wi+burrZ28/wCjxqqvfoFVmP4jtXpqvH5ySSVn1fcUy45UaVna23W29zgRq89QdqP5ja6VXE5m3J3feLKsjmuqI6jNdKzjpfievcKsTsc/P0LVF/fePWFplXfPvGVUpnDkriRmtQyJpdS/33EzIp7TT753FdQDi5yV7BVRGepVSu/vkJGvoR6tiqpq5IT6vYyRraEqTul4B7XVq7QkpK1jI6qadvvcLqpW2swPVpzdNv8AwVz1t3IxvEX1+XnzDKprz5p/0WLGqVX+v7B2uulnboc6nVbb+bXkVqvb5j1OPb4TiEo6PVeaOjQxkJ6J2ez0PPpjRY3hK5znY9GwpnJo8QktHry+fedCjWjLWL/bkzleNn9anKVeQXMEy0a5GIwXJadSHKbhz259QxafMRsw1+I0431u+71MlXjXurfma61ntHZuTtF9/fcebq8WqPrZd2hkeKk+bY/nV2ereMp9ZIolxSnuzzDr2KZYhmp4h2ennxmPSL+f7mWtx3ZJebR52pXe5TKZqeKDa7WJ47Ueil4aHKxOKlN5pO7/AOIz3Ijrx4Sfxaa4Li3IaA3CKC5E5LiXBcEZyA2JcIowLhiroEo26hqwxYqrsUuaVmVzr6MP6cao1b6XElWS++hj7crUi6luqV+vLqVSq9TNe+gZrRPxHIV0qnMCbeiKVNX15DQqWT1K+ji3M727i6crJfP0MXb21EqVrhlpxqo1NPu+yHc8yW9znOrYn4m3ILwt9lqdXW19gVMTaSdt0YXU1uVyqD0ONdOq0382VutrdlXalTkanFY+gIIEQ5vMZMeNRrVFEqiQv4hEsdOlj5J669NjbQxsZdbM83+JI8VoZvCUy2PVTqpK7ehRPHU08rkk1bzPLVcVJ6Nv/hU6oTxNa7eJ4y7tRtbo/wB+fgc6vjJS/wDptmJzFczpOEgaXMDnuZnVK3VHqsanVEdbYyuYMwyLF3aCuRVmJmHEsuBsrcgSkSPcmYrbBcji3MC5XmDmFHUiZivMRyBLMwLlWYDmWLFrYVOxllUK3ULGsbXiNGUTrt6GdyBcpFi1zFcivMLnHDi0GYpcxXIcWNHaAlV8jM5i5iw40OqK6pRmJcsOLXMVzEuBsWjOQLi3A5AjOQuYW5EyMhmwXAAjj6I5GSeIZsqYSpZ/lZl9n1vcZymPLFDkK5l74bW+GyezK/w5eRrZ9OMzmK5mp8Kr/Dfl6gfCcR8N+XqXbj9THmFczW+EYj4b8V6i+x8R8N+MfUe3H6GR1BHM2vg2I+G/GPqD2LiPh+cfUu3H6mHMDMbvY9f3POPqD2NX9z+UfUu0+lhuTMbfY9f3P5R9QeyK/ufyj6l2n1MbkDMbHwit7v8AKPqB8Kre6vqj6lsLHcjZr9lVtl9UfUnsursvqj6lsXpiuG5qfDKv6fqj6ivh1T9P1R9S2DYzXJmND4fU/T9SFeBnvH6kOxelGcVzLngp7x+pCPBy3j9SLSqlMWU7lrwct4+IPwst4+JFQ2JcveGlvHxFeGe68SKrMK5lrwr3XiLLDPePiPoqcwHIseHe68RXh3uvEircgXLHQe68RXRe6FelbYLjuk90Ds+9EdLclwuAHDvJQMwMxMjBkBoLkuTKTKRC4QWCkREgUgWBPovbS3YrxE92JclzljxaEsZU3YPx9TdhcUTs0OQ6R8RqbsHtOruF0B44Ntci9LVEuJ1X1ElxGr7xfX4bJK5lqYSSdrDOqB46r7zEljanvMWURbDkKPGVPeYksXU95jOAjpj6SPEz95i/iJbsDgLlL0TOvLd+IO2luwWFaJC6r3YrqPdkaA0STO9wZmSwLCRzMl2SxGBS7FbYxLCiNsSTZdlElEEozMXMy5xFcBKrMwNsZwFsJI2xW2WWBYkrdxSxxBlEqmAscRXEiW4AtEsCKAYjJojAPYDREpCNEREQgIBe+TGTEii6lRb5I5vAVF9DDSkbKWCS5muKtyMXn8OM1PBpPc1U6aWg6JY522tSFlESVKPOxbYFgVc3EcLjJ3XX1OfiOEyXI9EOom+9ix46rhpLRordNo9fUop80Z6mAg+hr9E8rkEyHo6nCV0MkuFMe8TiOmJKJ2nw97GepgXsM5ROVlBY3Twr2KJ0Xsb2JnaCkM4MgktgNDEJFIkEliKCSLLAaJKmGKIwEjqCaZVOkOmRyDCzzp2EcTWBxVmWnWKxEjVGmVuFma0qcpJQ0uWOAHeyLSocCKmX5RoLmFqY3AGQ15OSDOkXZpilEVxNUadxlSuXYxjygymmdPUWdOxa1FGUBoydCtxGUvpmFwPJs2wglyCiHltteTEGQEEycFkIgohggYxEiIRQw1iWDVhLAaLGgZS1WFSC4jJDNBpxUooEqEdi25C0YzTwkH0M9XhsH0N7Ia1lx6/A4taHMxnA5Ray63PWBGc7DjwNbBzi2muRRKDR9AqYaLvdc1Yw1uCwl0todZ5E8XYFj0+I/wAff+u3mYanBKi6dDXeLXHAb3w6YrwUlb5ou0LA4iWNrw7EVFj2LIwGmVIR0R7RKrliSsTsyKIWo2TQRxGb0CkBVumVypGpAyhqZHSEjDQ2yQFTHtWtZVAtcdC2EeYcmhm0xmhT5jZNPmXxjoGMAtMY3TDOly+ZrdMLhqg1qOd2f5n8yudLWx0FR1+YnZamuxfRAoUKOLzCEBCRkMKMRQYEQgli5AbIgGTRIiIJIQMYUjYUhGQWEJYiCRQZIUtgFSKIbDgJFJlCQSrdCL6IprYRPouafLY1xFmGrI5Nbh0WrWRU+FxtayOpIRG9ZscPEcI2Rz6/D2t/A9WzLjOX7G5yF9PJzopb+FipxR1cdz/Y5UjrIiuKIojAkWHQyiFm3yKxkWg2S5GKOE+YiYpAyFYgxQiHpmbGpUS0Cog6Dozh0rRHTC/vxGRYdf/Z');
    background-repeat: no-repeat;
    /* background-attachment: fixed; */
    background-position: center;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 10px;
    font-style: oblique;
    font-weight: bolder;
    font-variant: small-caps;
}

div.text-properties ul li{
    color: blue;
}
```

1. direction: It is used to display the direction of the text.
    
    By default the text direction is left to right.
    

syntax:

```jsx
css-selector{
	direction: ltr/rtl;
}
```

Examle:

style.css

```jsx
div.text-properties ul li{
    color: blue;
    direction: rtl;
}
```

1. text-decoration: It supports different decoration like underline, overline, line through etc..

syntax:

```jsx
css-selector{
	text-decoration: uderline;
}
```

example:

```jsx
div{
    background-color: blanchedalmond;
}

div.content{
    background-image: url('data:image/jpeg;base64,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');
    background-repeat: no-repeat;
    /* background-attachment: fixed; */
    background-position: center;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 10px;
    font-style: oblique;
    font-weight: bolder;
    font-variant: small-caps;
}

div.text-properties ul li{
    color: blue;
    /* direction: rtl; */
    text-decoration: line-through;
}
```

1. text-indent: This property is used to display indent at the starting of a paragraph.
2. text-align: This property is used to align the text in a specific direction.

Letter-spacing:

This property is used to apply space between letters.

syntax:

```jsx
css-selector{
	letter-spacing: value in pixel;
}
```

Word-spacing:

This property is used to add or substract space between the words.

syntax:

```jsx
css-selector{
	word-spacing: value in pixel;
}
```

text-transform:

This property is used to capitalize the text, convert text upper case or lower case format.

syntax:

```jsx
css-selector{
	text-transform: value;
}
```

different value for this property are: uppercase/ capitalize / lowercase etc.

white-space: This property is used to control the flow and formating of text.

syntax:

```jsx
css-selector{
	white-space: nowrap;
}
```

vertical-align: This property sets the vertical alignment of an element. It supports the below given list of values

1. baseline
2. sub
3. super
4. top
5. text-top
6. middle
7. bottom
8. text-bottom
9. 0px
10. 10px

text-properties example:

text-properties.html

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Text Properties</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Text Properties</h1>
    <p>There are different text properties in CSS. <span>Some of them are</span></p>
    <ol>
        <li>color</li>
        <li>text-align</li>
        <li>text-indent</li>
        <li>letter-spacing</li>
        <li>word-spacing</li>
        <li>text-transform</li>
        <li>white-space</li>
        <li>vertical align</li>
    </ol>
</body>
</html>
```

style.css

```jsx
h1{
    text-align: center;
    letter-spacing: 10px;
    word-spacing: 100px;
    text-transform: uppercase;
}
p{
    white-space: pre-wrap;
}
span{
    vertical-align: super;
}
```

CSS Border:

CSS supports the following list of border properties.

1. border-color : It is specifies the color of the border.
2. border-style : It specifies whether a border should be solid, dashed line, double line etc.
3. border-width: It specifies the width of the border.

example:

css-border.html

```jsx
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>CSS Border Properties</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <h1>CSS Border Properties</h1>
    <div>
        <p>There are different CSS Border properties in CSS. <span>Some of them are</span></p>
        <ol>
            <li>border-color</li>
            <li>border-style</li>
            <li>border-width</li>
        </ol>
    </div>
</body>

</html>
```

style.css

```jsx
h1{
    text-align: center;
    letter-spacing: 10px;
    word-spacing: 100px;
    text-transform: uppercase;
}
p{
    white-space: pre-wrap;
}
span{
    vertical-align: super;
}

div{
    border-color: green;
    border-style: dashed;
    border-width: 5px;
}
```

Working with advanced Style Sheets( CSS3) .

CSS3 is the latest version of the CSS which is being is used. 

It is divided into several modules. Each module having new capabilities and extended features. 

some of the features introduced in CSS3 are:

1. font-face
2. opacity
3. RGBA(Red Green Blue Alpha or  Amber)
4. Border-radius
5. box-shadow
6. text-shadow
7. gradient
8. multiple background images
9. transform
10. transition
11. multi column layout
12. styling forms with attribute selector
13. wrapping up
14. Box-sizing and Box-model
15. CSS3 new selector

## CSS3 Browser Support:

→ In CSS3 we are using the following prefixes for advanced properties:

1. IE requires the prefix -ms- (microsoft seen)
2. FireFox requires the prefix -moz-
3. Chrome and Safari requires the prefix -webkit-
4. opera requires a prefix -o-

## CSS3 Multiple Column Properties:

In CSS3 we can create multiple columns layout for e-news paper. 

The following is the list of properties frequently used :

1. column-count
2. column-gap
3. column-rule
4. column-fill
5. column-rule-color
6. column-rule-style
7. column-rule-width
8. column-span
9. column-width
10. columns

1. Column-count: This property is used to specify number of columns and elements divided into:

syntax:

```jsx
css-selector{
	column-count: number/auto;
}
```

| value | Description |
| --- | --- |
| number | The optimal number of columns into which the content of the element will be flowed |
| auto | The number of columns will be determined by other properties. |

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Column Properties</title>
    <style>
        div{
            column-count: 3;
            -moz-column-count: 3; 
            -webkit-column-count: 3;
            -ms-column-count:3;
            -moz-column-count: 3;
        }
    </style>
</head>
<body>
    <div>
        Some text ..........!!
    </div>
</body>
</html>
```

1. column-gap:

This property specifies the gap between the columns.

syntax:

```jsx
css-selector{
 column-gap: length/normal;
}
```

| value | Description |
| --- | --- |
| length | A specified lenght that will set the gap between the columns. |
| normal | specifies a normal gap between the columns |
1. column-rule property:

It is a shorthand property for setting all the column-rule properties. 

The column-rule property sets the width, style and color of the rule between the columns.

Syntax: 

```jsx
css-selector{
	column-rule: column-rule-width column-rule-style column-rule-color;
}
```

| value | description |
| --- | --- |
| column-rule-width | sets the width of the rule between the columns. |
| column-rule-style | it sets the style of the rule between the columns. |
| column-rule-color | sets the color of the rule between columns. |

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Column Properties</title>
    <style>
        div{
            column-count: 3;
            -moz-column-count: 3; 
            -webkit-column-count: 3;
            -ms-column-count:3;
            text-align: justify;
            column-gap: 30px;
            -moz-column-gap: 30px;
            -webkit-column-gap: 30px;
            -ms-column-gap: 30px;
            /* column-rule-width: 10px;
            -moz-column-rule-width: 10px;
            -webkit-column-rule-width: 10px;
            -ms-column-rule-width: 10px;
            column-rule-style: solid;
            -moz-column-rule-style: solid;
            -webkit-column-rule-style: solid;
            -ms-column-rule-style: solid;
            column-rule-color: brown;
            -moz-column-rule-color: brown;
            -webkit-column-rule-color: brown;
            -ms-column-rule-color: brown; */
            column-rule: 10px dashed green;
            -moz-column-rule: 10px dashed green;
            -webkit-column-rule: 10px dashed green;

        }
    </style>
</head>
<body>
    <div>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem nisi optio hic quae quod quasi tenetur provident corrupti quidem facere? Nisi beatae, consequuntur vel ex at earum animi. Dignissimos, tempore.
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aut quam at illum. Quos quis cumque iusto aliquam aut tempore saepe veritatis aperiam repellat quasi fugiat quod nobis consequatur, quam atque?
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto magnam quia doloremque tenetur placeat blanditiis nam debitis officia voluptas, inventore delectus beatae reprehenderit obcaecati recusandae voluptatem at animi suscipit repudiandae.
    </div>
    
</body>
</html>
```

1. column-fill: It specifies how to fill columns, balanced or not.

syntax:

```jsx
css-selector{
	column-fill balance/ auto;
}
```

| value | description |
| --- | --- |
| balance | columns are balanced. Browsers should minimize the variation in column length |
| auto | columns are filled sequentially, and they will have different lenght. |

Note: Currently no major web browser supports this property.

1. column-span: It specifies how many columns an element should span across.

syntax:

```jsx
css-selctor{
	column-span: 1/all;
}
```

| value | description |
| --- | --- |
| 1 | The element should span across 1 column. |
| all  | The element should span across all the columns |

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Column Properties</title>
    <style>
        div{
            column-count: 3;
            -moz-column-count: 3; 
            -webkit-column-count: 3;
            -ms-column-count:3;
            text-align: justify;
            column-gap: 30px;
            -moz-column-gap: 30px;
            -webkit-column-gap: 30px;
            -ms-column-gap: 30px;
            /* column-rule-width: 10px;
            -moz-column-rule-width: 10px;
            -webkit-column-rule-width: 10px;
            -ms-column-rule-width: 10px;
            column-rule-style: solid;
            -moz-column-rule-style: solid;
            -webkit-column-rule-style: solid;
            -ms-column-rule-style: solid;
            column-rule-color: brown;
            -moz-column-rule-color: brown;
            -webkit-column-rule-color: brown;
            -ms-column-rule-color: brown; */
            column-rule: 10px dashed green;
            -moz-column-rule: 10px dashed green;
            -webkit-column-rule: 10px dashed green;
            

        }
        h1{
            /* column-span: 1;
            -moz-column-span: 1;
            -webkit-column-span: 1;
            -ms-column-span: 1; */
            text-align: center;
            column-span: all;
            -moz-column-span: all;
            -webkit-column-span: all;
            -ms-column-span: all;
        }
    </style>
</head>
<body>
    <div>
        <h1>Todays Headlines</h1>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem nisi optio hic quae quod quasi tenetur provident corrupti quidem facere? Nisi beatae, consequuntur vel ex at earum animi. Dignissimos, tempore.
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aut quam at illum. Quos quis cumque iusto aliquam aut tempore saepe veritatis aperiam repellat quasi fugiat quod nobis consequatur, quam atque?
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto magnam quia doloremque tenetur placeat blanditiis nam debitis officia voluptas, inventore delectus beatae reprehenderit obcaecati recusandae voluptatem at animi suscipit repudiandae.
    </div>
    
</body>
</html>
```

1. column-width: It specifies the width of the column.

syntax:

```jsx
css-selector{
	column-width: auto/length;
}
```

| value | description |
| --- | --- |
| auto | The column width will be determined by the browser |
| length  | A length that specifies the width of the column |

Note: If you are going to increase the size of the page then number of columns will be decreased and vise-versa.

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Column Properties</title>
    <style>
        div{
            column-count: 3;
            -moz-column-count: 3; 
            -webkit-column-count: 3;
            -ms-column-count:3;
            text-align: justify;
            column-gap: 30px;
            -moz-column-gap: 30px;
            -webkit-column-gap: 30px;
            -ms-column-gap: 30px;
            /* column-rule-width: 10px;
            -moz-column-rule-width: 10px;
            -webkit-column-rule-width: 10px;
            -ms-column-rule-width: 10px;
            column-rule-style: solid;
            -moz-column-rule-style: solid;
            -webkit-column-rule-style: solid;
            -ms-column-rule-style: solid;
            column-rule-color: brown;
            -moz-column-rule-color: brown;
            -webkit-column-rule-color: brown;
            -ms-column-rule-color: brown; */
            column-rule: 10px dashed green;
            -moz-column-rule: 10px dashed green;
            -webkit-column-rule: 10px dashed green;
            column-width: 50px;
            -moz-column-width: 50px;
            -webkit-column-width: 50px;
            -ms-column-width: 50px;
            

        }
        h1{
            /* column-span: 1;
            -moz-column-span: 1;
            -webkit-column-span: 1;
            -ms-column-span: 1; */
            text-align: center;
            column-span: all;
            -moz-column-span: all;
            -webkit-column-span: all;
            -ms-column-span: all;
            column-width: 10px;
        }
    </style>
</head>
<body>
    <div>
        <h1>Todays Headlines</h1>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem nisi optio hic quae quod quasi tenetur provident corrupti quidem facere? Nisi beatae, consequuntur vel ex at earum animi. Dignissimos, tempore.
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aut quam at illum. Quos quis cumque iusto aliquam aut tempore saepe veritatis aperiam repellat quasi fugiat quod nobis consequatur, quam atque?
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto magnam quia doloremque tenetur placeat blanditiis nam debitis officia voluptas, inventore delectus beatae reprehenderit obcaecati recusandae voluptatem at animi suscipit repudiandae.
    </div>
    
</body>
</html>
```

1. columns: This property is shorthand property for setting column width and column count.

syntax:

```jsx
css-selector{
	columns: column-width column-count;
}
```

| value  | description |
| --- | --- |
| column-width | The width of the column |
| column-count | The number of columns |

### Working with the CSS3 background property

CSS3 supports the following list of advanced background properties.

| property name | Description |
| --- | --- |
| background-size | specifies the size of the background images. |
| background-origin | specifies the positioning area of the background images |
| background-clip | specifies the painting area of the background images. |
1. background-size:

syntax:

```jsx
css-selector{
	background-size:	length | percentage | cover | contain;
}
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Background size property</title>
    <style>
        body{
            background: url('engineer.jpg');
            background-size: 480px 480px;
            -moz-background-size: 480px 480px;
            background-repeat: no-repeat;

        }
    </style>
</head>
<body>
    <p>CSS-Image</p>
    <p>Original Image: <img src="https://media.istockphoto.com/photos/cloud-network-solution-picture-id1273823720?b=1&k=20&m=1273823720&s=170667a&w=0&h=ABsUVn4aZc1_nn2ftEijeVpIBeKTiTxuAH1hFdTIo7c=" alt="image" width="200" height="200"></p>
</body>
</html>
```

### Background clip:

syntax:

```jsx
css-selector{
	background-clip: border-box | padding-box | content-box ;
}
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Background size property</title>
    <style>
        body{
            background: url('engineer.jpg');
            background-size: 480px 480px;
            -moz-background-size: 480px 480px;
            background-repeat: no-repeat;

        }
        div{
            width: 300px; height: 300px;
            padding: 50px;
            background-color: lightblue;
            background-clip: border-box;
            border: 4px dashed #FF0000;
            text-align: justify;
        }
    </style>
</head>
<body>
    <p>CSS-Image</p>
    <p>Original Image: <img src="https://media.istockphoto.com/photos/cloud-network-solution-picture-id1273823720?b=1&k=20&m=1273823720&s=170667a&w=0&h=ABsUVn4aZc1_nn2ftEijeVpIBeKTiTxuAH1hFdTIo7c=" alt="image" width="200" height="200"></p>
    <div>
        Hi I am background property.
    </div>
</body>
</html>
```

### 3. background-origin:

This property specifies what the background position property relative to.

syntax:

```jsx
css-selector{
	background-origin: padding-box | border-box | content-box;
}
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Background size property</title>
    <style>
        body{
            background: url('engineer.jpg');
            background-size: 480px 480px;
            -moz-background-size: 480px 480px;
            background-repeat: no-repeat;

        }
        div{
            width: 300px; height: 300px;
            padding: 50px;
            /* background-color: lightblue; */
            background-clip: border-box;
            border: 4px dashed #FF0000;
            text-align: justify;
            background-image: url('./origin.jpg');
            background-repeat: no-repeat;
            background-position: left;
            background-origin: content-box;
        }
    </style>
</head>
<body>
    <p>CSS-Image</p>
    <p>Original Image: <img src="https://media.istockphoto.com/photos/cloud-network-solution-picture-id1273823720?b=1&k=20&m=1273823720&s=170667a&w=0&h=ABsUVn4aZc1_nn2ftEijeVpIBeKTiTxuAH1hFdTIo7c=" alt="image" width="200" height="200"></p>
    <div>
        Hi I am background property.
    </div>
</body>
</html>
```

### Working with CSS3 borders

CSS3 supports the following list of advanced properties:

| property | Description |
| --- | --- |
| border-image | A shorthand property for setting all the border image-properties. |
| border-radius | A shorthand property for setting all the four border - * - radius properties  |
| box-shadow | Attaches one or more drop-shadows to the box. |
1. border-image: It is a shorthand property for setting a border image source, border image slice, border-image-width, border-image-outset, border-image-repeat peroperties.

syntax:

 

```jsx
css-selector{
	border-image: source slice width outset repeat;
}
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Border CSS3 Properties</title>
    <style>
        div{
            border: 15px solid transparent;
            width: 250px;
            padding: 10px 20px;
        }
        #round{
            border-image: url('engineer.jpg') 30 30 round;
        }
    </style>
</head>
<body>
    <div id="round">
        I a border property.
    </div>
</body>
</html>
```

1. Box-shadow: The box shadow property attaches one or more drop shadows to the box.

syntax:

```jsx
css-selector{
	box-shadow: h-shadow v-shadow blur-shadow;
}
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Border CSS3 Properties</title>
    <style>
        div{
            border: 15px solid transparent;
            width: 250px;
            padding: 10px 20px;

            /* box-shadow property */
            width: 300px;
            height: 80px;
            box-shadow: 15px 15px 15px #FF0000;
        }
        #round{
            border-image: url('engineer.jpg') 30 30 round;
        }
    </style>
</head>
<body>
    <div id="round">
        I a border property.
    </div>
</body>
</html>
```

1. Border-radius:

It is a shorthand property for setting the four border-*-radius properties.

syntax:

```jsx
css-selector{
	border-radius: 1-4 length % / px;
}
```

### CSS3 Text Properties

CSS3 supports the following list of text properties:

1. hanging-punctuation.
2. punctuation-trim.
3. text-emphasis.
4. text-justify
5. text-overflow
6. text-shadow
7. text-wrap
8. word-wrap
9. word-break

1. word-wrap property:

This property allows long words to be able to be broken and wrap on to the next line.

syntax:

```jsx
CSS:
css-selector{
	word-wrap: normal | break-word;
}

JavaScript:
object.style.word-wrap = "break-word";
```

attributes

| value | description |
| --- | --- |
| normal | Breaks words only at allowed break points. |
| break-word | Allows underbreakable words to be broken. |

-malicious

Text wrap property:

This property specifies line breaking rules for text.

syntax:

```jsx
css-selector{
	text-wrap : normal | none | unrestricted | supress;
}

Javascript:
object.style.textwrap = "none | normal | supress | unrestricted ".
```

NOte: This property currently not supported by major of the browsers.

1. text-shadow: 

This property applies to text you specify the horizontal shadow, the vertical shadow, the blur distance, and the color of the shadow.

syntax:

```jsx
CSS
css-selector{
	text-shadow: h-shadow v-shadow blur color;
}

JavaScript:
object.style.textShadow = "2px 2px #FF0000";
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Text Properties</title>
    <style>
        div{
            width: 10 px;
            background-color: bisque;
            border: 2px solid #FF0000;
            word-wrap: break-word;
            font-size: 30px;
            /* text shadow */
            text-shadow: 2px 2px green;

        }
    </style>
</head>
<body>
    <div>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Modi reiciendis natus ullam optio maxime, cumque commodi exercitationem aperiam tempore, unde distinctio ipsum nisi ipsam est architecto. Aliquid officiis nam quia? Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ducimus modi iste consequatur iusto beatae adipisci quibusdam quia! Numquam saepe perferendis earum fuga officiis, esse dignissimos, cupiditate quasi cum culpa maxime! Lorem ipsum dolor sit amet consectetur adipisicing elit. Aut impedit, suscipit possimus veritatis incidunt culpa nulla voluptas molestias dolorem nemo vitae nesciunt commodi assumenda ea est dignissimos nisi quas ex!</div>
</body>
</html>
```

The text overflow property:

This property specifies what should happen when text overflow the containing element.

syntax: 

```jsx
css:
css-selector{
	text-overflow: clip | ellipses | string;
}

JavaScript:
object.style.textoverflow= "ellipses";
```

| value  | Description |
| --- | --- |
| clip |  clips the text |
| ellipses  | renders an ellipsis (”......”) to represent clipped text. |
| string | render the given string to represent clipped text. |

example:

```jsx
<!DOCTYPE html>
<html>

<head>
    <style>
        div.a {
            white-space: nowrap;
            width: 50px;
            overflow: hidden;
            text-overflow: clip;
            border: 1px solid #000000;
        }

        div.b {
            white-space: nowrap;
            width: 50px;
            overflow: hidden;
            text-overflow: ellipsis;
            border: 1px solid #000000;
        }

        div.c {
            white-space: nowrap;
            width: 50px;
            overflow: hidden;
            text-overflow: "----";
            border: 1px solid #000000;
        }
    </style>
</head>

<body>

    <h1>The text-overflow Property</h1>

    <p>The following two divs contains a text that will not fit in the box.</p>

    <h2>text-overflow: clip (default):</h2>
    <div class="a">Hello world!</div>

    <h2>text-overflow: ellipsis:</h2>
    <div class="b">Hello world!</div>

    <h2>text-overflow: "----" (user defined string):</h2>
    <div class="c">Hello world!</div>

    <p><strong>Note:</strong> The text-overflow: "<em>string</em>" only works in
        Firefox.</p>

</body>

</html>
```

### text-justify:

this property specifies the justification method to use when text-align is set to “justify”.  This property specifies how justified text should be aligned and spaced.

syntax:

```jsx
css-selector{
	text-justify: auto | inter-word | inter-ideograph | inter-cluster | distribute | kashida | trim;
}

Javascript syntax:
	object.style.textjustify="inter-word";
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>text-justify property</title>
    <style>
        div{
            text-align: justify;
            text-justify: distribute;
        }
    </style>
</head>
<body>
    <div>Some text ......... resize the browser ........ Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolore quaerat, dignissimos, blanditiis corrupti sit quisquam id hic error mollitia voluptates culpa commodi nesciunt! Cumque, tempore itaque rerum maiores incidunt autem. Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore maiores nobis temporibus ab! Hic eveniet ipsa facilis porro unde excepturi consequuntur molestias, magnam nemo non animi neque, maxime perspiciatis cum.</div>
</body>
</html>
```

## CSS3 font properties

CSS3 supports the following list of advanced font properties

1. @ font-face
2. font-size-adjust
3. font-stretch

1. font-face:
    
    The CSS3 font-face rule: Your “own” fonts are defined in the CSS3 @font-face.
    
    Before CSS3 web designers had to use fonts that are already installed in the user computers .
    
    refer to www.1001freefonts.com
    
    types of font we can create:
    
    1. ttf : true type fonts
    2. .otf: open type fonts
    3. .eot: embedded open type 
    4. .woff: web open font format
    5. svg - scalable vector graphics
    
    Note: Firefox, Chrome, Safari and opera support font of type .ttf and .otf.
    
    Note: Internet explorer support the new @font-face rule, but it only supports fonts of type .eot
    
    example:
    
    ```jsx
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>CSS3 Text properties</title>
        <style>
            @font-face {
                font-family: myfirst font;
                src: url('Angeline_Vintage_Demo.otf');
            }
            div{
                font-family: myfirst font;
            }
        </style>
    </head>
    <body>
        <div>
            some text
        </div>
    </body>
    </html>
    ```
    

1. font-size-adjust:

This property gives you better control of the font-size.

syntax:

```jsx
css-selector{
	font-size-adjust: number|none|inherit;
}
```

| value | description |
| --- | --- |
| number | defines the aspect value to use. |
| none | default value, no font size adjustment |
| inherit | Inherits the font-size adjustment from parent element. |

Example:

to be continued

1. font-stretch: 
    
    This property makes or allow text wider and narrower.
    

syntax:

```jsx
css-selector{
	font-stretch: wider | narrower | ultra-condensed | extra-condensed | consdensed | 
									normal| semi-expanded | extra-sexpanded | ultra -expanded | inherit
}
```

Note: none of the major browsers supports the font-stretch property.

### CSS3 Transform:

Transform is a powerfull property to move, scale, turn, spin and stretch the given element.

It supports the following list of properties:

1. transfrom
2. transform-origin.
3. transform-style.

Transform supports the following five methods as well:

1. translate()
2. rotate()
3. scale()
4. skew()
5. matrix()

1. translate(): 

This method can be used to move any object depending on its parameter.

This method takes two types of parameters

1. from left(x-axis) parameter.
2. from top(y-axis) parameter.

syntax:

```jsx
css-selector{
	transform: translate(x,y);
}
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Translate() of transform property</title>
    <style>
            div{
                width: 90px;
                height: 60px;
                border: 2px solid #FF00FF;
            }
            div#div1{
                transform: translate(20px,30px);
            }
            div#div2{
                transform: translate(40px,60px);
            }
    </style>
</head>
<body>
    <div id="div1"></div>
    <div id="div2"></div>
</body>
</html>
```

1. Rotate(): Wih the help of this method you can rotate your object depending on its value. 

Two types of value you can pass in this method one is positive and the other one is negative.

Syntax: 

```jsx
css-selector{
	transform: rotate(x,y)
}

where x -> represents clock wise rotation.
			y -> represents counter-clock wise rotation
```

Example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Translate() of transform property</title>
    <style>
            div{
                width: 90px;
                height: 60px;
                border: 2px solid #FF00FF;
            }
            div#div1{
                transform: translate(20px,30px) rotate(30deg);
            }
            div#div2{
                transform: translate(40px,60px);
            }
    </style>
</head>
<body>
    <div id="div1"></div>
    <div id="div2"></div>
</body>
</html>
```

1. scale: With the help of this method you can increase or decrease your object size depending on its value passed in the parameter.
    
    We can pass two types of values in the scale() parameter, 
    
    1. For width (x-axis)
    2. For height (y-axis)
    
    syntax:
    
    ```jsx
    css-selector{
    	transform: sclae(x,y);
    }
    ```
    
    Example:
    
    ```jsx
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Translate() of transform property</title>
        <style>
                div{
                    width: 90px;
                    height: 60px;
                    border: 2px solid #FF00FF;
                }
                div#div1{
                    transform: translate(20px,30px) rotate(30deg) scale(0.5,3);
                }
                div#div2{
                    transform: translate(40px,60px);
                }
        </style>
    </head>
    <body>
        <div id="div1"></div>
        <div id="div2"></div>
    </body>
    </html>
    ```
    
2. skew(): With the help of this method you can change the angle of your object depending on its value passed in the parameter. 
    
    We can pass two parameters in skew() method:
    
    1. for horizontal (x-axis)
    2. for vertical (y-axis)
    
    syntax:
    
    ```jsx
    css-selector{
    	transform: skew(x,y);
    }
    x-> angle in x axis.y-> angle in y axis.
    
    ```
    
    example:
    
    ```jsx
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Translate() of transform property</title>
        <style>
                div{
                    width: 90px;
                    height: 60px;
                    border: 2px solid #FF00FF;
                }
                div#div1{
                    transform: translate(20px,30px) rotate(30deg) scale(0.5,3) skew(20deg,30deg);
                }
                div#div2{
                    transform: translate(40px,60px);
                }
        </style>
    </head>
    <body>
        <div id="div1"></div>
        <div id="div2"></div>
    </body>
    </html>
    ```
    
3. matrix():

The **`matrix()`**
 [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) [function](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Functions) defines a homogeneous 2D transformation matrix. Its result is a `[<transform-function>](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function)`data type.

The `matrix()` function is specified with six values. The constant values are implied and not passed as parameters; the other parameters are described in the column-major order.

syntax:

```jsx
css-selector{
	transform: matrix(a, b, c, d, tx, ty);
}
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Translate() of transform property</title>
    <style>
            div{
                width: 90px;
                height: 60px;
                border: 2px solid #FF00FF;
            }
            div#div1{
                /* transform: translate(20px,30px) rotate(30deg) scale(0.5,3) skew(20deg,30deg); */
                transform: matrix(1, 2, -1, 1, 80, 80);
            }
            div#div2{
                transform: translate(40px,60px);
            }
    </style>
</head>
<body>
    <div id="div1"></div>
    <div id="div2"></div>
</body>
</html>
```

For more reference visit: [https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/matrix()](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/matrix())

### CSS Transitions

A transition is such a property of CSS3 which is used to animate the objects, without using flash or any other animation application/software.

This CSS3 feature allows us to change the shape and the size of our object with animated effects.

IT supports the following list of properties

1. Transition: A shorthand property for setting the four transition property into a single property.
2. transition-property: It specifies the name of the css property to which the transition is applied.
3. transition-duration: It defines the length of time that a transition takes.
4. transition-timing-function: It describes how the speed during the transition will be required.
5. transition-delay: It specifies when the transition effect will start. The transition-delay value is defined in seconds(s) or miliseconds(ms).

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Transition Property</title>
    <style>
        div#div1{
            width: 100px;
            height: 60px;
            border: 2px solid salmon;
            background-color: blueviolet;
            transition: width;
            border-radius: 20px;
            transition-duration: 1s;
        }
        div#div1:hover{
            width: 350px;
        }
    </style>
</head>
<body>
    <div id="div1"></div>
    <div></div>
</body>
</html>
```

with transtion-delay property

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Transition Property</title>
    <style>
        div#div1{
            width: 100px;
            height: 60px;
            border: 2px solid salmon;
            background-color: blueviolet;
            transition: width;
            border-radius: 20px;
            transition-duration: 1s;
            transition-delay: 3s;
        }
        div#div1:hover{
            width: 350px;
        }
    </style>
</head>
<body>
    <div id="div1"></div>
    <div></div>
</body>
</html>
```

For more on transition-timing-function refer [https://developer.mozilla.org/en-US/docs/Web/CSS/transition-timing-function](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-timing-function)

### CSS3 Animation

CSS3 supports the following list of advanced animations. We can create animations, which can replace animated images, flash animation and javascript in many webpages.

Animation is a property to change an object from one style to another style in a animated way.

Different animation properties in CSS3 are listed below:

1. @keyframes
2. animation
3. animation name
4. animation duration
5. animation delay
6. animation direction

1. @keyframes:

The @keyframes rule is where the animation is created, specify a css style inside the @keyfames rule and the animation will gradually change from the current style to the new style. we can create user defined animations

How to implement the animation:

An animation is an effect that lets element gradually change from one style to another style. 

We can chages as many styles as we want and we can also change as many times as we want.

To implement we need to specify when the change will happen in percent or the kewords “from”  & “to” which is the same as 0% and 100% . 

where 0% is the begining of the animation .

100% when the animation completes.

CSS3 Animation property:

The animation property is a shorthand property for all the six of the animation properties: 

1. animation-name,
2. animation-duration,
3. animation-timing-function
4. animation-delay
5. animation-iteration-count
6. animation-direction

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Animation</title>
    <style>
        div{
            width: 90px;
            height: 60px;
            background-color: #FF9900;
            transition: width;
            float: right;
            transition-duration: 5s;
        }
        div:hover{
            width: 350px;
        }
    </style>
</head>
<body>
    <div></div>
</body>
</html>
```

How to apply multiple transition

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Multiple Transition</title>
    <style>
        div{
            width: 90px;
            height: 60px;
            background-color: #FF0000;
            border-radius: 20px;
            transition: width;
            transition-duration: 2s;
        }
        div:hover{
            width: 350px;
        }
        #div-cont{
            width: 90px;
            height: 60px;
            background-color: #FF00FF;
            transition: width;
            border-radius: 5px;
        }
        div#div-cont:hover{
            width: 400px;
        }
    </style>
</head>
<body>
    <div></div><br>
    <div id="div-cont"></div>
</body>
</html>
```

Transition property: The transition property is a shorthand property for the four transition properties:

1. transition property.
2. transition duration
3. transition-timing-function
4. transition-delay

syntax:

```jsx
css-selector{
	transition: property duration timing-function delay;
}
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Transition Shorthand property</title>
    <style>
        div{
            width: 90px;
            height: 60px;
            background-color: #FF0000;
            transition: width 2s;
        }
        div:hover{
            width: 350px;
        }
    </style>
</head>
<body>
    <div></div>
</body>
</html>
```

### Transition Duration:

It specifies how many seconds(s) or milliseconds(ms) a transition effect takes to complete.

syntax: 

```jsx
css-selector{
	transition-duration: time;
	}
```

| value | description |
| --- | --- |
| time | specifies how many seconds or milliseconds a  transition effect takes to complete. |
|  |  |

### Transition Timing Function:

It specifies the speed curve of the transition effect. This property allows a transition effect to change speed over its duration.

syntax:

```jsx
css-selector{
	transition-timing -function: linear | ease | ease-in | ease-out | ease-in-out | cubic-bezier(n,n,n,n);
}
```

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Transition Shorthand property</title>
    <style>
        div{
            width: 90px;
            height: 60px;
            background-color: #FF0000;
            transition: width 2s step-end;
        }
        div:hover{
            width: 350px;
        }
    </style>
</head>
<body>
    <div></div>
</body>
</html>
```

### Working with Advanced selectors

### Attribute Selectors

In CSS3 selectors means styles reusability. There are the following list of advanced selectors:

1. [attribute ^=values] selctor:

The [attribute ^= value] selector, matches every element whose attribute value begins with the specified value.

It is supported by major of the browsers. for example:

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Attribute Selector</title>
    <style>
        div[class ^="test"]{
            background: #ff0000; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            
        }
    </style>
</head>
<body>
    <div class="first-test">The first division element</div>
    <div class="test">This is the second division element</div>
    <p class="test">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatum nobis libero architecto porro autem explicabo similique pariatur quo saepe esse. Unde corporis assumenda, nihil delectus eius est? Tempora, esse dignissimos.</p>

</body>
</html>
```

1. CSS3 [attribute $=value] selector:

The [attribute $= value] selector matches every element whose attribute value ends with a specified value.

Note: The [attribute $= value] selector is supported in all major browsers.

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Attribute Selector</title>
    <style>
        /* attribute selector */
        div[class $="test"]{
            background: #ff0000; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;

        }
    </style>
</head>
<body>
    <div class="first-test">The first division element</div>
    <div class="second-test">The second division element</div>
    <div class="test">This is the second division element</div>
    <p class="test">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatum nobis libero architecto porro autem explicabo similique pariatur quo saepe esse. Unde corporis assumenda, nihil delectus eius est? Tempora, esse dignissimos.</p>

</body>
</html>
```

1. CSS [attribute *= value] selector:

This attribute selector matches every element whose attribute value contains a specified value.

It is supported by major of the browsers.

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Attribute Selector</title>
    <style>
        /* attribute selector */
        div[class *="test"]{
            background: #ff0000; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;

        }
    </style>
</head>
<body>
    <div class="first-test">The first division element</div>
    <div class="second">The second division element</div>
    <div class="test">This is the second division element</div>
    <p class="test">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatum nobis libero architecto porro autem explicabo similique pariatur quo saepe esse. Unde corporis assumenda, nihil delectus eius est? Tempora, esse dignissimos.</p>

</body>
</html>
```

### CSS3 - First of type selector:

The first of type selector matches every element that is the first child, of a particular type of its parent.

This is supported by major browsers except the IE8.

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>First of type Selector</title>
    <style>
        p:first-of-type{
            background: #00ff00;
        }
    </style>
</head>
<body>
    <h1>This is a heading</h1>
    <p>This is first paragraph.</p>
    <p>This is the second paragraph</p>
    <p>This is the third paragraph.</p>
</body>
</html>
```

### CSS3- only-of-type selector:

The only-of-type selector matches every element that is the only child of its type of its parent.

example:

```jsx
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>First of type Selector</title>
    <style>
        p:only-of-type {
            background: #00ff00;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
    </style>
</head>

<body>
    <h1>This is a heading</h1>
    <div>
        <p>This is first paragraph.</p>
        <p>This is the second paragraph</p>
    </div>
    <p>This is the third paragraph.</p>
</body>

</html>
```

### CSS3- nth-child selector:

The nth child selector matches every element that is the nth child regardless of type of its parent.

It is supported by major of the modern web browsers.

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>nth child Selector</title>
    <style>
        p:nth-child(4){
            background: #00ff00;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
    </style>
</head>
<body>
    <h1>This is a heading</h1>
    <p>This is first paragraph.</p>
    <p>This is the second paragraph</p>
    <p>This is the third paragraph.</p>
    <p>This is the fourth paragraph.</p>
</body>
</html>
```

### CSS3 User Interface

User Interface is powerful property in CSS3 which is used to implement user interface without modifing a code section. 

You can resize div element and set the user interface property as shown below:

**CSS3 Resizing**

It specifies whether or not an elment should be resizable by the user.

**resize:** It is a property of user interface, by which you can resize your div layout on your browser. Three features of resize are:

1. resize: both
2. resize: vertical
3. resize: horizontal

syntax:

```jsx
css-selector{
	resize: none | both| horizontal | vertical
}
```

| value | description |
| --- | --- |
| none | user cannot resize the element. user can’t  adjust both the height and the width |
| horizontal | User can adjust the width of the of the element |
| vertical | user can adjust the height of the element. |
| both | user can resize the height and width of the element  |

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Basic UI Resizing.</title>
    <style>
        div{
            border: 2px solid;
            padding: 10px 40px;
            width: 300px;
            resize: vertical;
            overflow: auto;
        }
    </style>
</head>
<body>
    <div>Deepika </div>
</body>
</html>
```

### HTML5 Web Storage

It has the following alias name:

1. Client side storage
2. Web storage
3. offline storage
4. Local storage

It is very close to cookies concept. The main intension of web storage is, to store the data at client side without disturbing the perfromance of  the website.

In HTML5 web storage is classified into two types 

1. session storage
2. local storage.

1. session storage: 

It is also uses browsers data locally but it is for limited period of time when we close the browser it will automatically delete the stored data and we can’t see the browsers stored data again. 

HTML5 introduces the session storage attribute which would be used by the sites to add data to the session storage.

example:

```jsx

```

### Local Storage

Local storage is used to store the data locally. It stores the dat with no expiry date, means if browser is closed then it will not delete the data and we can view the data any time and even after years.

exxample:

```jsx

```

### Web SQL

Web SQL database is webpage API for storing data in databases that can be queried using a variant of SQL. The API is supported by Google Chrome, opera, safari, edge, android browser etc.

To work with Web SQL follow [https://developer.chrome.com/docs/devtools/storage/websql/?utm_source=devtools](https://developer.chrome.com/docs/devtools/storage/websql/?utm_source=devtools)

### Indexed DB:

It is basically a persistant data store in the browser a database on the client side .

Like a regular relational databases it maintains indexes over the records it stores and developers use the IndexDB Javascript API to locate records by key or by looking up for an index.

For more on IndexDB go on [https://developer.chrome.com/docs/devtools/storage/indexeddb/?utm_source=devtools](https://developer.chrome.com/docs/devtools/storage/indexeddb/?utm_source=devtools)

### HTML5 Geolocation( Deeper integration with OS)

HMTL5 Geolocation API allows users to share their location with web applications by capturing the approximate longitude and latitude coordinates of the user with their permission.

### latitude:

Latitude is a geographical coordinate that specifies the north-south position of a point on the earth surface.

### Longitude

It is a geographical coordinate that specifies the east - west position of a point on the earth surface.

### Types of Maps

Maps are classified into following basic types:

1. RoadMap(normal, default 2D map)
2. Satelite Map( photographic map)
3. Hybrid Map( Photographic map + roads &: cities name)
4. Terrain Map( Map with mountains, rivers etc)

### Google Maps controls

Google maps supports the following list of controls

1. zoom
2. pan
3. map type
4. street view
5. scale
6. rotate

### write a script to verify the map browser support

 

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Browser Map Support</title>
    <script>
        function mySupport(){
            if(navigator.geolocation){
                alert("your browser supports map services")
            }else{
                alert("you browser doesn't support the map services")
            }
        }
    </script>
</head>
<body>
    <p>Click the button to display the Map</p>
    <button onclick="mySupport()">Support Browser</button>
</body>
</html>
```

### GeoLocation methods

some of the important geolocation methods are: 

| method | description |
| --- | --- |
| getcurrentposition() | It retrieves the current geographical location of the user  |
| watchpostion() | It retrieves periodic updates about the current geographical location of the device. |
| clearwatch() | This method cancels an ongoing watch position call. |

For more details refer to [https://developer.mozilla.org/en-US/docs/Web/API/Geolocation](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation)

### Working with HTML5 Drag and Drop

Drag and Drop is powerful user interface concept in HTML5 which makes it easy to copy, reorder and deletion of items with the help of mouse clicks.

It allows the user to click and hold the mouse button down over an element, drag it to another location, release the mouse button.

### Creating a Draggable content

Making an object draggable is very simple, we just need to set an attribute ie

`draggable = true` on the element we want to make draggable/movable.

example:

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dragable content</title>
    <style>

    </style>
    
</head>
<body>
    <img src="https://image.shutterstock.com/image-photo/word-demo-appearing-behind-torn-260nw-1782295403.jpg" width="100px" height="50px" draggable="true">
</body>
</html>
```

### Drag & Drop events

Drag and Drop supports different events like

1. dragStart
2. dragEnter
3. dragOver
4. dragLeave
5. drag
6. drop
7. dragEnd

allow drop: By default all elements are not dragged or dropped.

To allow a drop we must prevent the default handling of the element

Example:

```jsx
function allowDrop(e){
	e.preventDefault();
}
```

What to drag: The `dataTransfer.setData()`  method sets the data type and value of the dragged data.

example:

```jsx
function drag(e){
	e.dataTransfer.setData("text", e.target.id);
}
```