# CSS Selectors
- Simple selectors (based on name, id, class)
- Combinator selectors (based on specific relationship between elements)
- Pseudo-class selecors (based on certain state of elements)
- Pseudo-elements selectors (part of an alement)
- Atribute selectors (based on attribute or attribute value)

```
  element
  .className
  #element-id
  * - universal selector
  element1, element2
```

# Pseudo-classes
```
:root - root element of DOM (:scope)
:target - element from URL fragment (url#elementId)

:autofill - input autofilled by browser
:invalid - inputs (or other form elements) that failed to validate
:valid - inputs (or other form elements) that validate successfully
:in-range - inputs with value in min/max
:out-of-range - inputs with value outside min/max
:placeholder-shown - inputs, textareas with placeholder visible
:optional - input, select, textarea that is not required
:required - input, select, textarea with attribute required
:checked - radio, cb, option is on
:indeterminate - form elements that are indeterminate
:default - form elements that are the default in a group of related elements
:disabled - elements in disabled state (no click, type or focus)
:read-only - elements that are not editable by user
:read-write - elements that are editable by user
:enabled - may be activated or accept focus

:active
:link - unvisited link
:visited - visited link

:not()
:first-child | :first-of-type
:last-child | :last-of-type
:nth-child() | :nth-of-type()
:nth-last-child() | :nth-last-of-type()
:only-child | :only-of-type

:empty - no child nodes or text
:focus | :focus-visible - focused and is visible by user
:focus-within - element or descendant is focused
:fullscreen - elements currently in full-screen mode
:picture-in-picture - elements currently in picture-in-picture mode
:lang() - elements in given language

@page :first
@page :left
@page :right

:defined - defined elements (built in or custom)
:host()
:host
```

# Pseudo-elements
```
::after(:after) - creates last child of the selected element
::before(:before) - creates first child of the selected element
::backdrop - element behind fullscreen element
::first-letter(:first-letter) - first letter of the first line of a block-level element
::first-line(:first-line) - first line of a block-level element
::placeholder - in input or textarea
::selection - part of the document highlighted by user

::cue - WebVTT cues within a selected element
::slotted()
```
external CSS
  <link rel="stylesheet" href="mystyle.css">

internal CSS
  <style>
    body {
      background-color: linen;
    }

    h1 {
      color: maroon;
      margin-left: 40px;
    }
  </style>

inline CSS
  <h1 style="color:blue;text-align:center;">This is a heading</h1>
  <p style="color:red;">This is a paragraph.</p>
```

# CSS Priorities

When **MULTIPLE** stylesheet,
**LAST** value is used

## Cascade priority (1 - highest)

1. Inline style (inside an HTML element)
2. External and internal style sheets (in the head section)
3. Browser default

# units
```
# Distance
em	Font size of the element.
ex	x-height of the element's font.
cap	Cap height (the nominal height of capital letters) of the element's font.
ch	Average character advance of a narrow glyph in the element’s font, as represented by the “0” (ZERO, U+0030) glyph.
ic	Average character advance of a full width glyph in the element’s font, as represented by the “水” (CJK water ideograph, U+6C34) glyph.
rem	Font size of the root element.
lh	Line height of the element.
rlh	Line height of the root element.
vw	1% of viewport's width.
vh	1% of viewport's height.
vi	1% of viewport's size in the root element's inline axis.
vb	1% of viewport's size in the root element's block axis.
vmin	1% of viewport's smaller dimension.
vmax	1% of viewport's larger dimension.

cm	Centimeters	1cm = 96px/2.54
mm	Millimeters	1mm = 1/10th of 1cm
Q	Quarter-millimeters	1Q = 1/40th of 1cm
in	Inches	1in = 2.54cm = 96px
pc	Picas	1pc = 1/6th of 1in
pt	Points	1pt = 1/72th of 1in
px	Pixels	1px = 1/96th of 1in

# Angle
deg	Degrees	There are 360 degrees in a full circle.
grad	Gradians	There are 400 gradians in a full circle.
rad	Radians	There are 2π radians in a full circle.
turn	Turns	There is 1 turn in a full circle.

# Time
s	Seconds	
ms	Milliseconds	There are 1,000 milliseconds in a second.

# Frequency
Hz	Hertz	Represents the number of occurrences per second.
kHz	KiloHertz	A kiloHertz is 1000 Hertz.

# Resolution
dpi	Dots per inch.
dpcm	Dots per centimeter.
dppx, x	Dots per px unit.

# Percentage
%
```

# types
```
initial - default value
inherit - parent's value
unset - parents or default

<custom-ident>
  - any alphabetical character (A to Z, or a to z),
  - any decimal digit (0 to 9),
  - a hyphen (-),
  - an underscore (_),
  - an escaped character (preceded by a backslash, \),
  - a Unicode character (in the format of a backslash, \, followed by one to six hexadecimal digits, representing its Unicode code point)

<integer>
<number> = <integer> | float
<percentage>
<alpha-value> = <number> | <percentage>
<dimension> = <number> + unit
<ratio> = <integer>/<integer> | <number>/<number>

<display-box> = contents | none
<display-inside> = flow-root | table | flex | grid | exp:flow | exp:ruby
<display-internal> = table-row-group | table-header-group | table-footer-group | table-row | table-cell | table-column-group | table-column | table-caption | exp:ruby-base | exp:ruby-text | exp:ruby-base-container | exp:ruby-text-container
<display-legacy> = inline-block | inline-table | inline-flex | inline-grid
<display-outside> = block | inline

<angle>
  0deg, 90deg, 14.23deg (360)
  0grad, 100grad, 38.8grad (400)
  0rad, 1.0708rad, 6.2832rad (2Pi / 6.28)
  0turn, 0.25turn, 1.2turn (1turn)

<angle-percentage> = <angle> | <percentage>

<basic-shape>
  inset( <shape-arg>{1,4} [round <border-radius>]? )
  circle( [<shape-radius>]? [at <position>]? )
  ellipse( [<shape-radius>{2}]? [at <position>]? )
  polygon( [<fill-rule>,]? [<shape-arg> <shape-arg>]# )
  path( [<fill-rule>,]? <string>)

<color>
  - keyword
  - #hexademical notation
  - rgb(...) / rgba(...) [red green blue]
  - hsl(...) / hsla(...) [hue saturation lightness]
  - hwb(194 0% 0%), hwb(194 0% 0% / .4) [hue whiteness blackness]
  - lch(29.2345% 44.2 27), lch(52.2345% 72.2 56.2 / .5) [lightness chroma hue]
  - lab(29.2345% 39.3825 20.0664), lab(52.2345% 40.1645 59.9971 / .5) [lightness a-axis b-axis]
  - color(display-p3 1 0.5 0 / .5)

<easing-function>
  cubic-bezeir(x1, y1, x2, y2)
    ease
    ease-in
    ease-in-out
    ease-out
  steps(number_of_steps, jump-start | jump-end | jump-both | jump-none | start | end)
 
<filter-function>
  blur() | brightness() | contrast() | drop-shadow() | grayscale() | hue-rotate() | invert() | opacity() | saturate() | sepia()
  
<transform-function>
  matrix() | matrix3d()
  perspective()
  rotate() | rotate3d() | rotateX() | rotateY() | rotateZ()
  scale() | scale3d() | scaleX() | scaleY() | scaleZ()
  skew() | skewX() | skewY()
  translate() | translate3d() | translateX() | translateY() | translateZ()
```

# Gradients
```
linear-gradient( [ <angle> | to <side-or-corner> ]? , <color-stop-list> )
repeating-linear-gradient( [ <angle> | to <side-or-corner> ]? , <color-stop-list> )
radial-gradient( [ <ending-shape> || <size> ]? [ at <position> ]? , <color-stop-list> )
repeating-radial-gradient( [ <ending-shape> || <size> ]? [ at <position> ]? , <color-stop-list> )
conic-gradient( [ from <angle> ]? [ at <position> ]?, <angular-color-stop-list> )
```

# Backgrounds

```
background-color: <color>;
background-image: none/url(...)/image()/image-set()/element()/paint()/cross-fade()/<gradient>;
background-repeat: no-repeat/repeat/repeat-x/repeat-y/revert/round/space;
background-position: center/top right/100px/30% 40%;
background-attachment: scroll/fixed;
background: <color> <image> <repeat> <attachment> <position>;
```

# Borders
```
dotted, dashed, solid, double
groove, ridge, inset, outset
none, hidden
```
