
## Card layout pushing footer down

Whether you use flexbox or [[CSS]] Grid to lay out a list of card components, these layout methods only work on direct children of the flex or grid component. This means that if you have variable amounts of content, the card will stretch to the height of the grid area or flex container. Any content inside uses regular block layout, meaning that on a card with less content the footer will rise up to the bottom of the content rather than stick to the bottom of the card.

<img src="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Typical_Use_Cases_of_Flexbox/flex-cards.png">

Flexbox can solve this. We make the card a flex container, with [`flex-direction`](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-direction)`: column`. We then set the content area to `flex: 1`, which is the shorthand for `flex: 1 1 0` — the item can grow and shrink from a flex basis of `0`. As this is the only item that can grow, it takes up all available space in the flex container and pushes the footer to the bottom. If you remove the `flex` property from the live example you will see how the footer then moves up to sit directly under the content.

![[Pasted image 20230204151618.png]]
![[Pasted image 20230204151654.png]]

