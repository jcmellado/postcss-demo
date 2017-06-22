
# PostCSS demo

## Installation

```bash
git clone https://github.com/jcmellado/postcss-demo

cd postcss-demo

npm install
```

## Execution

```bash
npm run build
```

## Examples

### cssnano

Tool written on top of the PostCSS ecosystem, which allows us to use a lot of powerful features in order to compact CSS appropriately.

https://github.com/ben-eb/cssnano


### postcss-cssnext

PostCSS plugin that helps you to use the latest CSS syntax today. It transforms CSS specs into more compatible CSS so you don’t need to wait for browser support.

https://github.com/MoOx/postcss-cssnext

```css
:root {
  --badge: {      /* Custom properties set */
    width: 50px;
    height: 50px;
  };
  --badge-color: #D4AF37;   /* Custom property */
}

.badge {
  @apply --badge;                 /* Custom properties set reference */
  background: var(--badge-color);  /* Custom property reference */
}
```

### postcss-color-function

PostCSS plugin to transform W3C CSS color function to more compatible CSS.

https://github.com/postcss/postcss-color-function

```css
body {
  background: color(red a(90%))

  color: color(blue w(+ 20%) s(+ 20%))
}
```

### postcss-font-magician

PostCSS plugin that magically generates all of your @font-face rules. Never write a @font-face rule again.

https://github.com/jonathantneal/postcss-font-magician

```css
body {
  font-family: "Alice";
}
```

### postcss-inline-svg

PostCSS plugin to reference an SVG file and control its attributes with CSS syntax.

https://github.com/TrySound/postcss-inline-svg

```css
@svg-load nav url(img/nav.svg) {
    fill: #cfc;
    path:nth-child(2) {
        fill: #ff0;
    }
}
.nav {
    background: svg-inline(nav);
}
.up {
    background: svg-load('img/arrow-up.svg', fill=#000, stroke=#fff);
}
```

### lost

Powerful grid system built in PostCSS that works with any preprocessor and even vanilla CSS.

https://github.com/peterramsing/lost

```css
@lost flexbox flex;

section {
  lost-center: 980px;
}

div {
  lost-column: 1/3;
}
```
