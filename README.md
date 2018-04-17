SCSS Utility Library that provides utility classes for spacing and displaying elements according to Bootstrap 4's breakpoints without writing any repetitive CSS.

The library assumes that your wireframes are designed using an 8pt grid system, so all margin, padding, and text sizes are multiples of 4px.

A typographic hierarchy is built-in and line heights are divisible by 4px so text elements will **not** disrupt the grid, thereby force you to write custom CSS to compensate.

**Some Examples**

Use .show-* and .hide-* to control the display property of an element at a given breakpoint.
- .hide-xs will hide the element at all breakpoints, but changing it to .hide-sm will only hide it at the 'small' breakpoint and up.

Use the margin and padding classes to add box model properties in multiples of 8px.
```
.mt-xs3     // margin-top: 24px; at all breakpoints
.pb-xs4     // padding-bottom: 32px; at all breakpoints
.mx-xs5     // margin-left: 40px; margin-right: 40px; at all breakpoints
```

Use the 'u' suffix to increment by 4px instead of 8px
```
.mt-xs3     // margin-top: 24px; at all breakpoints
.mt-xs3u    // margin top: 28px; at all breakpoints
```

Add breakpoints to the classes to add responsive margins and paddings
```
.mr-sm3     // margin-right: 24px; for breakpoints 'sm' and up
```

The same values used at the end of classes can be used as variables in your SASS code to represent pixel values. This means you don't have to convert your grid values (4 grid spaces) to pixel values (32px) mentally if you want to use them in stylesheets.
```
$x10        // 80px
$x10u       // 84px
```

# Full List of Available Classes
*[bracketed] denotes available options for that spot in the class.*

**Margin & Padding Classes**
```
.m[t, r, b, l, x, y]-[sm, md, lg, xl][1-40][u] // margin-[*]: [#]px
.p[t, r, b, l, x, y]-[sm, md, lg, xl][1-40][u] // padding-[*]: [#]px

.mauto-[xs, sm, md, lg, xl]     // margin: auto
.mintial-[xs, sm, md, lg, xl]   // margin: initial
```

**Display Classes**
```
.show-[xs, sm, md, lg, xl]      // display: block
.show-ib-[xs, sm, md, lg, xl]   // display: inline-block
.show-i-[xs, sm, md, lg, xl]    // display: inline

.hide-[xs, sm, md, lg, xl]      // display: none
```

**Text Align Classes**
```
.ta[l, r, c]-[xs, sm, md, lg, xl]  // text-align: [left, right, center]
``` 

**Typography Classes**
```
.h1-[xs, sm, md, lg, xl]        // font-size: 36px; line-height: 36px;
.h2-[xs, sm, md, lg, xl]        // font-size: 28px; line-height: 28px;
.h3-[xs, sm, md, lg, xl]        // font-size: 24px; line-height: 24px;
.h4-[xs, sm, md, lg, xl]        // font-size: 20px; line-height: 20px;
.h5-[xs, sm, md, lg, xl]        // font-size: 20px; line-height: 20px;
.body-[xs, sm, md, lg, xl]      // font-size: 16px; line-height: 24px;
.caption-[xs, sm, md, lg, xl]   // font-size: 14px; line-height: 16px;
.small-[xs, sm, md, lg, xl]     // font-size: 12px; line-height: 12px;

.secondary                      // opacity: 0.65
.disabled                       // opacity: 0.3

.white                          / color: #fff
.uppercase                      // text-transform: uppercase
```
