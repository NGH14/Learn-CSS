# Sass Variables vs CSS Variables

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

## Conclusion

- CSS Variables: runtime flexibility, dynamic, JavaScript interaction. According to [CANIUSE](https://caniuse.com/css-variables), `96.89%` CSS Variables supported in global brownsers.

![CSS Variable in caniuse 2025](<CSSVariable(Caniuse).png>)

- SASS Variables: powerful compile-time logic, better code organization, or needed to compatibility with very very older browsers.
