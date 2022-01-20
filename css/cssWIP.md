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

# Colors
```
  - keyword
  - #hexademical notation
  - rgb(...) / rgba(...) [red green blue]
  - hsl(...) / hsla(...) [hue saturation lightness]
  - hwb(194 0% 0%), hwb(194 0% 0% / .4) [hue whiteness blackness]
  - lch(29.2345% 44.2 27), lch(52.2345% 72.2 56.2 / .5) [lightness chroma hue]
  - lab(29.2345% 39.3825 20.0664), lab(52.2345% 40.1645 59.9971 / .5) [lightness a-axis b-axis]
  - color(display-p3 1 0.5 0 / .5)
```

# Gradients
```
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
