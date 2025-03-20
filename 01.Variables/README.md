# [SASS Variables](https://sass-lang.com/guide/#variables)

> Think of variables as a way to store information that you want to reuse throughout your stylesheet. You can store things like colors, font stacks, or any CSS value you think you’ll want to reuse. Sass uses the $ symbol to make something a variable.

## Example

Simple example for SASS Variable

**_SCSS_**

```scss
$text-color: #fafbfa;
body {
  color: $primary-color;
}
```

**_CSS_**

```css
body {
  color: #fafafa;
}
```

## Sass Variables vs CSS Variables

| Feature                             | **Sass Variables** (`$var`)     | **CSS Variables** (`--var`) |
| ----------------------------------- | ------------------------------- | --------------------------- |
| **Evaluated at**                    | Compile-time                    | Runtime                     |
| **Dynamic at runtime**              | ❌                              | ✅                          |
| **Scoped**                          | ❌                              | ✅ (`:root`, etc.)          |
| **Browser support**                 | ✅ All (after compile)          | ❌ IE11 support             |
| **JavaScript access**               | ❌                              | ✅                          |
| **Media query support**             | ❌                              | ✅                          |
| **Functions & logic**               | ✅ (loops, conditionals)        | ❌                          |
| **Visible in DevTools**             | ❌                              | ✅                          |
| **Theming support**                 | ⚠️ Only with compile-time logic | ✅ Easy runtime theming     |
| **Math support**                    | ✅ Full                         | ⚠️ Limited (`calc()` only)  |
| **Interpolation (e.g. in classes)** | ✅                              | ❌                          |

### Conclusion

- CSS Variables:  runtime flexibility, dynamic, JavaScript interaction. According to [CANIUSE](https://caniuse.com/css-variables), `96.89%` CSS Variables supported in global nrownsers.

![CSS Variable in caniuse 2025](CSSVariable(Caniuse).png)

- SASS Variables: powerful compile-time logic, better code organization, or needed to compatibility with very very older browsers.
