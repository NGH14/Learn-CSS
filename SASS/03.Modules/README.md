# [SASS Modules](https://sass-lang.com/guide/#modules)

> You don’t have to write all your Sass in a single file. You can split it up however you want with the @use rule. This rule loads another Sass file as a module, which means you can refer to its variables, mixins, and functions in your Sass file with a namespace based on the filename. Using a file will also include the CSS it generates in your compiled output!

```scss
// In _base.scss file
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

// In style.scss file
@use 'base';
```

## Example

`_modules.scss` is the simple implement of modules in sass. Run the command below:

```cmd
sass --watch _modules.scss style.css
```
