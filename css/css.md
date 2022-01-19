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

# Backgrounds

```
background-color: <color>;
background-image: url("/path/to/image");
```
