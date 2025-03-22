# [SASS Mixins](https://sass-lang.com/guide/#mixins)

> Some things in CSS are a bit tedious to write, especially with CSS3 and the many vendor prefixes that exist. A mixin lets you make groups of CSS declarations that you want to reuse throughout your site. It helps keep your Sass very DRY. You can even pass in values to make your mixin more flexible. Here’s an example for theme.

- The `@mixin` directive create CSS code that reused.

- The `@include` directive create to use the created mixin.

```scss
@mixin flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

main {
@include flex-center;
}
```

## Example

`_mixins.scss` is the simple implement of mixins in sass. Run the command below:

```cmd
sass --watch _mixins.scss style.css
```
