# at-rules

## conditional
```
	@media
	@supports
	@document
```

## nested
```
	@media
	@supports
	@page
	@font-face
	@keyframes
	@counter-style
	@font-feature-values (plus @swash, @ornaments, @annotation, @stylistic, @styleset and @character-variant)
	@property
	@color-profile
```

```
@charset "utf-8"; / @charset "iso-8859-15"; / ...
// Should be placed at the beginning of stylesheet file

@color-profile --swop5c
// background: color(--swop5c 0% 70% 20% 0%)

@counter-style <counter-style-name> {
  [ system: <counter-system>; ] ||
  [ symbols: <counter-symbols>; ] ||
	...
}

@font-face {
  [ font-family: <family-name>; ] ||
  [ src: <src>; ] ||
  [ font-variant: <font-variant>; ] ||
  [ font-stretch: <font-stretch>; ] ||
  [ font-weight: <font-weight>; ] ||
  [ font-style: <font-style>; ] ||
	...
}
TrueType			font/ttf
OpenType			font/otf
Web Open Font Format		font/woff
Web Open Font Format 2		font/woff2

@font-feature-values <family-name># {
  <feature-value-block-list>
}
<feature-type> = @stylistic | @historical-forms | @styleset | @character-variant | @swash | @ornaments | @annotation

@import [ <string> | <url> ]
        [ layer | layer(<layer-name>) ]?
        [ supports( [ <supports-condition> | <declaration> ] ) ]?
        <media-query-list>? ;

@keyframes <keyframes-name> {
 from {}
 to {}
 <percentage> {}
}

@media <media-query-list> {
  <group-rule-body>
}

MEDIA TYPES
all
print
screen

MEDIA FEATURES
width/height
aspect-ratio
orientation
resolution

color
color-gamut
color-index
forced-colors
inverted-colors
monochrome
prefers-contrast
prefers-reduced-motion
prefers-color-scheme

pointer
hover
any-pointer
any-hover

overflow-block
overflow-inline
display-mode
grid
scripting
update

MEDIA OPERATORS
and not only comma(,)

@namespace url(http://www.w3.org/1999/xhtml);
@namespace svg url(http://www.w3.org/2000/svg);

@page <page-selector-list> {
  <page-body>
}
:blank
:first
:left
:right
:recto 
:verso

@property <custom-property-name> {
  <declaration-list>
}

@supports <supports-condition> {
  <group-rule-body>
}
```