
---
# Box Positioning

[Back to index](../index.md)

---
## Box Model

- Each html element creates a box.
- Box are made from (inside out):
	- `content` is the actual contents of the element (usually text).
	- `padding` is the spacing between the content and border.
	- `border` is a line that encloses the content and padding
	- `margin` is the spacing between this element and another ones.
- Two ways of calculating
	- `box-sizing: content-box;`
		- `width` and `height` modify `contents`.
		- default behaviour.
	- `box-sizing: border-box;`
		- `width` and `height` modify `contents` + `padding` + `border`.

---
## Box position

```css
.something {
	position: /* value */;
	
	/* OPTIONAL */
	
	top: /* unit */;
	bottom: /* unit */;
	right: /* unit */;
	left: /* unit */;
}
```

- `absolute`
	- Is Independent from other elements.
	- Position is absolute to the document.
- `relative`
	- Is contain in another element.
	- Position is relative to the container element.
- `fixed`
	- Is Independent from other elements.
	- Position is fixed in the screen.
- `sticky`
	- Is contain in another element.
	- Position is stick to the screen on scrolling.

---
## Box display
```css
.container {
	display: /* value */;
}
```

- `block` displays element as a block (default).
- `inline` displays element as a inline element.
- `flex` displays element as a flex block element.
- `inline-flex` displays element as a inline flex element.
- `grid` displays element as a grid block element.
- `inline-grid` displays element as a inline grid element.

---
## Flex
### Container
- **flex-direction**
	- `flex-direction: row;` (default)
	- `flex-direction: row-reverse;`
	- `flex-direction: column;`
	- `flex-direction: column-reverse;`
- **flex-wrap**
	- `flex-wrap: nowrap;`
	- `flex-wrap: wrap;`
	- `flex-wrap: wrap-reverse;`
- **justify-content** (main or X axes)
	- `justify-content: flex-start;`
	- `justify-content: flex-end;`
	- `justify-content: center;`
	- `justify-content: space-between;`
	- `justify-content: space-around;`
	- `justify-content: space-evenly;`
- **align-items** (cross or Y axes)
	- `align-items: flex-start;`
	- `align-items: flex-end;`
	- `align-items: center;`
	- `align-items: baseline;`
	- `align-items: stretch;`
- **align-content** (for +1 lines)
	- `align-content: flex-start;`
	- `align-content: flex-end;`
	- `align-content: center;`
	- `align-content: baseline;`
	- `align-content: stretch;`
### Children
- order
- flex-basis: 50%;

---
## Grid

---
