## form
```
ATTRIBUTES
action="url"		autocomplete="on|off"	accept-charset="utf-8"
method="GET|POST"	novalidate		enctype="..."
target="_blank|iframe"				rel="..."
name="..."

ENC TYPES
text/plain	multipart/form-data 	application/x-www-form-urlencoded

REL
external		 nofollow
next/prev		 opener/noopener
help/license/search	 noreferrer

ELEMENTS
input	select		fieldset
label	textarea	outcome
	datalist
	button
```
## label
```
<label for="field-id">...</label>
```
## input
```
TYPES
button/submit		date		file	text/number/search
radio/checkbox		datetime-local	image	password
reset			month/week		email/tel/url
hidden			time			color
						range
										
ATTRIBUTES
id/name/value			size			multiple
placeholder			maxlength		height/width
readonly/disabled		min/max			formaction
required			pattern			formenctype
autofocus			step			formmethod
autocomplete="on|off"		list			formtarget
form							formnovalidate
```
## select
```
ATTRIBUTES		ELEMENTS
id/name			<option>(value, selected)
size			<optgroup>(label)
multiple
```
## textarea
```
ATTRIBUTES
id/name
rows/cols
```
## datalist
```
ATTRIBUTES	ELEMENTS
id		<option>(value)
```
## fieldset
```
ELEMENTS
<legend>
...form elements
```
