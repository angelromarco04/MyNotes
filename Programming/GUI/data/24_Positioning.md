
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
	- `box-sizing: border-box;`
		- `width` and `height` modify `contents` + `padding` + `border`.

## Box position
```css
.something {
	position: <pos>;
}
```

- `absolute`
	- Is Independent from other elements.
	- Position is absolute to the screen.