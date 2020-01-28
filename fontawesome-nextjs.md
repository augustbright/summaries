# Fontawesome with NextJS

--------------------------------------

1. Setup SASS loading (@zeit/next-sass)
2. Add fontawesome free:

```npm i --save @fortawesome/fontawesome-free```

3. move **webfonts** to your public directory
4. import fontawesome styles:

```
/* main.scss */

@import "~@fortawesome/fontawesome-free/scss/fontawesome";
$fa-font-path: "/webfonts";
@import "~@fortawesome/fontawesome-free/scss/solid";

/* ... */

```

5. Use fontawesome free icons:

```html
<i className="fas fa-lg fa-mobile-alt" />
```