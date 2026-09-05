---
layout: post
title: CSS Properties
---

# CSS Properties

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
When using the dev tools in the web browser you can see browser defaults that applies styles to elements. Browser defaults have a very low priority. body and h1 also got default margin. Browser defaults target the element so they override inheritance or property we want to be inherited.

## Inheritance
Inheritance means the element also inherits some styles of the parent element. Inheritance have a very low specificity. It is even below browser defaults.

Instead of using star or universal selector that got a low specificity, we can set a global font by putting it in `body`. 

## Combinator
### Adjacent Sibling Combinator
Select the second element that is immediately after the first element. Both elements should have the same parent.
`div + p`

Multiple chaining:
`div + p + a`

### General Sibling Combinator
Select the second element that is after the first element. Both should have the same parent.
`div ~ p`

### Child Combinator
Select the second element that is a direct child and not a grandchild of first element.
`div > p`

Select the anchor that is inside a paragraphn that is inside a div.
`div > p > a`

### Descendant Combinator
Select the second element that is a descendant of the first element.
`div p`

## Box Model
### Content
The space inside an element.

### Padding
The space surrounding the content of an element.
`padding: 20px;`

### Border
The line surrounding the padding of an element.

Shorthand:
`border: 5px solid black;`

Subproperties:
`border-width: 5px;`
`border-style: solid;`
`border-color: black;`
`border-bottom: 5px solid white;`

### Margin
The space surrounding the border of an element.

Shorthand:
Set margin to all sides.
`margin: 20px;`

Subproperties:
`margin-top: 5px`
`margin-right: 10px`
`margin-bottom: 5px`
`margin-left: 10px`

Values are placed to set top, bottom, right and left margin.
`margin: 5px 10px 5px 10px;`

Values are placed to set top and bottom then left and right margin.
`margin: 5px 10px;`

### Shorthand
Short way of writing CSS code. If a value is omitted, the default value will be used so the style might not apply like in `border: 3px black;`. Order of values doesn't matter as long as values aren't the same.

## Margin Collapsing
It is when margins of two elements overlap into one combined space. Bigger margin will be applied. Use `margin-top` only or `margin-bottom` most of the time as a good practice.
Margin collapsing will happen in:
- Adjacent siblings where both have margins.
- A parent that got a child or first and or last child have margin (the parent's margin will collapse with the child's margin) [if the parent got a content other than the child, border or padding then this will not occur].
- Element with no content, padding, border or height.

## Width Property
Change the width of the element. Block level elements have width set to 100% by default.

Absolute values can be used:
`width: 300px;`

The element will take 100% width of the page or container.
`width: 100%;`

## Height Property
Change height of the element.

Takes 100% height available from parent container which if it is main then main will be by default only have height to fit only the contents. Set main to an absolute value to make elements inside it be able to use percentage values. If main will have 100% height then body should also have 100% height to be able to pass it down for elements inside main to have 100% height too.
`height: 100%;`

`height: 500px;`

## Box Sizing Property
We can't combine margin even with `border-box`;
`box-sizing: content-box;` - Default value. Height and width applies to the content of the element only.
`box-sizing: border-box;` - Combines content, padding and border in height and width. We can't combine margin even with `border-box;`. `border-box` is usually used for all elements. When placed in body, inheritance won't take effect because the browser sets its own box-sizing for block level element. Use universal selector. Universal selector overrides inheritance and browser defaults.
```css
h1 {
	box-sizing: border-box;
}
```

## Block Element Modified
A way to name elements.

## Inline Level Element
Inline elements don't take the full width. It only takes the needed space for its content so elements can be in one line. Margin top and bottom and padding and width and height (width and height are auto to take space needed by content) can't be set since they won't have an effect. A line break will be placed if the content of the element take a lot of space. Uses box model. Will push elements with border.
- `a`
- `span`
- `img`

## Block Level Element
Takes the full available width minus margin and padding. Takes a new line.
- `div`
- `section`
- `article`
- `nav`
- `h1`
- `p`

## Display Property
Changes the behavior of the element. Values: `inline`, `block`, `inline-block` and `none`. `none` makes the element disappear and its position be taken by other elements (taken out of document flow but still part of DOM). Changing inline to block is not that useful. `inline-block` is a mixed behavior and we can set margin top and bottom and padding but only takes the needed space for content so they can be side by side. Flexbox is another tool to position elements instead of using `ineline-block` and setting padding or margin.
```css
h1 {
	display: inline-block;
}
```

## Visibility Property
`visible` - Element can be seen.
`hidden` - Element is hidden but the space it is covering won't be taken by other elements (other elements won't fill the empty spot). It is not removed from the document flow and not removed in DOM.
```css
h1 {
	visibility: hidden;
}
```

## Text Align Property
Move text and inline elements to left, right or center.
`text-align: right;`

## Calc Function
`width: calc(100% - 49px);`

## Text Decoration Property
For anchors, `underline` is default value. Setting `text-decoration: none;` to container with anchors won't remove underline because of default browsers so `none` can't be inherited.

Remove underline of anchor.
`text-decoration: none;`

## Font Weight Property

Make the text bold.
`font-weight: bold;`

## Font Size Property
Change size of text.
`font-size: 22px;`

## Vertical Align Property
Moves the position of text to the middle vertically.
`vertical-align: middle;`

## Pseudo Classes
Select a state of an element or be be precise on what we want to style.

Add hover effects.

Hover effect.
```css
a:hover {
	color: white;
}
```

Effect on holding mouse button.
```css
a:active {
	color: white;
}
```

`:first-of-type` - Style the first element of sibling elements of the same type.

`:focus` - Style selected input elements.

`:first-child`

`:invalid`

## Pseudo Element
Style a part of an element.

`::first-letter` - Style the first letter of an element like a paragraph.

```css
p::first-letter {
    color: red;
    font-size: 20px;
}
```

`::first-line`

`::after` - Render content through CSS (helpful content that adds to design).
`::before`

## Content Property
Can only be used in `::before` and `::after`. Add content to DOM. We can render icon after a text.
```css
.main-nav__item a::after {
    content: " (Link)";
    color: red;
}
```

## Grouping
Combine selectors with the same declaration set using `,` into one rule.
```css
.main-nav__item a:hover,
.main-nav__item a:active {
    color: white;
}
```

## Border Radius
Round the corners.
`border-radius: 8px;`

## URL Helper Method
Add a background image. URL can be using a link like `http...` or path to file.
`background: url("freedom.jpg");`

## Properties Worth Remembering
`color`
`background-color`
`display`
`padding`
`border`
`margin`
`width`
`height`

## Chained Selector / Combined Selector
Select an anchor with an active class in it. `a .active` is a different selector that selects elements with .active class and got a direct or indirect anchor parent. `a#active` also words as a chain. Not an official selector.
```css
a.active {

}
```

```html
<a href="#" class="active">
```

## Linking / Bookmark
Clicking on anchor makes the browser jump to the element.
```html
<a href="#outro">Outro</a>
```

```html
<section id="outro" class="main-section">
    
</section>
```

## Important Rule
Overwrites specificity and all other selectors.`!important` is almost never used.
```css
div {
	color: red !important;
}
```

## Not Pseudo Class
Reverse certain rules or exclude a certain selector. Applying more than one selector is experimental so use only one selector all the time. Some browsers don't support complex selectors.

Apply blue to elements that is not a paragraph.
```css
:not(p) {
	color: blue;
}
```

Select anchor that is not active.
```css
a:not(active) {
	color: blue;
}
```

We can avoid using :not() by writing in a positive way. We can just use blue as default for all anchors then change color if they have active class. Order need no to be changed since above the tag selector is a more specific selector so it will apply to anchor with active class. Writing positively is better than using :not().
```css
a {
	color: blue;
}
```

## Browser Support
It is important to know if a feature you will be using is working on your target audiences' browsers. `caniuse.com` is useful for checking browser support.