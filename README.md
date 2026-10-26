
# HTML & CSS — Learning Notes

## 1. HTML Classes

The `class` attribute identifies elements so CSS can style them.

```html
<div class="card">Content</div>
```

Here, `card` is the class name.

### Multiple classes on one element

An HTML element can have multiple classes separated by spaces.

```html
<div class="left card">Beauty content</div>
<div class="right card">Construction content</div>
```

- The first element has two classes: `left` and `card`.
- The second element has two classes: `right` and `card`.
- Both elements share the `card` class.

**Remember:** Spaces separate class names in an HTML `class` attribute.

## 2. CSS Class Selectors

Use a period (`.`) before a class name.

```css
.card {
  width: 45%;
}

.left {
  float: left;
}

.right {
  float: right;
}
```

An element with `class="left card"` receives styles from both `.left` and `.card`.

### Combining class selectors

```css
.left.card {
  float: left;
}
```

This selects an element that has **both** the `left` and `card` classes.

There is no space between `.left` and `.card`.

### Descendant selectors

```css
.left .card {
  width: 45%;
}
```

This selects an element with the `card` class inside an element with the `left` class.

The space means the second element is a descendant of the first.

| Selector | Meaning |
|---|---|
| `.card` | Element with the `card` class |
| `.left.card` | Element with both `left` and `card` classes |
| `.left .card` | Element with `card` inside an element with `left` |

## 3. The `<span>` Element

`<span>` is an inline HTML element used to group a piece of text for styling.

Example:

```html
<h1>
  We are a <span class="creative">Creative</span> Design Agency
</h1>
```

CSS:

```css
.creative {
  color: midnightblue;
}
```

Only the word `Creative` receives the specified text color.

## 4. CSS Floats

The `float` property positions an element to the left or right, allowing surrounding content to flow around it.

```css
.left {
  float: left;
}

.right {
  float: right;
}
```

Common uses include positioning images alongside text.

Floats can be useful for text wrapping, but modern layouts often use Flexbox or Grid.

## 5. Image Styling

HTML:

```html
<img class="tile-image" src="beautiful.jpg" alt="Flower in water">
```

CSS:

```css
.tile-image {
  height: 200px;
  float: left;
  margin-right: 50px;
}
```

- `height`: Sets the image height.
- `float`: Positions the image to one side.
- `margin-right`: Adds space to the right of the image.

Use a class selector when you want to style specific images rather than every image on the page.

## 6. Responsive Design

Responsive design adapts a website's layout to different screen sizes.

A media query lets you apply CSS only when specified conditions are met.

Example:

```css
.card {
  width: 45%;
}

@media (max-width: 680px) {
  .card {
    width: 100%;
  }
}
```

**On wider screens:** Each card occupies 45% of its containing block.

**At viewport widths of 680px or less:** Each card occupies 100% of its containing block.

The media query changes the card width. The surrounding layout determines whether the cards actually appear side by side or stacked vertically.

## 7. Key Takeaways

- An HTML element can have multiple classes.
- Separate class names in HTML with spaces.
- Use `.class-one.class-two` to select an element with both classes.
- Use `.class-one .class-two` to select a descendant.
- Use `<span>` to style part of a line of text.
- Use `float` when appropriate for positioning content and wrapping text.
- Use media queries to apply styles at particular viewport widths.
- Changing an element's width does not, by itself, guarantee a particular layout.

## 8. Practice Questions

Try answering these without looking at the notes.

**Q1.** How many classes does this element have?

```html
<div class="left card">
```

**Q2.** Which selector targets an element with both `left` and `card` classes?

A. `.left .card`  
B. `.left.card`  
C. `left.card`

**Q3.** What does the space mean in `.left .card`?

**Q4.** What is the purpose of a media query?

**Q5.** What is the difference between `width: 45%` and `width: 100%` in your responsive card example?
