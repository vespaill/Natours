# [Learning Advanced CSS & Sass: Flexbox, Grid, Animations, etc.](https://www.udemy.com/course/advanced-css-and-sass/)

## Table of Contents
1. [Building a header](#Buildingaheader)
2. [CSS animations](#CSSanimations)
3. [Building a complex animated button](#Buildingacomplexanimatedbutton)
4. [The 3 pillars to writing good HTML and CSS](#The3pillarstowritinggoodHTMLandCSS)
5. [The Cascade and Specificity](#TheCascadeandSpecificity)
6. [How CSS values are processed](#HowCSSvaluesareprocessed)
7. [Inheritance](#Inheritance)
8. [CSS Units](#CSSUnits)
9. [How CSS renders a website](#HowCSSrendersawebsite)
10. [Box Types](#BoxTypes)
11. [Positioning schemes](#Positioningschemes)
12. [The Think-Build-Architect Mindset](#TheThink-Build-ArchitectMindset)
13. [What is Sass?](#WhatisSass)
14. [Sass syntax vs SCSS syntax](#SasssyntaxvsSCSSsyntax)
15. [Basic responsive design principles](#Basicresponsivedesignprinciples)
16. [Layout types](#Layouttypes)
17. [Building a Custom Grid with Floats](#BuildingaCustomGridwithFloats)
18. [Building the About Section](#BuildingtheAboutSection)

---

###  1. <a name='Buildingaheader'></a>Building the header
- The best way to perform a basic reset using the universal selector.
- Setting up project-wide font definitions.
- Clipping parts of elements using [`clip-path`](https://developer.mozilla.org/en-US/docs/Web/CSS/clip-path).
- The easiest way to center anything with the [`transform`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform), [`top`](https://developer.mozilla.org/en-US/docs/Web/CSS/top) and [`left`](https://developer.mozilla.org/en-US/docs/Web/CSS/left) properties.

###  2. <a name='CSSanimations'></a>CSS animations
- Creating CSS animations using [`@keyframes`](https://developer.mozilla.org/en-US/docs/Web/CSS/@keyframes) and the [`animation`](https://developer.mozilla.org/en-US/docs/Web/CSS/animation) property.

###  3. <a name='Buildingacomplexanimatedbutton'></a>Building a complex animated button
- Using [pseudo-classes and pseudo-elements](https://www.growingwiththeweb.com/2012/08/pseudo-classes-vs-pseudo-elements.html#:~:text=A%20pseudo%2Delement%20is%20a,classes%20of%20elements%20using%20JavaScript.) such as [`::after`](https://developer.mozilla.org/en-US/docs/Web/CSS/::after).
- Creating a hover animation using the [`transition`](https://developer.mozilla.org/en-US/docs/Web/CSS/transition) property.
  <br />

---
###  4. <a name='The3pillarstowritinggoodHTMLandCSS'></a>The 3 pillars to writing good HTML and CSS
- **Responsive design**
  - Fluid layouts
  - Media queries
  - Responsive images
  - Correct units
  - Desktop-first vs mobile-first
- **Maintainable and scalable code**
  - Clean
  - Easy-to-understand
  - Supports potential for future growth
  - Reusable
  - How to organize files
  - How to name classes
  - How to structure HTML
- **Web performance**
  - Make less HTTP requests
  - Write less code
  - Compress code
  - Use a CSS preprocessor
  - Use as few images as possible
  - Compress images

###  5. <a name='TheCascadeandSpecificity'></a>The Cascade and Specificity
- **Cascade**: the process of combining different stylesheets and resolving conflicts between different CSS rules and declarations when more than one rule applies to a certain element.
- To resolve conflicts between conflicting declarations, the Cascade first looks at the **importance (weight)**, then at the **selector specificity**, and lastly at the **source order**.
- **Importance**
  - User `!important` declarations
  - Author `!important` declarations
  - Author declarations
  - User declarations
  - Default browser declarations
- **Specificity**
  - Inline styles
  - IDs
  - Classes, pseudo-classes, attribute
  - Elements, pseudo-elements
- **Source order**
  - The last declaration in the code will override all other and will be applied.
- CSS declarations marked with `!important` have the highest priority.
- But, only use `!important` as a last resource. It's better to use correct specificities – **more maintainable code**!
- Inline styles will always have priority over styles in external stylesheets.
- A selector that contains **1** ID is more specific than one with **1000** classes.
- A selector that contains **1** class is more specific than one with **1000** elements.
- The universal selector `*` has no specificity value (0, 0, 0, 0).
- Rely more on **specificity** than on the **order** of selectors.
- But, rely on order when using 3rd-party stylesheets – always put your author stylesheet last.

###  6. <a name='HowCSSvaluesareprocessed'></a>How CSS values are processed
- Each property has an initial value, used if nothing is declared (and if there is no inheritance).
- Browsers specify a **root `font-size`** for each page (usually `16px`).
- Percentages and relative values are always converted to pixels.
- Percentages are measured relative to their parent's **`font-size`**, if used to specify `font-size`.
- Percentages are measured relative their parent's **`width`**, if used to spefify lengths.
- `em` are measured relative to their **parent** `font-size`, if used to specify `font-size`.
- `em` are measured relative to the **current** `font-size`, if used to specify lengths.
- `rem` are always measured relative to the **document's root** `font-size`.
- `vh` and `vw` are simply percentage measurements of the viewport's `height` and `width`.

###  7. <a name='Inheritance'></a>Inheritance
- Inheritance passes the values for some specific properties from parents to children – **more maintainable code**.
- Properties related to text are inherited: `font-family`, `font-size`, `color`, etc. Other properties like `padding` and `margin` are not inherited.
- The computed value of a property is what gets inherited, **not** the declared value.
- Inheritance of a property only works if no one declares a value for that property.
- The `inherit` keyword forces inheritance on a certain property.
- The `initial` keyword resets a property to its initial value.

###  8. <a name='CSSUnits'></a>[CSS Units](https://www.w3schools.com/cssref/css_units.asp)
- Absolute Lengths vs Relative Lengths.
- The `em` and `rem` units are practical in creating perfectly scalable layouts.

###  9. <a name='HowCSSrendersawebsite'></a>How CSS renders a website
- **The Visual Formatting Model**: an algorithm that calculates boxes and determines the layout of these boxes, for each element in the render tree, in order to determine the final layout of the page. It takes into account:
  - **Dimensions of boxes**: the box model.
  - **Box type**: inline, block, and inline-block.
  - **Positioning scheme**: floats and positioning.
  - **Stacking context**.
  - Other elements in the render tree.
  - Viewport size, dimensions of images, etc.<br><br>
- **The Box Model**:
  - **Content**: text, images, etc.
  - **Padding**: transparent area around the content, inside the box.
  - **Border**: goes around the padding and the content.
  - **Margin**: space between boxes.
  - **Fill area**: area that gets filled with background color or background image.

###  10. <a name='BoxTypes'></a>Box Types
- **Block-level boxes**
  - Elements formatted visually as blocks
  - 100% of parent's width
  - Vertically, one after another
  - Box-model applies as showed
    <pre><code>display: block
    (display: flex)
    (display: list-item)
    (display: table)</code></pre>
- **Inline-block boxes**
  - A mix of block and inline
  - Occupies only content's space
  - No line-breaks
  - Box-model applies as showed<br>
    `display: inline-block`<br><br>
- **Inline boxes**
  - Content is distributed in lines
  - Occupies only content's space
  - No line-breaks
  - No heights and widths
  - Paddings and margins only horizontal<br>
    `display: inline`

###  11. <a name='Positioningschemes'></a>Positioning schemes
- **Normal flow**
  - Default positioning scheme
  - **NOT** floated
  - **NOT** absolutely positioned
  - Elements laid out according to their source order<br>
    `position: relative`<br><br>
- **Floats**
  - **Element is removed from the normal flow.**
  - Text and inline elements will wrap around the floated element
  - The container will not adjust its height to the element
    <pre><code>float: left
    float: right</code></pre>
- **Absolute positioning**
  - **Element is removed from the normal flow**
  - No impact on surrounding content or elements
  - We use `top`, `bottom` and `right` to offset the element from its relatively positioned container
    <pre><code>position: absolute
    position: fixed</code></pre>

###  12. <a name='TheThink-Build-ArchitectMindset'></a>The Think-Build-Architect Mindset
1. **Think** about the layout of your webpage or web app before writing code.<br/>**Component Driven Design**:
   - **Modular building blocks** that make up interfaces.
   - Held together by the **layout** of the page.
   - **Re-usable** across a project, and between different projects.
   - **Independent**, allowing us to use them anywhere on the page.<br/><br/>
2. **Build** your layout in HTML and CSS with a consistent structure for naming classes.<br/>**BEM – Block Element Modifier**:
   - **BLOCK**: standalone component that is meaningful on its own.
   - **ELEMENT**: part of a block that has no standalone meaning.
   - **MODIFIER**: a different version of a block or an element.
   - Low-specificity selectors:<br/><pre><code>.block {}
     .block__element {}
     .block__element--modifier {}</code></pre>
3. Create a logical **architecture** for your CSS with files and folders.<br/>**The 7-1 Pattern**:
   - 7 different folders for partial Sass files, and 1 main Sass file to import all other files into a compiled CSS stylesheet:<br/><pre><code>base/
     components/
     layout/
     pages/
     themes/
     abstracts/
     vendors/</code></pre>

###  13. <a name='WhatisSass'></a>What is Sass?
- Sass is a CSS preprocessors; an extension of CSS that adds power and elegance to the basic language.
- Sass source code gets compiled into CSS code.
- Features:
  - **Variables** for reusable values such as colors, font-size, spacing, etc.
  - **Nesting** of selectors inside of one another, allowing us to write less code.
  - **Operators** for mathematical operations right inside of CSS.
  - **Partials and imports** to write CSS in different files and importing them all into one single file.
  - **Mixins** to write reusable pieces of CSS code.
  - **Functions** similar to mixins, but also produce a value that can be used later.
  - **Extends** to make different selectors inherit declarations that are common to all of them.
  - **Control directives** for writing complex code using conditionals and loops.

###  14. <a name='SasssyntaxvsSCSSsyntax'></a>Sass syntax vs SCSS syntax
- Sass syntax uses indentation instead of curly braces.
- SCSS syntax is closer to CSS; uses curly braces.

###  15. <a name='Basicresponsivedesignprinciples'></a>Basic responsive design principles
1. **Fluid grids and layouts**<br>To allow content to easily adapt to the current viewport width used to browse the website. Uses `%` rather than `px` for all layout-related lengths.

1. **Flexible/responsive images**<br>Images behave differently than text content, and so we need to ensure that they also adapt nicely to the current viewport.

1. **Media queries**<br>To change styles on certain viewport widths (breakpoints), allowing us to create different versions of our website for different widths.

###  16. <a name='Layouttypes'></a>Layout types
- Float layouts
- Flexbox
- CSS grid

###  17. <a name='BuildingaCustomGridwithFloats'></a>Building a Custom Grid with Floats
- Architecting and building a simple grid system.
- Using the [attribute selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors).
- Using the [`:not`](https://developer.mozilla.org/en-US/docs/Web/CSS/:not) pseudo-class.
- Using [`calc()`](https://developer.mozilla.org/en-US/docs/Web/CSS/calc) instead Sass operations to perform operations on different units.

### 18. <a name='BuildingtheAboutSection'></a>Building the About Section
- Thinking about components.
- Using utility classes.
- Using the [`background-clip`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-clip) property.
- [`transform`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform)ing multiple properties simultaneously.
- Using the [`outline-offset`](https://developer.mozilla.org/en-US/docs/Web/CSS/outline-offset) property together with [`outline`](https://developer.mozilla.org/en-US/docs/Web/CSS/outline).
- Styling elements that are NOT hovered while others are.
