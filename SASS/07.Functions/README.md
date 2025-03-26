# [SASS Function](https://sass-lang.com/documentation/at-rules/function/)

>Functions allow you to define complex operations on [SassScript values](https://sass-lang.com/documentation/values) that you can re-use throughout your stylesheet. They make it easy to abstract out common formulas and behaviors in a readable way.

```scss
@function invert($color, $amount: 100%) {
  $inverse: change-color($color, $hue: hue($color) + 180);
  @return mix($inverse, $color, $amount);
}

$primary-color: #036;
.header {
  background-color: invert($primary-color, 80%);
}
```

## Example

`_functions.scss` is the simple implement of functions in sass. Run the command below:

```cmd
sass --watch _functions.scss style.css
```
