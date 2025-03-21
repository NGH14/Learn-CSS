# [SASS Nesting](https://sass-lang.com/guide/#nesting)

> Sass will let you nest your CSS selectors in a way that follows the same visual hierarchy of your HTML. Be aware that overly nested rules will result in over-qualified CSS that could prove hard to maintain and is generally considered bad practice.

```scss
header {
  nav {
    ul {
      margin: 0;
      padding: 0;
      list-style: none;
    }

    li {
      display: inline-block;
    }
  }
}
```

## Example

`_nesting.scss` is the simple implement of nesting in sass. Run the command below:

```cmd
sass --watch _nesting.scss style.css
```
