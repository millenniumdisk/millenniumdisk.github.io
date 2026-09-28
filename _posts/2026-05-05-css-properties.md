---
layout: post
title: CSS Properties
---

# CSS Properties

## Shorthand
When using shorthand, other properties are also overwrites other properties because it will initialize other properties as default even if only one value is added.
Short way of writing CSS code. If a value is omitted, the default value will be used so the style might not apply like in `border: 3px black;`. Order of values doesn't matter as long as values aren't the same.

Use shorthand and then use specific subproperty to override a part of the shorthand.

Add a border but left border is removed.
```css
border: 4px solid black;
border-left: none;
```

## Background Property (Shorthand)
Change the background color of the element. Using `url("")` and adding an image path will need width and height with px values and not percent values when `position: fixed` is not placed. Use `position: fixed` to make the image be out of the document flow and be able to use percent values in height and width.
```css
h1 {
	background: violet;
}
```

Image value comes first then position values and then size values. 

Setting only one `border-box` will put it as value for both origin and clip.
`background: url("freedom.jpg") left 10% bottom 20%/cover no-repeat border-box`

Order matters so `border-box` is set for origin and `padding-box` is set for clip.
`background: url("freedom.jpg") left 10% bottom 20%/cover no-repeat border-box padding-box;`

Local can be placed as last value.

### Background Image Property
Multiple background images can be defined.
`background-image: url("freedom.jpg");`

### Linear Gradient
Linear and radial gradients are treated as images.

First argument is the direction which can be ommitted which will make first argument to be color. Default direction is vertically. It is from top to bottom.
`background-image: linear-gradient(red, blue);`

From top to bottom.
`background-image: linear-gradient(to bottom, red, blue);`

From top right to bottom left.
`background-image: linear-gradient(to left bottom, red, blue);`

`background-image: linear-gradient(to left top, red, blue);`

`background-image: linear-gradient(to right top, red, blue);`

Start from bottom left to top right.
`background-image: linear-gradient(30deg, red, blue);`

Start from bottom to top.
`background-image: linear-gradient(0deg, red, blue);`

From top to bottom.
`background-image: linear-gradient(180deg, red, blue);`

We can add as many colors and even hex.
`background-image: linear-gradient(180deg, red, blue, green, yellow, #fa923f);`

We can transition to transparent.
`background-image: linear-gradient(180deg, red, transparent);`

We can use RGBA.
`background-image: linear-gradient(180deg, red, rgba(0, 0, 0, 0.5));`

30% is red. Blue also takes the same space. RGBA also follows the same space taken.
`background-image: linear-gradient(180deg, red, blue, rgba(0, 0, 0, 0.5));`

Red will take 70% of the space.
`background-image: linear-gradient(180deg, red 70%, blue, rgba(0, 0, 0, 0.5));`

At 80%, blue will be finished in occupying space.
`background-image: linear-gradient(180deg, red 70%, blue 80%, rgba(0, 0, 0, 0.5));`

When blue got a lower percent value than red, it will make a hard edge because there is no space for blue to transition. So when blue enters, it is already to late.
`background-image: linear-gradient(180deg, red 70%, blue 60%, rgba(0, 0, 0, 0.5));`

### Radial Gradient
Create a radial gradient.

Default position is in the middle and default shape is ellipse. Start with red color and then use blue.
`background-image: radial-gradient(red, blue);`

Multiple colors can be used.
`background-image: radial-gradient(red, blue, green);`

The only alternative is circle.
`background-image: radial-gradient(circle, red, blue, green);`

Circle will start at the top with at attribute.
`background-image: radial-gradient(circle at top, red, blue, green);`

Start at top left.
`background-image: radial-gradient(circle at top left, red, blue, green);`

Custom values can be used. Move 20% from the left and 50% from top. First is x axis, second is y axis. px values can be used instead of percent values.
`background-image: radial-gradient(circle at 20% 50%, red, blue, green);`

We can add the size after circle. 20px is diameter of the shape except the other part. Size won't have an effect on ellipse because we need to values for size.
`background-image: radial-gradient(circle 20px at 20% 50%, red, blue, green);`

Ellipse with size. First is width and next is height.
`background-image: radial-gradient(ellipse 20px 20px at 20% 50%, red, blue, green);`

`background-image: radial-gradient(ellipse 20px 30px at 20% 50%, red, blue, green);`

`background-image: radial-gradient(ellipse 80px 30px at 20% 50%, red, blue, green);`

The point where blue and green changes is barely touching the edge horizontally.
`background-image: radial-gradient(ellipse farthest-side at 20% 50%, red, blue, green);`

The point where blue and green changes is barely touching the edge vertically so it is top and bottom.
`background-image: radial-gradient(ellipse closest-side at 20% 50%, red, blue, green);`

Closest corner ensures the outermost ring touches the closest corner.
`background-image: radial-gradient(ellipse closest-corner at 20% 50%, red, blue, green);`

Touch the farthest corner.
`background-image: radial-gradient(ellipse farthest-corner at 20% 50%, red, blue, green);`

Color stops can be defined also.
`background-image: radial-gradient(ellipse farthest-corner at 20% 50%, red, blue 70%, green);`

### Background Color Property
`background-color: red;`
Only one background color can be defined. If defined with background image, the color won't show because the image is in front.

### Background Size Property
Change size of background image.

Set width of image to 100 pixels. Height adjusts to keep the aspect ratio when not specified.
`background-size: 100px;`

Image can be distorted when height is also specified.
`background-size: 300px 100px;`

Percent value can be used.

Take 50% of available space.
`background-size: 50%;`

50% width and 100% height.
`background-size: 50% 100%;`

If you don't want to distort it (keep aspect ratio), auto can be used for width.
`background-size: auto 100%;`

When height is undefined like in `background-size: 100%;`, it is the same as `background: 100% auto;`. Image will take full width of container and will not overlap in all sides even if if image height doesn't match container height. The image is automatically cropped. We can control how the image is cropped.

Predefined value is cover. Cover is the same as `background-size: 100%;`. It may look like cover is making the image be 100% in width but it is not. Cover finds what is the important value to be aligned to background image. Image is landscape so cover will set width to 100% because height is lesser than width. Portrait mode container is opposite. Cover always set image to fill the entire container.
`background-size: cover;`

Makes sure the whole image is seen in the container but will make whitespace appear on the container. Might not fill the entire container.
`background-size: contain;`

Using a small px value will make multiple small images be the background.

### Background Repeat
Image is set to repeat as default value.

`background-repeat: no-repeat;`

Repeat in x axis.
`background-repeat: repeat-x;`

Repeat in y axis.
`background-repeat: repeat-y;`

### Background Position Property
First value defines x axis which is for how the left edge of the image should be positioned relative to left edge of the container. 

Move the background image to the right by 20 pixels.
`background-position: 20px;`

Second value is for y axis which is top.
`background-position: 20px 50px;`

Percent can be used but to define how much can be excess. Width is not affected since it is all being displayed.
Only 10% will be cropped at the top.
`background-position: 10%;`

Left part of excess space which we have none is at the edge.
`background-position: 0%;`

Excess space should go to top when there is second value.
`background-position: 0% 10%;`

50% means excess that don't fit in the container, 50% at the top will be cropped and 50% at the bottom will be cropped.
`background-position: 0% 50%;`

100% means excess that should be cropped will be cropped at the top 100% and nothing will be cropped at the bottom.
`background-position: 0% 100%;`

Center is a predefined value. It is the same as setting `background-position: 50% 50%;`
`background-position: center;`

left and top are predefined values. It is the same as setting `background-position: 0% 0%;`. It means left side and top side will both be not cropped.
`background-position: left top;`

Bottom will not be cropped.
`background-position: left bottom;`

Percent can be combined with predefined values.

Crop left side by 10% and crop bottom side by 20%.
`background-position: left 10% bottom 20%;`

### Background Origin Property
Background origin is like box sizing. Default got space in left and right border but not in top and bottom if image is cropped.
`background-origin: border-box;`

Content box is not the default.

There will be padding that will appear because we are setting height and width of image but only content and not including padding and border.
`background-origin: content-box;`

Default value. Content and padding will be included but not border.
`background-origin: padding-box;`

### Background Clip Property
It is where we want to clip or crop the image. Affects the width.

We can use border box value.
`background-clip: border-box;`

Padding box value will mean we are cropping the image after the padding.
`background-clip: padding-box;`

Clip or crop the image before the padding.
`background-clip: content-box;`

### Background Attachment Property
Defines scrolling behavior on image that is not fixed. Rarely used.

`fixed` - Image would not be fixed to the container but the viewport.
`inherit`
`initial`
`local` - Image scrolls with the other content of the container.
`scroll` - Image would stay in place and content would scroll over it above it.
`unset`

### Multiple Backgrounds
It is ok to have multiple backgrounds (image / gradient) and some can be transparent. Only one solid color can be used and it should be at the most bottom layer.

#ff1b68 is used as a fallback background when the image won't load.

The image that will only be modified is #ff1b68 because it is followed by the background properties.
`background: url("images/freedom.jpg") #ff1b68 left 10% bottom 20%/cover no-repeat border-box;`

Use , to add multiple image / gradient. Linear gradient will be on top of image because it comes first.
`background: linear-gradient(), url("images/freedom.jpg") left 10% bottom 20%/cover no-repeat border-box, #ff1b68;`

Add a light brown linear gradient that will go transparent and it starts from bottom to top with 0.6 transparency and 10% color stop.
`background: linear-gradient(to top, rgba(80, 68, 18, 0.6) 10%, transparent), url("images/freedom.jpg") left 10% bottom 20%/cover no-repeat border-box, #ff1b68;`

Each background image can have their own background properties and they are separated by commas.
`background: <image> <properties>, <image> <properties>;`

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
`border-left-color: #ff5454;`

### Margin
The space surrounding the border of an element. `auto` as value will make the element fill the left and right space equally which will make it centered but it won't work vertically but `margin: 0 auto;` and `margin: auto;` are both ok to use. `auto` is ok to use even if width is not 100%.
`margin: auto;`

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
Inline elements don't take the full width. It only takes the needed space for its content so elements can be in one line. Margin top and bottom and padding and width and height (width and height are auto to take space needed by content) can't be set since they won't have an effect. A line break will be placed if the content of the element take a lot of space. Uses box model. Will push elements with border. Width has no effect on inline elements.
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

Using inline or block as value is useful if you want the behavior to be specific like it should only take space as its content needs or the element should take the full available width.
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
For anchors, `underline` is default value. Setting `text-decoration: none;` to container with anchors won't remove underline because of browser defaults so `none` can't be inherited.

Remove underline of anchor.
`text-decoration: none;`

## Font Weight Property

Make the text bold.
`font-weight: bold;`

## Font Size Property
Change size of text.
`font-size: 22px;`

## Vertical Align Property
Moves the position of text to the middle vertically. `top` and `middle` are values.
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
Round the corners. Setting a value of 50% will make a circle.

`border-radius: <top_left> <top_right> <bottom_right> <bottom_left>;`

`border-radius: 4px 4px 4px 4px;`

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

## Box Shadow Property
Blurriness can be ommitted. Spread can also be ommitted. Spread is how big of an area the shadow will cover.
`box-shadow: <x_axis> <y_axis> <blurriness> <spread> <color>;`

`box-shadow: 2px 2px 2px 2px rgba(0, 0 , 0, 0.5);`

Spread is not added.
`box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);`

## Color Function
`rgb(255, 255, 255)`

Fourth arg is alpha channel (transparency).
1 = not transparent
0.5 = 50% transparent
0 = fully transparent
`rgba(255, 255, 255, 0.5)`

## List Style Property
Can be set to `none` so bullet points won't appear on list items when property is placed in the `ul` or `ol` element.
`list-style: none;`

## Font Shorthand Property
`font: inherit;`

## Inherit
Applies what would have been inherited and sets those as the style.
`font: inherit;`

## Cursor
Default value is default. Set this in a button to see a pointing hand when on a button.
`cursor: pointer;`

## Outline
It is a browser default that can be seen in dev tools. Go to :hov. It is the focus pseudo selector. Outline is not part of box model.
`outline: none;`

## Float
Not that much used anymore since flex box is better. Floating elements can be useful to position some elements differently in the document flow. Overwrite default positioning and tell the browser to push the element to left or right. Take out element from document flow and elements below the floated element will take its previous place but the elements below the floated element will float around the floated element. Float is great for positioning an image in text and the text will float around the image. Float is not great for positioning block level elements because the text will respond but block elements won't. We need to make its space be reserved and tell other block level elements after it that they shoudn't respect any previous floatings. We can float text too. Don't use float to position elements.
`float: right;`

`clear: both;` is used to clear both left and right floats.
```html
<div class="clearfix"></div>
```

```css
.clearfix {
    clear: both;
}
#highlighted {
    float: right;
}
```

## Position Property
Changes the position of the element. Can be applied to block and inline element. Position changes will only apply if we use a value that is not `static` so `top: 100px` won't do anything.

Values:
- `static` - Default value.
- `fixed`
  - Takes element out of document flow.
  - Will create a stacking context even if no z index is applied manually.
  - Element will be positioned depending on the viewport (viewport is the positioning context).
- `absolute`
  - Takes element out of document flow.
  - Will only create a new stacking context when you apply a z index manually.
  - Positioning context will be html element if no ancestors or parent got a position property applied.
  - When there is an ancestor with the position property applied, the closest ancestor that got the position property applied will be the positioning context for the element (element will be positioned in relation with the ancestor).
- `relative`
  - Doesn't take the element out of document flow.
  - Will only create a new stacking context when you apply a z index manually.
  - The positioning context is the element itself. We can move an element down and to right from its previous or initial position with `top: 50px` and `left: 50px`. We can push the element out of its parent with a higher value like `top: 300px`.
- `sticky`
  - A new value so there are limitations to it.
  - Browser support is not the best.
  - A combination of relative and fixed.
  - Adding `position: sticky` only won't do anything so also add `top: 20px` and when border space is reached, element will become fixed. If `top: 0` is used then the border around the element will be on edge of viewport when it is turned to fixed.
  - The element won't be fixed anymore when it is the end of the parent's content.

Takes the element out of the document flow making the next element take the previous position of the element with `fixed` but even thought it is changed, it is still visible. Other elements will think the element with `fixed` doesn't exist. `fixed` makes the element behave like an inline block element where its width can be changed. `top: 100px` will have an effect moving the element down. `top: 0` and `margin: 0` will make the element stick to the top edge. The element has the viewport as the position in context so it will stick to the top of viewport. Element's position depends on the viewport.
```css
position: fixed;
```

Change position of elements in document flow. Percent and px values can be used.
`top: 100px;`
`bottom`
`left: 0;`
`right`

`top: 20px;` might mean add 20px to top of current element's position and change its position. It could also mean 20px from the top of our viewport or of our HTML element or of body element or other element. These options are positioning context.

If html or body element got a margin and we want the navigation bar to be on the top, we need to add `top: 0` and `left: 0` but if there is no margin, then there is no need to add them.

## Positioning Context
Defines the anchor point when an element's position change.

## Viewport
The visible part of the website.

## Z Index Property
Default value is `auto`. `auto` is equal to `0` value. Putting an element above an element with a z index of 0, a higher value is needed which can be 1, 10 or 100. Use a lower value like -1, -10 or -100 to put the element below. To make z index have an impact on the element, the position property should have a value that is not `static`. If z index value is both the same or both are 0, then the order of the elements in the HTML file matters. The element on the bottom most part of the HTML file will be on top of other elements that are at the top of the HTML file.

An element with a low z index can't be behind its parent with a high z index.

## BEM Notation
A convention which is good practice to follow when naming HTML element's classes.

## Overflow
By putting `overflow: hidden` in the parent container, an element with `position` disappear when it is outside its parent container.

When `overflow: hidden` is added to body, it will be passed to html. So it means that body won't have `overflow: hidden` and html got it instead. Just add `overflow: hidden` to both body and html. The same thing will happen if `overflow: hidden` is added to body and `overflow: auto` is added to html.

## Stacking Context
Stacking context is the system on how elements are layered on the webpage in the z dimension. Child elements are considered one unit with the parent container so they don't interfere with the z index of other parent containers that are siblings.

## Images
Images will display their original size by default even if the container's height and width are changed. Select the image and change its height but using 100% won't make it be the size of the container because the image will use its original size. It is because the image is inside an anchor which is an inline element. Set anchor to inline-block to use 100%. The problem is that the anchor isn't an inline-block or block element. This is all we can do in normal images. All the other styling we did in background images can't be done to normal images. Hacky solutions like a -5px margin top sometimes work to move the image to the top a little bit. If you want to do complex styling on an image, use background image but it won't be part of the document flow. It doesn't have its own HTML element that signals that it is an image.

Add a `vertical-align: top` or bottom or set image to block with display to an image element that is inside a container when using it because of a bug that makes box shadow get a whitespace at the bottom part. This bug happens because image is an inline element.

## Filter Property
Applies blurring, grayscale or changing the contrast of an element.

Element without any content but got a background of brown and height and width. Applying filter will turn it into a blurry box.
```css
div {
	background: brown;
	filter: blur(10px);
}
```

MDN contains a list of filters.
We can apply more than one filter.

Grayscale accepts a percent value. 100% means black and white image.
`filter: grayscale(100%);`

A little grey added.
`filter: grayscale(40%);`

Basic support for filters may be not present for IE. Polyfill can be used instead or implement some other fallback or just use filter to enhance the look only and not something that is depended on heavily.

Affects all content.

## SVG
Browser support is decent.
Styling the color of the lines in an SVG can be done by overwriting fill color but it is more related to SVG than CSS and is advanced.

Adding a padding to the container of an SVG can make the SVG small. The SVG got inline styles and they can be overwritten with !important.

Fill property is how SVG is filled.

Stroke property can be added.
`stroke: black;`

Thickness of stroke.
`stroke-width: 10px;`

## Units
px - pixels
% = precentages
rem - root em refers to the font size
em - em also refers to the font size
vh - viewport height
vw - viewport width

Properties where applying units makes sense.

font-size
padding
border
margin
width
height
top
bottom
left
right

Absolute Lengths - Mostly ignore user settings (px ignore browser settings).
- px - Used mostly.
- cm - Don't use in web development.
- mm - Don't use in web development.

Viewport Lengths - Adjusts the size of element we apply to according to the viewport. Lengths that allow us to to adjust our size more dynamically to the viewport.
- vh - Apply viewport lengths with vh. Viewport Height.
- vw
- vmin
- vmax

Font-Relative Lengths - Font-relative lengths adjust to the default font size.
- rem - Apply font-relative lengths with rem.
- em - Apply font-relative lengths with em.

Percent Value Lengths - Special case.

Percent Values

Three Rules to Remember

1. If there is an element with percentage value unit applied like 10% width and got position fixed, containing block will refer to viewport so 10% of viewport or container's width will be the width of the element.
2. Element with a percentage value and got position absolute will have a containing block which is the ancestor's content + padding. The ancestor should have a position that is not static (absolute, relative, fixed or sticky).
3. We have an element and we apply a percetage value to it and it got position static or position relative applied. The containing block is the ancestor's content. The closest ancestor that is a block level element is the containing block. An image which can be 50% or 100% inside a div will only have the 50% or 100% width of the content. Not content + padding. If it's closest parent becomes an inline, element will find the next closest parent that is a block level element as containing block.

When position fixed is applied and there is a width property to an element and percent value is used instead of px.

The position fixed changes how the percentage unit behaves.

Containing Block - Reference point for an element with a percentage unit. It can be an element or a parent with a width like 100px.

The child will have 10px if the child got 10% width.

If position is fixed, instead of element, the viewport becomes the containing block.

top: 0% means the element's top margin will be placed on top of its parent's top.

top: 50% means the element's top margin will be placed on the center of the parent.

bottom: 0% means the element's bottom margin will be placed on the parent's bottom.

bottom: 50% means the element's bottom margin will be placed on the center of the parent.

When the element got a position static or relative and height property is set with a percent value, the containing block will be the closest ancestor that is a block level element. The ancestor is also an element with position static or relative. height 100% won't work because height depends on the content but width 100% works because the value can be found in the containing block. To solve this with percent values, add html element selector and add height 100% and add height 100% to body also. Use position absolute to backdrop to make it go out of document flow and be above the webpage but height 100% is not needed for html and body but backdrop won't cover the whole viewport because testimonial got two margins added to it and margin collapsing happens but there is also no ancestor with position that is not static applied so it will act like position fixed and viewport is the containing block since we used percent value. The backdrop doesn't stick to the viewport though. So change position to fixed. Add top 0 and left 0 to fix margin collapsing.

Fonts without specified font size in a css file will change in size when browser settings font size is changed. If you want to change the font size for all elements in the beginning depending on the browser settings by using html tag selector and using font size 100% but it will overtake browser settings which is a behavior we already have. 75% can be used to make the browser settings default smaller.

## Combining Pixels and Percent Values
We can combine pixels and percent values.

Element will take 65% of the containing block but won't be very big and its max width is 580px.
```css
width: 65%;
max-width: 580px;
```

## Max Width Property
Element won't become more bigger than the limit specified.

Limit is 580px so image will stay 580px if it can become more than 580px.
`max-width: 580px;`

## Min Width Property
Element won't become more smaller than the limit specified.

The limit is 350px so image won't go smaller below 350px.
`min-width: 350px;`

## Other Font Size Units
An h1 element may have a font size assined by browser like 2em. We can go to dev tools and in computed tab. Untick show all. Font size applied to h1 will be listed as 40px. It is based on 20px that wasn't applied but 2em is used to multiply 2 to 20px so we get 40px. 1.5em can make 20px into 30px. Em is calculated based on the actual size of our element which is inherited from the parent and then multiplied by the factor in em. 1 em is equal to 16px. When browser settings is set to font size of very large, font size will become 24 and 16 * 1.2 will become 24 * 1.2 so a bigger font size if 1.2em is used. When there is a browser default that applies em to font size, it is ok to apply font size with em manually in the CSS file. 1.1em will make 16px to 18px. Em got a problem though since it inherits the previous size and increases its size.

### Rem (Root Em)
Can be used on other things aside from font size. Unit calculated based on font size. Takes the font size set by browser settings and multiplies with the specified value. Goes to root element which is html element. New. Browser support is now decent.

Browser default font size times 1.1.
`font-size: 1.1rem;`

### Em
Can be used on other things aside from font size. Unit calculated based on font size. Em inherits the previous size and multiplies the em with the previous em. Be careful when using em. There are some cases where em can be used.

1.2em is 19.2px. We got 19.2 from 16 * 1.2.
`font-size: 1.2em;`

## Viewport Units
Support is generally good but only partial support (vmax only) for Internet Explorer 11. Using position fixed and using percent values for width and height is a good alternative.

## Viewport Width
Unit always refers to viewport regardless of position value.

Same as width at 100%.
`width: 100vw;`

80% of viewport.
`width: 80vw;`

In Windows machines, 100vw is 100% of the viewport width + scrollbars.

If you don't want to display scrollbars, use width 100% instead of 100vw.

Second way is to use `overflow-x: hidden;` to body selector to hide horizontal scrollbar. `overflow-y: hidden;` hides vertical scrollbar.

Third way is using a pseudo element.
body::-webkit-scrollbar {
    width: 0
}

## Viewport Height
Unit always refers to viewport regardless of position value.

Same as height at 100%.
`height: 100vh;`

50% of viewport.
`height: 50vh;`

## Vieport Min
Looks at the width and height values. Takes the smaller from the two and adjusts its size based on the specified value.

Width becomes 80% of the smaller value.
`width: 80vmin;`

You can create overlaying elements and make them stick to the viewport.

## Viewport Max
Looks at the width and height values. Takes the bigger from the two and adjusts its size based on the specified value.

Width becomes 80% of the bigger value.
`width: 80vmax;`

You can create overlaying elements and make them stick to the viewport.

## Choosing Units
- Font Size (Root Element) - Percent value.
- Font Size - Rem (use em on child only and avoid em chains).
- Padding - Rem.
- Border - Pixel value.
- Margin - Rem.
- Width - Percent value or vw (use pixel value when using vmin or vmax).
- Height - Percent value or vh (use pixel value when using vmin or vmax).
- Top - Percent value.
- Bottom - Percent value.
- Left - Percent value.
- Right - Percent value.

## Center Elements
The auto value can be used to center elements. It only works on block level elements with width value.
`margin: auto;`

## Modal
A pop-up or overlay that appears on top or over the content of the webpage.

## JavaScript
Add `<script>` tag inside the bottom most part of the body tag of the HTML file.
`<script src="shared.js"><script>

The JavaScript file can have a short code.
`alert("This works!");`

We need to access the DOM element (what the browser makes of our HTML code).

We can access elements in the DOM.

Create a variable with `var` or `const`.

The `document` object is provided by the browser.

Use `querySelector` method to get an element. Argument is a normal CSS selector. Tag, ID, attribute or class selector or combinators can be used. `querySelector` always selects only one element (the first element the selector finds).

Get an element with anotherclass which has some parent with someclass.
`const backdrop = document.querySelector(".someclass .anotherclass");`

`const backdrop = document.querySelector(".backdrop");`

Use `console.log()` to see the element.
`console.log(backdrop);`

Object notation.
`console.dir(backdrop);`

`querySelectorAll` will get all elements with the class specified and put them in an array (node list). Index 0 is the first element.

We can see properties of the element selected with object notation `console.dir()`. `style` is one property of the element. We can see all style properties we can set for the element and their respective values. These style properties are added as inline styles.

Access style of element.
`backdrop.style.display = "block";`