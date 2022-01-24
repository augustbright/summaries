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