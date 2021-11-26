# <!Doctype>
[Doctypes elements table](https://www.w3schools.com/tags/ref_html_dtd.asp)
```markdown
# HTML5
<!DOCTYPE html>
<!Doctype html>
<!doctype html>

# HTML4
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">

# XHTML
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
```

# Head
```
contains:
 <title> - for browser tab/favorite/search engines results
 <style>
 <meta>
 <link>
 <script>
 <base>
```

# Meta
```
 <meta charset="UTF-8">
 
 name="keywords" content="HTML, CSS, JavaScript"
 name="description" content="Free Web tutorials"
 name="author" content="John Doe"
 name="viewport" content="width=device-width, initial-scale=1.0"
 
 http-equiv="refresh" content="30"
```

# Base
```
 <base href="https://www.w3schools.com/" target="_blank">
```

# Paths
```
// better
picture.jpg -	current folder
images/picture.jpg -	images in current folder
/images/picture.jpg -	images in root folder
../picture.jpg - folder up

// worse
https://www.w3schools.com/images/picture.jpg - absolute
```

# Elements
[HTML Tag Reference](https://www.w3schools.com/tags/default.asp)

# Attributes
[HTML Attributes Reference](https://www.w3schools.com/tags/ref_attributes.asp)
```markdown
- <html lang="en"> - To assist search engines and browsers
- Use alt atribute
- Avoid absolute src paths
- Use title attribute or custom titles for tooltips 
- Use lowercase attributes (HTML - W3C recommendation, XHTML - W3C demand)
- Quote attribute values (HTML - W3C recommendation, XHTML - W3C demand)
- double-quotes and single-quotes are ok, but double-quites are more common.
```

# Comments
```
<!-- Write your comments here -->
```

# CSS
```
 - inline - style attribute
 - internal - <style> tag in <head> seaction
 - external - <link> tag to external CSS file

# example

internal
<style>
 body {background-color: powderblue;}
 h1   {color: blue;}
 p    {color: red;}
</style>

external
 - full url - <link rel="stylesheet" href="https://www.w3schools.com/html/styles.css">
 - relative url - <link rel="stylesheet" href="/html/styles.css">
 - same folder - <link rel="stylesheet" href="styles.css">
```

# Color
[HTML Standard Color Names](https://www.w3schools.com/colors/colors_names.asp)
```
 - RGB - rgb(red, green, blue) - rgb(256, 256, 256)
 - HEX - #RRGGBB - #000000-#FFFFFF 
 - HSL - hsl(hue, saturation, lightness) - hsl(9, 100%, 64%)
   - hue - position of color wheel
   - saturation (0% - shade of gray, 100% - color)
   - lightness (0% - black, 100% white)
 - RGBA - rgba(red, green, blue, alpha) - rgba(256, 256, 256, 0.5)
 - HSLA - hsla(hue, saturation, lightness, alpha) hsla(9, 100%, 64%, 0.5)
 
 - alpha
  0 - transparent
  1 - non-transparent
```

# Entities
[Full Emojis Ref](https://www.w3schools.com/charsets/ref_emoji.asp)
[Full Symbols Ref](https://www.w3schools.com/charsets/ref_utf_symbols.asp)
[Full Arrows Ref](https://www.w3schools.com/charsets/ref_utf_arrows.asp)
[Full Currency Ref](https://www.w3schools.com/charsets/ref_utf_currency.asp)
```
	non-breaking space	&nbsp;	&#160;	
<	less than	&lt;	&#60;	
>	greater than	&gt;	&#62;	
&	ampersand	&amp;	&#38;	
"	double quotation mark	&quot;	&#34;	
'	single quotation mark (apostrophe)	&apos;	&#39;
©	copyright	&copy;	&#169;	
®	registered trademark	&reg;	&#174;
```

# Semantics
```
 - <article> - independent, self-contained content
 - <aside> - some content aside from the content it is placed in (like a sidebar)
 - <footer> - a footer for a document or section
 - <header> - container for introductory content or a set of navigational links
 - <main> - main content of a document
 - <mark> - marked/highlighted text
 - <nav> - a set of navigation links
 - <section> -  a thematic grouping of content, typically with a heading 
 - <time> - a date/time
 
 - <details> - additional details that the user can view or hide
 - <summary> - a visible heading for a <details> element
 
 - <figcaption> - a caption for a <figure> element
 - <figure> - self-contained content, like illustrations, diagrams, photos, code listings, etc
```

# Formatting
```
 <b> - Bold text
 <strong> - Important text
 <i> - Italic text
 <em> - Emphasized text
 <mark> - Marked text
 <small> - Smaller text
 <del> - Deleted text
 <ins> - Inserted text
 <sub> - Subscript text
 <sup> - Superscript text
```
# Quotations
```
 <blockquote cite="source"> indented block of quote
 <q> - inline short quote
 <abbr title="full"> - inline abbreviations
 <address> - author/owner contact information
 <cite> - the title of a creative work
 <bdo dir="rtl"> - bi-directional override
```

# Headings
```
<h1> to <h6>
For search engines and usability.

# example
<h1>This is heading 1</h1> - most important
...
<h6>This is heading 6</h6> - least important
```

# Paragraphs
```
- Always starts on a new line
- Browser adds margins before and after
- Browser automatically removes extra whitespaces and new lines

# <hr> Horizontal Rule
 - Defines a thematic break
 - Used to separate content
 - Displayed as a horizontal line

# <br> Line break
 - a new line without starting a new paragraph

# <pre> - Display preformatted text (keep spaces and line breaks)

# example
<p>This is a paragraph.</p>
<p>This is another paragraph.</p>
```

# Links
```
 - href
 - target
   _self - Default. Opens the document in the same window/tab as it was clicked
   _blank - Opens the document in a new window or tab
   _parent - Opens the document in the parent frame
   _top - Opens the document in the full body of the window
   iframe_name = Opens the document in an iframe

- unvisited - blue (:link)
- visited - purple (:visited)
- active - red (:active)
- hover - (:hover)

# example
 - absolute - <a href="https://www.google.com/">Google</a>
 - relative - <a href="/css/default.asp">CSS Tutorial</a>
 - relative, same page - <a href="html_images.asp">HTML Images</a>
 - to email - <a href="mailto:someone@example.com">Send email</a>
 - button as link - <button onclick="document.location='default.asp'">HTML Tutorial</button>
 
 - bookmark - <a href="#C4">Jump to Chapter 4</a> (C4 - id of an element)
```

# Images
```
 - empty tag

 - src - source file
   - absolute (uncontrollable, copyright laws)
   - relative
 - alt - alternative text - for errors/slow connection/screen readers
 
 - width - in pixels - not recommended (consider style)
 - height - in pixels - not recommended
 
 - APNG -	Animated Portable Network Graphics -	.apng
 - GIF - Graphics Interchange Format -	.gif
 - ICO -	Microsoft Icon -	.ico, .cur
 - JPEG - Joint Photographic Expert Group image -	.jpg, .jpeg, .jfif, .pjpeg, .pjp
 - PNG -	Portable Network Graphics -	.png
 - SVG - Scalable Vector Graphics -	.svg

 - <img> -	Defines an image (usemap="#mapname")
 - <map> -	Defines an image map (name="mapname")
 - <area> -	Defines a clickable area inside an image map (shape="rect/circle/poly/default" coords="coords" href/onclick)
 - <picture> -	Defines a container for multiple image resources (media="(min-width: 650px)" srcset="img_food.jpg")

# example
<img src="w3schools.jpg" alt="W3Schools.com" width="104" height="142">

<img src="workplace.jpg" alt="Workplace" usemap="#workmap">
<map name="workmap">
  <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm">
  <area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.htm">
  <area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.htm">
</map>

<picture>
  <source media="(min-width: 650px)" srcset="img_food.jpg">
  <source media="(min-width: 465px)" srcset="img_car.jpg">
  <img src="img_girl.jpg">
</picture>
```

# Favicon
[https://favicon.cc/](Create a favicon)
```
<link rel="icon" type="image/x-icon" href="/images/favicon.ico">
formats: ICO	PNG	GIF	JPEG	SVG
```

# Tables
```
 <table>
 <tr> - table row
 <td> - table data
 <th> - table header (bold+centered)
 
 <caption>
 <colgroup>
 <col>

 <thead>
 <tbody>
 <tfoot>
 
# examples
<table>
 <caption>...</caption>
 <tr>
  <th>...</th>
  <td>...</td>
 </tr>
</table>


 - set column width:
<th style="width:70%">...</th>

- set column span
<th colspan="2">...</th>
- set row span
<th rowspan="2">...</th>

 - collapse borders
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}

```

# Lists
```
 list-style-type: disc/circle/square/none

 <ul>	- unordered list
 <ol>	- ordered list (type = 1/A/a/I/i, start=50)
 <li>	- list item

 <dl>	- description list
 <dt> -	description term
 <dd> -	description definition
```

# IFrames
```
 - nested Browsing Context
 - own Session History

 # basic
 <iframe src="url" title="description"></iframe>
 
 # Link for iframe
 <iframe src="demo_iframe.htm" name="iframe_a" title="Iframe Example"></iframe>
 <a href="https://www.w3schools.com" target="iframe_a">W3Schools.com</a></p>

```

# Computercode
```
 - <kbd> - keyboard input
 - <samp> - sample output from a computer program
 - <code> - a piece of computer code
 - <var> - a variable in programming or in a mathematical expression
 - <pre> - preformatted text
```

# HTML vs XHTML
```
 - <!DOCTYPE> is mandatory
 - The xmlns attribute in <html> is mandatory
 - <html>, <head>, <title>, and <body> are mandatory
 - Elements must always be properly nested
 - Elements must always be closed
 - Elements must always be in lowercase
 - Attribute names must always be in lowercase
 - Attribute values must always be quoted
 - Attribute minimization is forbidden
```
