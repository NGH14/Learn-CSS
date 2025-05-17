# [width, min-width and max-width](https://www.w3.org/TR/CSS2/visudet.html#min-max-widths)

- [width](https://developer.mozilla.org/en-US/docs/Web/CSS/width): The width CSS property sets an element's width. By default, it sets the width of the content area, but if box-sizing is set to border-box, it sets the width of the border area.
- [min-width](https://developer.mozilla.org/en-US/docs/Web/CSS/min-width): The min-width CSS property sets the minimum width of an element. It prevents the used value of the width property from becoming smaller than the value specified for min-width.
- [max-width](https://developer.mozilla.org/en-US/docs/Web/CSS/max-width):The max-width CSS property sets the maximum width of an element. It prevents the used value of the width property from becoming larger than the value specified by max-width.

## The Conflict Between `min-width` Greater Than `max-width`

___Question___: What is the width of a `section` tag `width: 100px;` `min-width: 150px;` `max-width: 50px;`?

___Answer___: The final width of that section is __`150px`__

Based on [the algorithm in w3c](https://www.w3.org/TR/CSS2/visudet.html#propdef-min-width):

1. The tentative used width is calculated (without 'min-width' and 'max-width') following the rules under "Calculating widths and margins" above.
2. If the tentative used width is greater than 'max-width', the rules above are applied again, but this time using the computed value of 'max-width' as the computed value for 'width'.
3. If the resulting width is smaller than 'min-width', the rules above are applied again, but this time using the value of 'min-width' as the computed value for 'width'.
