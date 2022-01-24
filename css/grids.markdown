# terminology
- grid container/grid item
- grid line/grid cell
- grid track/grid area

# container properties
```
	display: grid/inline-grid;
	grid-template-columns/grid-template-rows: 1fr minmax(10px, 1fr) repeat(5, 1fr) 50px auto
	grid-template-areas: "<grid-area-name> | . | none | ..."
	grid-template: none | <grid-template-rows> / <grid-template-columns>;
	column-gap/row-gap/grid-column-gap/grid-row-gap: <line-size>
	gap: <grid-row-gap> <grid-column-gap>
	justify-items: start | end | center | stretch;
	align-items: start | end | center | stretch;
	place-items: start | end | center | stretch;
	justify-content: start | end | center | stretch | space-around | space-between | space-evenly;
	align-content: start | end | center | stretch | space-around | space-between | space-evenly;
	place-content: align-content: start | end | center | stretch | space-around | space-between | space-evenly;
	grid-auto-columns, grid-auto-rows: <track size> ...
	grid-auto-flow: row | column | row dense | column dense;
	
	grid: [row1-start] "header header header" 1fr [row1-end]
        [row2-start] "footer footer footer" 25px [row2-end]
        / auto 50px auto;
```

# item properties
```
	grid-column-start: <number> | <name> | span <number> | span <name> | auto;
	grid-column-end: <number> | <name> | span <number> | span <name> | auto;
	grid-row-start: <number> | <name> | span <number> | span <name> | auto;
	grid-row-end: <number> | <name> | span <number> | span <name> | auto;

	grid-column: <start-line> / <end-line> | <start-line> / span <value>;
	grid-row: <start-line> / <end-line> | <start-line> / span <value>;
	
	grid-area: <name> | <row-start> / <column-start> / <row-end> / <column-end>;
	
	justify-self: start | end | center | stretch;
	align-self: start | end | center | stretch;
	place-self: start | end | center | stretch;
	
SIZING KEYWORDS
	min-content, max-content, fit-content, auto, fr

SIZING FUNCTIONS
	minmax(), min(), max()
```
