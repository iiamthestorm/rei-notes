
## Box Model
Box Model adalah paradigma penting dalam [[CSS]].
-   `padding` increases the space between the edge of a box and the content inside of it.
-   `margin` increases the space between a box and any others that sit next to it.
-   `border` adds space (even if it’s only a pixel or two) between the margin and the padding.
<img src="https://cdn.statically.io/gh/TheOdinProject/curriculum/main/foundations/html_css/the-box-model/imgs/box-model.png">

-   The [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width) and [`height`](https://developer.mozilla.org/en-US/docs/Web/CSS/height) properties are respected.
-   Padding, margin and border will cause other elements to be pushed away from the box.
-   If [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width) is not specified, the box will extend in the inline direction to fill the space available in its container. In most cases, the box will become as wide as its container, filling up 100% of the space available.
