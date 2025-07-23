# @function vs @mixin vs @extend

|           | return           | reuse scenario                            | dynamic                            |
| --------- | ---------------- | ----------------------------------------- | ---------------------------------- |
| @function | value            | reuse it on **different CSS properties**. | caculation and return value        |
| @mixin    | block style rule | reuse it on **same CSS properties**       | flexible value in same properties  |
| @extend   | block style rule | reuse it on **same CSS properties**       | reuse the same block of style rule |

`@function` useful specifically because they _return_ values so that reuse in different `CSS` properties like `min-width` and `width` below

```scss
@function caculated-width($width, $padding) {
  @return $width + $padding;
}

.sm {
  min-width: caculated-width(600px, 30px);
}

.m {
  width: caculated-width(300px, 30px);
}
```

`@mixin` are nothing like functions. they usually just provide valuable blocks of code.

```scss

@mixin caculated-width($width, $padding) {
  min-width: $width;
  padding: $padding;
}

.foo {
  @include caculated-width(300px, 30px);
}

```

`@extend` are same with `@mixin` but not support arguments And usage when one class should have all the styles of another class, as well as its own specific styles.

```scss
%message-shared {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.message {
  @extend %message-shared;
}

.success {
  @extend %message-shared;
  border-color: green;
}

.error {
  @extend %message-shared;
  border-color: red;
}

.warning {
  @extend %message-shared;
  border-color: yellow;
}
```

and [`unlike @mixin`](https://sass-lang.com/documentation/at-rules/extend/#how-it-works) are copy the block style rule and paste into the current style. the `@extend` updates style rules that contain the ==extended selector== so that they contain the extending selector as well - in other hand, the `@extend` could be assumed to extend the group of CSS selectors of the same style rule.

- `@extend`

```scss
%message-shared {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.message {
  @extend %message-shared;
}

.success {
  @extend %message-shared;
  border-color: green;
}

.error {
  @extend %message-shared;
  border-color: red;
}

.warning {
  @extend %message-shared;
  border-color: yellow;
}
```

The `CSS (Compiled)`

```scss
.warning, .error, .success, .message {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.success {
  border-color: green;
}

.error {
  border-color: red;
}

.warning {
  border-color: yellow;
}
```

- `@mixin`

```scss
@mixin message-shared {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.message {
  @include  message-shared;
}

.success {
  @include message-shared;
  border-color: green;
}

.error {
  @include message-shared;
  border-color: red;
}

.warning {
  @include message-shared;
  border-color: yellow;
}
```

The `CSS (Compiled)`

```css
.message {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.success {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
  border-color: green;
}

.error {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
  border-color: red;
}

.warning {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
  border-color: yellow;
}
```

- ref:
  - https://sass-lang.com/documentation/at-rules/extend/#how-it-works
  - https://sass-lang.com/documentation/at-rules/mixin/
  - https://sass-lang.com/documentation/at-rules/function/