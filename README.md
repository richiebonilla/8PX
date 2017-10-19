# 8pt
SCSS mini-framework built on top of Bootstrap 3. Creates responsive helper classes to hide/show elements, specify margins &amp; padding, and more, without writing CSS. It assumes there is a standard grid size being used by the designers on the project. The default is an 8px grid, so all numbered suffixes represent multiples of 8px. This reduces the need for one-off CSS that bloats stylesheets and works alongside Bootstrap's native helper classes.

# Helper Classes
Helper classes are applied mobile-first. So, if a style is applied for all screen sizes, then the “xs” helper is only needed.

**Screen sizes (Based on Bootstrap 3 breakpoints)**
```
XS - 0 and greater
SM - 768–991px wide
MD - 992–1199px wide
LG - 1200px and greater
```

## Margins & Padding

###### Class Structure
```
[declaration] + [modifier] + [screen size] + [value]
```

###### Example: 

```
class=”p-top-xs-4”
[padding] + [top] + [screen size: small] + [4*8px = 32px]
```

###### Output:
```
@media screen and (min-width: $screen-sm-min) {
	padding-top: 32px;
}
```

###### Options:
```
[margin / padding] + [top / right / bottom / left / x / y ] + [screen size] + 
[1–35; 1.5–5.5]
(1.5 is declared as “1_5”; Example: p-top-xs-1_5)
```

“X” defines -left and -right modifiers simultaneously
“Y” defines -top and -bottom modifiers simultaneously

## Text Alignment
**Example:**
```
	class=”left-sm”
```

###### Output:
```
@media screen and (min-width: $screen-sm-min) {
	text-align: left;
}
```

###### Options:
```
[left / center / right] + [screen size]
```

**Floats Example:**
```
	class=”float-left-md”
```

###### Output:
```
	@media screen and (min-width: $screen-md-min) {
	Float: left;
}
```

###### Options:
```
	[float] + [left / none / right] + [screen size]
```

**Margin Auto Example:**
```
class=”margin-auto-m”
```

###### Output:
```
@media screen and (min-width: $screen-md-min) {
	Margin: auto;
}
```

###### Options:
```
    [margin] + [auto / initial] + [screen size]
```

**Vertical Alignment Example:**
```
class=”valign-middle-lg”
```

###### Output:
```
@media screen and (min-width: $screen-lg-min) {
	Vertical-align: middle;
}
```

###### Options:
```
[margin] + [auto / initial] + [screen size]
```

**Display Example:**
```
class=”hide-sm”
```

###### Output:
```
@media screen and (min-width: $screen-sm-min) {
	display: none
}
```

###### Output:
```
[hide / show] + [screen size] + [i / ib (optional)]
.hide-md - display: none
.show-md - display: block;
.show-md-i - display: inline;
.show-md-ib - display: inline-block
```

**Widths Example:**
```
class=”w-sm-20”
```

###### Output:
```
@media screen and (min-width: $screen-sm-min) {
	Width: 20%;
}
```

###### Options:
```
[width] + [screen size] + [10, 20, 30, 40, 50, 60, 70, 80, 90, 100]
```

## Stacking Helper Classes in HTML
Classes are applied from smallest to largest and in the order of the box model (top, right, bottom, left). 
If an element does not change based between screen sizes, then it should only receive an XS class. 

###### Padding, Stacking Example
```
class=”p-top-xs-1  p-top-md-3  p-top-lg-5”
```

###### Output:
```
<style>
padding-top: 8px;

@media screen and (min-width: $screen-md-min) {
	padding-top: 32px;
}
@media screen and (min-width: $screen-lg-min) {
	padding-top: 32px;
}
</style>
```

**Display, Stacking Example**
```
class=”hide-xs  show-md-ib  show-lg”
```

###### Output:
```
<style>
display: none;

@media screen and (min-width: $screen-md-min) {
	display: inline-block;
}
@media screen and (min-width: $screen-lg-min) {
	display: block;
}
</style>
```

**Box Model, Stacking Example**

Declare by box model order first, then by screen size.
This makes the classes easy to read and identify overrides.

```
class=”p-top-xs-1  p-top-sm-2  p-right-xs-1  p-right-sm-2  p-bottom-xs-1”
```

**Multiple Types of Helpers, Stacking Example**

Declare in the same order we declare CSS: alignment & display, box model, appearance.
```
class=”float-xs show-xs p-top-xs-2 center-xs”
(float, display, padding, text-align)
```