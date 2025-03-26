# [SASS Interpolation](https://sass-lang.com/documentation/interpolation/)

> Demonstrates how to use variables within selectors, property names, and other parts of your SASS code for greater flexibility.

```scss
@mixin inline-animation($duration) {
  $name: inline-#{unique-id()};

  @keyframes #{$name} {
    @content;
  }

  animation-name: $name;
  animation-duration: $duration;
  animation-iteration-count: infinite;
}

.pulse {
  @include inline-animation(2s) {
    from { background-color: yellow }
    to { background-color: red }
  }
}
```

## Example

`_interpolation.scss` is the simple implement of interpolation in sass. Run the command below:

```cmd
sass --watch _interpolation.scss style.css
```
