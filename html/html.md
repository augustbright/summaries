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

# Forms
```html
	<form
		action="/action_page.php"
		target="_black/_self/.../framename"
		method="GET/POST"
		autocomplete="on/off"

		novalidate
		
		accept-charset="utf-8"
		name="myForm"	// is used to reference elements in a JavaScript, or to reference form data after a form is submitted

		// can be used only if method="post".
		enctype="application/x-www-form-urlencoded"
		enctype="multipart/form-data"
		enctype="text/plain"
		
		rel="external"	// Specifies that the referenced document is not a part of the current site
		rel="help"	// Links to a help document
		rel="license"	// Links to copyright information for the document
		rel="next"	// The next document in a selection
		rel="nofollow"	// Links to an unendorsed document, like a paid link.
		// ("nofollow" is used by Google, to specify that the Google search spider should not follow that link)
		rel="noopener"	 
		rel="noreferrer"	// Specifies that the browser should not send a HTTP referrer header if the user follows the hyperlink
		rel="opener"	 
		rel="prev"	// The previous document in a selection
		rel="search"	// Links to a search tool for the document
	>
		<label for="field-id">label: </label>	// when the user clicks the text within the <label> element, it toggles the radio button/checkbox
		<input name="field-name" id="field-id" type="text">	Displays a single-line text input field

		<select
			id="cars"
			name="cars"
			
			size="3" // number of visible elements
			multiple // ?cars=volvo&cars=saab&cars=fiat
		>
			<option value="fiat">Fiat</option>
			<option value="audi">Audi</option>

			<optgroup label="Swedish Cars">	// group related options in a <select> element

				<option value="volvo">Volvo</option>
				<option
					value="saab"
					selected // predefined selected option
				>Saab</option>
			</optgroup>
		</select>

		<textarea
			name="message"

			rows="10"
			cols="30"
			style="width:200px; height:600px;"
		>
			The cat was playing in the garden.
		</textarea>
		
		<button type="button" onclick="alert('Hello World!')">Click Me!</button>

		<fieldset>	// group related data in a form
			<legend>Personalia:</legend>	// defines a caption for the <fieldset> element.

			<label for="fname">First name:</label><br>
			<input type="text" id="fname" name="fname" value="John"><br>
			<label for="lname">Last name:</label><br>
			<input type="text" id="lname" name="lname" value="Doe"><br><br>
		</fieldset>

		// list of pre-defined options for an <input> element
		<input name="browser" list="browsers">	// The list attribute of the <input> element, must refer to the id attribute of the <datalist> element
		<datalist id="browsers">
			<option value="Internet Explorer">
			<option value="Firefox">
			<option value="Chrome">
			<option value="Opera">
			<option value="Safari">
		</datalist>
		
		// represents the result of a calculation (like one performed by a script)
		<output name="x" for="a b"></output>
		
		<input type="password">	// defines a password field
		<input type="button">	// defines a button
		<input type="radio">	// defines a radio button
		<input type="color">	// color picker
		<input type="date">	// date
		<input type="datetime-local">	// datetime, without TZ
		<input type="month">	// a month and year
		<input type="time">	// time, without TZ
		<input type="week">	// a week and year
		<input type="email">	// email
		<input type="file">	// defines a file-select field and a "Browse" button for file uploads
		<input type="image">
		<input type="number">	// defines a numeric input field
		<input type="range" id="vol" name="vol" min="0" max="50">	// defines a control for entering a number whose exact value is not important (like a slider)
		<input type="search">	// is used for search fields (a search field behaves like a regular text field)
		<input type="tel">	// is used for input fields that should contain a telephone number
		<input type="url">	// is used for input fields that should contain a URL address

		<input type="hidden">	// defines a hidden input field (not visible to a user)

		<input type="reset">	// defines a reset button that will reset all form values to their default values
		<input type="submit">	// Displays a submit button (for submitting the form)
		
		<input
			value="initial value"
			readonly	// cannot be modified (however, a user can tab to it, highlight it, and copy the text from it)
			disabled	// unusable and un-clickable, not sent!
			size="20"	// the visible width, in characters, of an input field (text, search, tel, url, email, and password)
			maxlength="10"	// the maximum number of characters allowed in an input field
			min/max="10"	// minimum and maximum values for an input field (number, range, date, datetime-local, month, time and week)
			multiple	// email and file
			pattern="[A-Za-z]{3}"	// a regular expression that the input field's value is checked against, when the form is submitted (text, date, search, url, tel, email, and password)
			placeholder="foo"	// short hint that describes the expected value of an input field
			required	// must be filled out before submitting the form
			step="2"	// legal number intervals for an input field (number, range, date, datetime-local, month, time and week)
			autofocus	// input field should automatically get focus when the page loads
			height/width="200"	// for image input
			list="list-id"	// refers to a <datalist> element that contains pre-defined options for an <input> element
			autocomplete="on/off"	// input field should have autocomplete on or off (text, search, url, tel, email, password, datepickers, range, and color)
			form="form-id"	// the form the <input> element belongs to

			formaction="/url"	// overrides the action attribute of the <form> element (image, submit)
			formenctype="multipart/form-data"	// overrides the enctype attribute of the <form> element (image, submit)
			formmethod="GET/POST"	// overrides the method attribute of the <form> element (image, submit)
			formtarget="_blank"	// overrides the target attribute of the <form> element (image, submit)
			formnovalidate		// overrides the novalidate attribute of the <form> element (submit)
		/>
	</form>
	
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
