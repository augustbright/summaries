# terminology
- flex container/flex item
- main size/cross size
- main start/cross start
- main end/cross end
- main axis/cross axis

# container properties
```
	display: flex / inline-flex;
	flex-direction: row | row-reverse | column | column-reverse;
	flex-wrap: nowrap | wrap | wrap-reverse;
	flex-flow: column wrap;
	justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly | start | end | left | right ... + safe | unsafe;
	align-items: stretch | flex-start | flex-end | center | baseline | first baseline | last baseline | start | end | self-start | self-end + ... safe | unsafe;
	align-content: flex-start | flex-end | center | space-between | space-around | space-evenly | stretch | start | end | baseline | first baseline | last baseline + ... safe | unsafe;
	gap, row-gap, column-gap;
```
# item properties
```
	order: 5; /* default is 0 */
	flex-grow: 4; /* default 0 */
	flex-shrink: 3; /* default 1 */
	flex-basis: 10px | auto; /* default auto */
	flex: <grow shrink basis> | none
	align-self: auto | flex-start | flex-end | center | baseline | stretch;
```