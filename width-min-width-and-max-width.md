# [width, min-width and max-width](https://www.w3.org/TR/CSS2/visudet.html#min-max-widths)

- [width](https://developer.mozilla.org/en-US/docs/Web/CSS/width): The width CSS property sets an element's width. By default, it sets the width of the content area, but if box-sizing is set to border-box, it sets the width of the border area.
- [min-width](https://developer.mozilla.org/en-US/docs/Web/CSS/min-width): The min-width CSS property sets the minimum width of an element. It prevents the used value of the width property from becoming smaller than the value specified for min-width.
- [max-width](https://developer.mozilla.org/en-US/docs/Web/CSS/max-width):The max-width CSS property sets the maximum width of an element. It prevents the used value of the width property from becoming larger than the value specified by max-width.

## The Conflict Between min-width over max-width

- Question: What is the width of a div element `width: 100px;` `min-width: 150px;` `max-width: 50px;`?


