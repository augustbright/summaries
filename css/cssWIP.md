# types
```
initial - default value
inherit - parent's value
unset - parents or default

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
