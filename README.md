# [Learning Advanced CSS & Sass: Flexbox, Grid, Animations, etc.](https://www.udemy.com/course/advanced-css-and-sass/)

<h3><style>
  table td, table td * {
    vertical-align: top;
  }
</style><u>Building the header</u></h3>

- The best way to perform a basic reset using the universal selector.
- How to set project-wide font definitions.
- How to clip parts of elements using [`clip-path`](https://developer.mozilla.org/en-US/docs/Web/CSS/clip-path).
  <br /><br />
- The easiest way to center anything with the [`transform`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform), [`top`](https://developer.mozilla.org/en-US/docs/Web/CSS/top) and [`left`](https://developer.mozilla.org/en-US/docs/Web/CSS/left) properties.

<h3><u>CSS animations</u></h3>

- How to create CSS animations using [`@keyframes`](https://developer.mozilla.org/en-US/docs/Web/CSS/@keyframes) and the [`animation`](https://developer.mozilla.org/en-US/docs/Web/CSS/animation) property.

<h3><u>Building a complex animated button</u></h3>

- What pseudo-elements and pseudo-classes are.
- How and why to use the [`::after`](https://developer.mozilla.org/en-US/docs/Web/CSS/::after) pseudo-element;
- How to create a creative hover animation using the [`transition`](https://developer.mozilla.org/en-US/docs/Web/CSS/transition) property.
  <br />

---

<h3><u>The 3 pillars to writing good HTML and CSS</u></h3>

- <strong>Responsive design</strong>
  - <small>Fluid layouts</small>
  - <small>Media queries</small>
  - <small>Responsive images</small>
  - <small>Correct units</small>
  - <small>Desktop-first vs mobile-first</small>
- <strong>Maintainable and scalable code</strong>
  - <small>Clean</small>
  - <small>Easy-to-understand</small>
  - <small>Supports potential for future growth</small>
  - <small>Reusable</small>
  - <small>How to organize files</small>
  - <small>How to name classes</small>
  - <small>How to structure HTML</small>
- <strong>Web performance</strong>
  - <small>Make less HTTP requests</small>
  - <small>Write less code</small>
  - <small>Compress code</small>
  - <small>Use a CSS preprocessor</small>
  - <small>Use as few images as possible</small>
  - <small>Compress images</small>

<h3><u>The Cascade and Specificity</u></h3>

- <strong>Cascade</strong>: the process of combining different stylesheets and resolving conflicts between different CSS rules and declarations when more than one rule applies to a certain element.

- To resolve conflicts between conflicting declarations, the Cascade first looks at the **importance (weight)**, then at the **selector specificity**, and lastly at the **source order**.

<table>
  <tr>
    <td><strong>Importance</strong></td>
    <td><strong>Specificity</strong></td>
    <td><strong>Source order</strong></td>
  </tr>
  <tr>
    <td>
      <ol>
        <li>User <code>!important</code> declarations</li>
        <li>Author <code>!important</code> declarations</li>
        <li>Author declarations</li>
        <li>User declarations</li>
        <li>Default browser declarations</li>
      </ol>
    </td>
    <td>
      <ol>
        <li>Inline styles</li>
        <li>IDs</li>
        <li>Classes, pseudo-classes, attribute</li>
        <li>Elements, pseudo-elements</li>
      </ol>
    </td>
    <td>
      The last declaration in the code will override all other declarations and will be applied.
    </td>
  </tr>
</table>

- CSS declarations marked with `!important` have the highest priority.
- But, only use `!important` as a last resource. It's better to use correct specificities – **more maintainable code**!
- Inline styles will always have priority over styles in external stylesheets.
- A selector that contains **1** ID is more specific than one with **1000** classes.
- A selector that contains **1** class is more specific than one with **1000** elements.
- The universal selector `*` has no specificity value (0, 0, 0, 0).
- Rely more on **specificity** than on the **order** of selectors.
- But, rely on order when using 3rd-party stylesheets – always put your author stylesheet last.

<h3><u>How CSS values are processed</u></h3>

- Each property has an initial value, used if nothing is declared (and if there is no inheritance).
- Browsers specify a **root `font-size`** for each page (usually `16px`).
- Percentages and relative values are always converted to pixels.
- Percentages are measured relative to their parent's **`font-size`**, if used to specify `font-size`.
- Percentages are measured relative their parent's **`width`**, if used to spefify lengths.
- `em` are measured relative to their **parent** `font-size`, if used to specify `font-size`.
- `em` are measured relative to the **current** `font-size`, if used to specify lengths.
- `rem` are always measured relative to the **document's root** `font-size`.
- `vh` and `vw` are simply percentage measurements of the viewport's `height` and `width`.

<h3><u>Inheritance</u></h3>

- Inheritance passes the values for some specific properties from parents to children – **more maintainable code**.
- Properties related to text are inherited: `font-family`, `font-size`, `color`, etc. Other properties like `padding` and `margin` are not inherited.
- The computed value of a property is what gets inherited, **not** the declared value.
- Inheritance of a property only works if no one declares a value for that property.
- The `inherit` keyword forces inheritance on a certain property.
- The `initial` keyword resets a property to its initial value.

<h3><u>Converting a px to a rem – An effective workflow</u></h3>

- How and why to use `rem` units.
- A great workflow for converting `px` to `rem`.

<h3><u>How CSS renders a website</u></h3>

- **The Visual Formatting Model**: an algorithm that calculates boxes and determines the layout of these boxes, for each element in the render tree, in order to determine the final layout of the page. <br /><br />Takes into account:

  - **Dimensions of boxes**: the box model.
  - **Box type**: inline, block, and inline-block.
  - **Positioning scheme**: floats and positioning.
  - **Stacking context**.
  - Other elements in the render tree.
  - Viewport size, dimensions of images, etc.

- **The Box Model**:

  - **Content**: text, images, etc.
  - **Padding**: transparent area around the content, inside the box.
  - **Border**: goes around the padding and the content.
  - **Margin**: space between boxes.
  - **Fill area**: area that gets filled with background color or background image.

- **Box types**:
  <table>
  <tr>
    <td><strong>Block-level boxes</strong></td>
    <td><strong>Inline-block boxes</strong></td>
    <td><strong>Inline boxes</strong></td>
  </tr>
  <tr>
    <td>
    <ul>
      <li>Elements formatted visually as blocks.</li>
      <li>100% of parent's width.</li>
      <li>Vertically, one after another.</li>
      <li>Box-model applies as showed.</li>
    </ul>
    <pre><code> display: block
  (display: flex)
  (display: list-item)
  (display: table)
    </code></pre>
    </td>

    <td>
    <ul>
      <li>A mix of block and inline.</li>
      <li>Occupies only content's space.</li>
      <li>No line-breaks.</li>
      <li>Box-model applies as showed.</li>
    </ul>
    <pre><code>display: inline-block</code></pre>
    </td>

    <td><ul>
      <li>Content is distributed in lines.</li>
      <li>Occupies only content's space.</li>
      <li>No line-breaks.</li>
      <li>No heights and widths.</li>
      <li>Paddings and margins only horizontal.</li>
    </ul>
    <pre><code>display: inline</code></pre>
    </td>
  </tr>
  </table>

- **Positioning schemes**:
  <table>
  <tr>
    <td><strong>Normal flow</strong></td>
    <td><strong>Floats</strong></td>
    <td><strong>Absolute positioning</strong></td>
  </tr>
  <tr>
    <td>
    <ul>
      <li>Default positioning scheme.</li>
      <li><strong>NOT</strong> floated.</li>
      <li><strong>NOT</strong> absolutely positioned.</li>
      <li>Elements laid out according to their source order.</li>
    </ul>
    <pre><code>position: relative</code></pre>
    </td>

    <td>
    <ul>
      <li><strong>Element is removed from the normal flow.</strong></li>
      <li>Text and inline elements will wrap around the floated element.</li>
      <li>The container will not adjust its height to the element.</li>
    </ul>
    <pre><code>float: left
  float: right</code></pre>
    </td>

    <td><ul>
      <li><strong>Element is removed from the normal flow</strong>.</li>
      <li>No impact on surrounding content or elements.</li>
      <li>We use <code>top</code>, <code>bottom</code> and <code>right</code> to offset the element from its relatively positioned container</li>
    </ul>
    <pre><code>position: absolute
  position: fixed</code></pre>
    </td>
  </tr>
  </table>

<br /><h3><u>The Think-Build-Architect Mindset</u></h3>

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
    .block__element--modifier {}</code></pre><br/>
3. Create a logical **architecture** for your CSS with files and folders.<br/>**The 7-1 Pattern**:
    - 7 different folders for partial Sass files, and 1 main Sass file to import all other files into a compiled CSS stylesheet:<br/><pre><code>base/
    components/
    layout/
    pages/
    themes/
    abstracts/
    vendors/</code></pre>
