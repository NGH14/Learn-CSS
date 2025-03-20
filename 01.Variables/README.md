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

Absolutely! Here's a more detailed comparison between **Sass variables** and **CSS variables** in table form:

---

### 🧠 Sass Variables vs CSS Variables — Full Comparison Table

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
