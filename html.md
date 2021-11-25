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
 - set column width:
<th style="width:70%">...</th>

- set column span
<th colspan="2">...</th>

 - collapse borders
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}

```
