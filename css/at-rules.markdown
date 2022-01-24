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
  [ additive-symbols: <additive-symbols>; ] ||
  [ negative: <negative-symbol>; ] ||
  [ prefix: <prefix>; ] ||
  [ suffix: <suffix>; ] ||
  [ range: <range>; ] ||
  [ pad: <padding>; ] ||
  [ speak-as: <speak-as>; ] ||
  [ fallback: <counter-style-name>; ]
}

@font-face {
  [ font-family: <family-name>; ] ||
  [ src: <src>; ] ||
  [ unicode-range: <unicode-range>; ] ||
  [ font-variant: <font-variant>; ] ||
  [ font-feature-settings: <font-feature-settings>; ] ||
  [ font-variation-settings: <font-variation-settings>; ] ||
  [ font-stretch: <font-stretch>; ] ||
  [ font-weight: <font-weight>; ] ||
  [ font-style: <font-style>; ] ||
  [ size-adjust: <size-adjust>; ] ||
  [ ascent-override: <ascent-override>; ] ||
  [ descent-override: <descent-override>; ] ||
  [ line-gap-override: <line-gap-override>; ]
}
TrueType			font/ttf
OpenType			font/otf
Web Open Font Format		font/woff
Web Open Font Format 2		font/woff2

@font-feature-values <family-name># {
  <feature-value-block-list>
}
where 
<family-name> = <string> | <custom-ident>+
<feature-value-block-list> = <feature-value-block>+

where 
<feature-value-block> = <feature-type> '{' <feature-value-declaration-list> '}'

where 
<feature-type> = @stylistic | @historical-forms | @styleset | @character-variant | @swash | @ornaments | @annotation
<feature-value-declaration-list> = <feature-value-declaration>

where 
<feature-value-declaration> = <custom-ident>: <integer>+;


@import [ <string> | <url> ]
        [ layer | layer(<layer-name>) ]?
        [ supports( [ <supports-condition> | <declaration> ] ) ]?
        <media-query-list>? ;
where 
<supports-condition> = not <supports-in-parens> | <supports-in-parens> [ and <supports-in-parens> ]* | <supports-in-parens> [ or <supports-in-parens> ]*
<media-query-list> = <media-query>#

where 
<supports-in-parens> = ( <supports-condition> ) | <supports-feature> | <general-enclosed>
<media-query> = <media-condition> | [ not | only ]? <media-type> [ and <media-condition-without-or> ]?

where 
<supports-feature> = <supports-decl> | <supports-selector-fn>
<general-enclosed> = [ <function-token> <any-value> ) ] | ( <ident> <any-value> )
<media-condition> = <media-not> | <media-and> | <media-or> | <media-in-parens>
<media-type> = <ident>
<media-condition-without-or> = <media-not> | <media-and> | <media-in-parens>

where 
<supports-decl> = ( <declaration> )
<supports-selector-fn> = selector( <complex-selector> )
<media-not> = not <media-in-parens>
<media-and> = <media-in-parens> [ and <media-in-parens> ]+
<media-or> = <media-in-parens> [ or <media-in-parens> ]+
<media-in-parens> = ( <media-condition> ) | <media-feature> | <general-enclosed>

where 
<complex-selector> = <compound-selector> [ <combinator>? <compound-selector> ]*
<media-feature> = ( [ <mf-plain> | <mf-boolean> | <mf-range> ] )

where 
<compound-selector> = [ <type-selector>? <subclass-selector>* [ <pseudo-element-selector> <pseudo-class-selector>* ]* ]!
<combinator> = '>' | '+' | '~' | [ '||' ]
<mf-plain> = <mf-name> : <mf-value>
<mf-boolean> = <mf-name>
<mf-range> = <mf-name> [ '<' | '>' ]? '='? <mf-value> | <mf-value> [ '<' | '>' ]? '='? <mf-name> | <mf-value> '<' '='? <mf-name> '<' '='? <mf-value> | <mf-value> '>' '='? <mf-name> '>' '='? <mf-value>

where 
<type-selector> = <wq-name> | <ns-prefix>? '*'
<subclass-selector> = <id-selector> | <class-selector> | <attribute-selector> | <pseudo-class-selector>
<pseudo-element-selector> = ':' <pseudo-class-selector>
<pseudo-class-selector> = ':' <ident-token> | ':' <function-token> <any-value> ')'
<mf-name> = <ident>
<mf-value> = <number> | <dimension> | <ident> | <ratio>

where 
<wq-name> = <ns-prefix>? <ident-token>
<ns-prefix> = [ <ident-token> | '*' ]?  | 
<id-selector> = <hash-token>
<class-selector> = '.' <ident-token>
<attribute-selector> = '[' <wq-name> ']' | '[' <wq-name> <attr-matcher> [ <string-token> | <ident-token> ] <attr-modifier>? ']'

where 
<attr-matcher> = [ '~' |  |  | '^' | '$' | '*' ]? '='
<attr-modifier> = i | s

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