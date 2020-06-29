# [Learning Advanced CSS & Sass: Flexbox, Grid, Animations, etc.](https://www.udemy.com/course/advanced-css-and-sass/)

### Building the header

- The best way to perform a basic reset using the universal selector.
- How to set project-wide font definitions.
- How to clip parts of elements using [`clip-path`](https://developer.mozilla.org/en-US/docs/Web/CSS/clip-path).
  <br /><br />
- The easiest way to center anything with the [`transform`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform), [`top`](https://developer.mozilla.org/en-US/docs/Web/CSS/top) and [`left`](https://developer.mozilla.org/en-US/docs/Web/CSS/left) properties.

### CSS animations

- How to create CSS animations using [`@keyframes`](https://developer.mozilla.org/en-US/docs/Web/CSS/@keyframes) and the [`animation`](https://developer.mozilla.org/en-US/docs/Web/CSS/animation) property.

### Building a complex animated button

- What pseudo-elements and pseudo-classes are.
- How and why to use the [`::after`](https://developer.mozilla.org/en-US/docs/Web/CSS/::after) pseudo-element;
- How to create a creative hover animation using the [`transition`](https://developer.mozilla.org/en-US/docs/Web/CSS/transition) property.
  <br />

---

### The 3 pillars to writing good HTML and CSS

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

### The Cascade and Specificity

- **Cascade**: the process of combining different stylesheets and resolving conflicts between different CSS rules and declarations when more than one rule applies to a certain element.

- To resolve conflicts between conflicting declarations, the Cascade first looks at the **importance (weight)**, then at the **selector specificity**, and lastly at the **source order**.

<br>

- **Importance**
  - User `!important` declarations
  - Author `!important` declarations
  - Author declarations
  - User declarations
  - Default browser declarations

<br>

- **Specificity**
  - Inline styles
  - IDs
  - Classes, pseudo-classes, attribute
  - Elements, pseudo-elements

<br>

- **Source order**
  - The last declaration in the code will override all other and will be applied.

---

- CSS declarations marked with `!important` have the highest priority.
- But, only use `!important` as a last resource. It's better to use correct specificities – **more maintainable code**!
- Inline styles will always have priority over styles in external stylesheets.
- A selector that contains **1** ID is more specific than one with **1000** classes.
- A selector that contains **1** class is more specific than one with **1000** elements.
- The universal selector `*` has no specificity value (0, 0, 0, 0).
- Rely more on **specificity** than on the **order** of selectors.
- But, rely on order when using 3rd-party stylesheets – always put your author stylesheet last.

### How CSS values are processed

- Each property has an initial value, used if nothing is declared (and if there is no inheritance).
- Browsers specify a **root `font-size`** for each page (usually `16px`).
- Percentages and relative values are always converted to pixels.
- Percentages are measured relative to their parent's **`font-size`**, if used to specify `font-size`.
- Percentages are measured relative their parent's **`width`**, if used to spefify lengths.
- `em` are measured relative to their **parent** `font-size`, if used to specify `font-size`.
- `em` are measured relative to the **current** `font-size`, if used to specify lengths.
- `rem` are always measured relative to the **document's root** `font-size`.
- `vh` and `vw` are simply percentage measurements of the viewport's `height` and `width`.

### Inheritance

- Inheritance passes the values for some specific properties from parents to children – **more maintainable code**.
- Properties related to text are inherited: `font-family`, `font-size`, `color`, etc. Other properties like `padding` and `margin` are not inherited.
- The computed value of a property is what gets inherited, **not** the declared value.
- Inheritance of a property only works if no one declares a value for that property.
- The `inherit` keyword forces inheritance on a certain property.
- The `initial` keyword resets a property to its initial value.

### Converting a px to a rem – An effective workflow

- How and why to use `rem` units.
- A great workflow for converting `px` to `rem`.

### How CSS renders a website

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

### Box Types

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

### Positioning schemes

- **Normal flow**
  - Default positioning scheme
  - **NOT** floated
  - **NOT** absolutely positioned
  - Elements laid out according to their source order
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

### The Think-Build-Architect Mindset

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
