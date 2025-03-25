# SASS/SCSS Nesting vs CSS Nesting

| Feature                    | **SASS\***             | **CSS**           |
| -------------------------- | ---------------------- | ----------------- |
| **Evaluated at**           | Compile-time           | Runtime by `is()` |
| **Browser support**        | ✅ All (after compile) | 90.82%            |
| **Suffix Parent Selector** | ✅                     | ❌                |

## Suffix Parent Selector

> Sass nesting and native CSS nesting both support syntax that looks like &foo, but it means different things. In Sass, this adds a suffix to the parent selector.

- SCSS Suffix:

```scss
.class {
  &-suffix {
    /* ... */
  }
}
```

- CSS:

```css
.foo-suffix {
  /* ... */
}
```

## Resource

- [Sass and Native Nesting Document](https://sass-lang.com/blog/sass-and-native-nesting/)

- CSS Nesting: [CANIUSE CSS NESTING](https://caniuse.com/css-nesting), `90.82%` CSS Nesting supported in global brownsers.

![CSS Nesting in caniuse 2025](<CSS_Nesting(caniuse).png>)

[Suffix to the parent selector]{#suffix}
