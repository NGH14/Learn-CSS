# [SASS Operators](https://sass-lang.com/guide/#operators)

> Doing math in your CSS is very helpful. Sass has a handful of standard math operators like +, -, \*, math.div(), and %. In our example we’re going to do some simple math to calculate widths for an article and aside.

```scss
main {
  padding: 10px == 10px; // true
  margin: 10px < 17px; // true
  width: math.div(600px, 960px) * 100%; //  width: 62.5%;
}
```

## Example

`_operators_.scss` is the simple implement of operator in sass. Run the command below:

```cmd
sass --watch _operators.scss style.css
```
