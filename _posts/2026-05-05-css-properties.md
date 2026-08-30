---
layout: post
title: CSS Properties
---

# CSS Properties

## Display Property
Changes the behavior of the element. Values: `inline`, `block`, `inline-block` and `none`.
```css
h1 {
	display: inline-block;
}
```

## Box Sizing Property
Values: `content-box` and `border-box`. Default value is `content-box`. `border-box` is the value to use to make calculations easier (combines content, padding and border).
```css
h1 {
	box-sizing: border-box;
}
```

## Visibility Property
Values: `visible` and `hidden`.
```css
h1 {
	visibility: hidden;
}
```

## Background Shorthand Property
Change the background color of the element.
```css
h1 {
	background: violet;
}
```

## Color Property
Change the text color of the element.
`color: green;`

## Font Family Propery
Change the font family of the element. Browser defaults font family can be used like `sans-serif`, `serif`, `monospace`. When a font is imported like in Google Fonts, CSS code can look like `font-family: "Anton", sans-serif;`.
`font-family: sans-serif;`

## Inline CSS
Placed inside the html element that is inside the html file.
```html
<!DOCTYPE html>
<head>
</head>
<body>
	<h1 style="background: #ff1b68;">Learning Tool</h1>
</body>
```

We can use `;`.
```html
<!DOCTYPE html>
<head>
</head>
<body>
	<h1 style="background: red; color: green;">Learning Tool</h1>
</body>
```

## Internal CSS
The css code is still inside the html file.
```html
<!DOCTYPE html>
<head>
	<style>
		h1 {
			background: blue;
		}
	</style>
</head>
<body>
	<h1>Drop Chance calculator</h1>
</body>
```

## External CSS (External Stylesheet)
- The css code is in a different file.
- Create a css file. with a .css file extension like `main.css`
- Add css inside the created file.
- Connect the css file by specifying a stylesheet and `href` or hyper reference attribute will point to the path of the css file inside the html file.

`main.css`
```css
h1 {
	background: red;
}
```

`index.html`
```bash
<!DOCTYPE html>
<head>
	<link rel="stylesheet" href="main.css">
</head>
<body>
	<h1>International News</h1>
</body>
```

If CSS file is inside a `css-files` folder:
```html
<link rel="stylesheet" href="css-files/main.css">
```

## CSS Declaration
A CSS line is a CSS declaration.
```css
background: violet;
```

## CSS Property
A CSS property is what we want to modify.

## CSS Value
A CSS value is the change we want to apply to a property.

## Selector
The name of what we want to select.

## CSS Rule
Needs curly braces. Multiple selectors can be added to multiple elements.
```css
h1 {
	color: green;
}
```

## Color Property
Changes color of text.
```css
h1 {
	color: green;
}
```

## Externally Imported Font
Add our own fonts but might affect performance of the website.
Get fonts in: https://fonts.google.com/
```html
<!DOCTYPE html>
<head>
	<link rel="preconnect" href="https://fonts.googleapis.com">
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
	<link href="https://fonts.googleapis.com/css2?family=Anton&display=swap" rel="stylesheet">
	<link rel="stylesheet" href="main.css">
</head>
<body>
	<h1>International News</h1>
</body>
```

## Font Family Property
Changes how the font looks.

Anton needs to be imported first from Google Fonts.
```css
h1 {
	font-family: "Anton", sans-serif;
}
```

## Selectors

### Element Selector (Tag Selector)
Selects all of the specified element.

Select all `h1` elements.
```css
h1 {
	color: red;
}
```
```html
<!DOCTYPE html>
<html>
	<head>
		<link rel="stylesheet" href="main.css">
	</head>
	<body>
		<h1>This is a heading</h1>
		<p>This is a paragraph</p>
		<div>This is a div</div>
	</body>
</html>
```

### Class Selector
Selects all elements with the specified class.
```css
.blog-post {
	color: red;
}
```
```html
<!DOCTYPE html>
<html>
	<head>
		<link rel="stylesheet" href="main.css">
	</head>
	<body>
		<h1 class="blog-post">This is a heading</h1>
		<p class="blog-post">This is a paragraph</p>
		<div class="blog-post">This is a div</div>
	</body>
</html>
```

### Universal Selector
Selects all elements in the webpage. Universal selector is rarely used.
```css
* {
	color: green;
}
```
```html
<!DOCTYPE html>
<html>
	<head>
		<link rel="stylesheet" href="main.css">
	</head>
	<body>
		<h1>This is a heading</h1>
		<p class="blog-post">This is a paragraph</p>
	</body>
</html>
```

### ID Selectors
Selects only one element with eh specified ID.
```css
#main-title {
	color: blue;
}
```
```html
<!DOCTYPE html>
<html>
	<head>
		<link rel="stylesheet" href="main.css">
	</head>
	<body>
		<h1 id="main-title">This is a heading</h1>
	</body>
</html>
```

### Attribute Selector
Selects all elements with the specified attribute.
```css
[disabled] {
	color: violet;
}
```
```html
<!DOCTYPE html>
<html>
	<head>
		<link rel="stylesheet" href="main.css">
	</head>
	<body>
		<button disabled>This is a button</button>
	</body>
</html>
```

## ID
ID is not only used for styles. It can be used as a bookmark to make the browser jump to the element with the ID when a link is click connected to it. Can only be used once and must be unique.

## Class
Used to specify the group that will be styled. Can be reused.

## Multiple Classes
Multiple classes can be added on an element.
```html
<!DOCTYPE html>
<html>
	<head>
		<link rel="stylesheet" href="main.css">
	</head>
	<body>
		<h1 class="section-title highlighted">Choose Your Plan</h1>
	</body>
</html>
```
```css
.section-title {
	color: pink;
}

.highlighted {
	background: green;
}
```

## Cascading
Cascading means multiple rules can be applied to the same element. When conflicts happens, specificity is used to solve them.

### Specificity
The more specific selector have a higher priority.

Order of Priority:
1. Inline Styles
2. ID Selector
3. Class Selector, Attribute Selector, Pseudo Classes
4. Element Selector (Tag Selector), Attribute Selector

### Order
CSS is parsed from top to bottom so the code that is at the bottom of the file will have a higher priority.

When there are two CSS Rules with the same priority or specificity, the bottom one will be applied.

## Browser Defaults
When using the dev tools in the web browser, you can see the top most styles. The styles at the top part have the highest priority and are applied. There are also browser defaults that applies styles to elements.

## Inheritance
Inheritance means the element also inherits some styles of the parent element. Inheritance have a very low specificity. It is even below browser defaults.

Instead of using star or universal selector that got a low specificity, we can set a global font by putting it in `body`. 



read 08 in section 2 of css udemy notes

Padding
Border
Margin
Height
Width
