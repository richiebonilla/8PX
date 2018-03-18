Mini CSS Library that provides helper classes for spacing and displaying elements according to Bootstrap 4's breakpoints without writing any repetitive CSS.

The library assumes that your wireframes are designed using an 8pt grid system, so all margin/padding sizes are multiples of 8px.

Use .xshow and .xhide to control the display property of an element at a given breakpoint.
- .xhide will display the element at all breakpoints, but changing it to .xhide-sm will only hide it at the 'small' breakpoint and up.

Use the margin and padding classes to add box model properties in multiples of 8px.
- .xmt-3 will add a margin-top of 24px to the element
- .xpb-4 will add a padding-bottom of 32px to the element
- .xmx-5 will add a margin-left and margin-right of 40px to the element

Use the 'u' suffix for multiples under 10 to increment by 4px instead of 8px
- .xmt-3 = margin-top of 24px, while .xmt-3u = margin top of 28px

Add breakpoints to the classes to add responsive margins and paddings
- .xmr-sm3 = margin-right of 24px for breakpoints 'sm' and up

# Full List of Available Classes

**Margin & Padding Classes**
```
.x (the x prefix starts all classes in Eightpx to avoid conflicts)
.xm[t, r, b, l, x, y]-[1-40] 
.xm[t, r, b, l, x, y]-[sm, md, lg, xl][1-40]

.xp[t, r, b, l, x, y]-[1-40] 
.xp[t, r, b, l, x, y]-[sm, md, lg, xl][1-40]

.xmauto-[xs, sm, md, lg, xl] // margin: auto
.xmintial-[xs, sm, md, lg, xl] // margin: initial
```

**Display Classes**
```
.xshow // display: block
.xshow-[sm, md, lg, xl] // display: block
.xshow-ib // display: inline-block
.xshow-i // display: inline

.xhide // display: none
.xhide-[sm, md, lg, xl] // display: none
```

**Text Align Classes**
```
.xta[l, r, c] // text-align: [left, right, center]
``` 

**Typography Classes**
```
.h1-[xs, sm, md, lg, xl]  // font-size: 36px; line-height: 36px;
.h2-[xs, sm, md, lg, xl]  // font-size: 28px; line-height: 28px;
.h3-[xs, sm, md, lg, xl]  // font-size: 24px; line-height: 24px;
.h4-[xs, sm, md, lg, xl]  // font-size: 20px; line-height: 20px;
.h5-[xs, sm, md, lg, xl]  // font-size: 20px; line-height: 20px;
.body-[xs, sm, md, lg, xl]  // font-size: 16px; line-height: 24px;
.caption-[xs, sm, md, lg, xl]  // font-size: 14px; line-height: 16px;
.small-[xs, sm, md, lg, xl]  // font-size: 12px; line-height: 12px;

.secondary // opacity: 0.65
.disabled // opacity: 0.3

.white // color: #fff
.uppercase // text-transform: uppercase
```