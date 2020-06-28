## [Learning Advanced CSS & Sass: Flexbox, Grid, Animations, etc.](https://www.udemy.com/course/advanced-css-and-sass/)

<h4><u>Building the header</u></h4>

- The best way to perform a basic reset using the universal selector.
- How to set project-wide font definitions.
- How to clip parts of elements using [`clip-path`](https://developer.mozilla.org/en-US/docs/Web/CSS/clip-path).
  <br /><br />
- The easiest way to center anything with the [`transform`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform), [`top`](https://developer.mozilla.org/en-US/docs/Web/CSS/top) and [`left`](https://developer.mozilla.org/en-US/docs/Web/CSS/left) properties.

<h4><u>CSS animations</u></h4>

- How to create CSS animations using [`@keyframes`](https://developer.mozilla.org/en-US/docs/Web/CSS/@keyframes) and the [`animation`](https://developer.mozilla.org/en-US/docs/Web/CSS/animation) property.

<h4><u>Building a complex animated button</u></h4>

- What pseudo-elements and pseudo-classes are.
- How and why to use the [`::after`](https://developer.mozilla.org/en-US/docs/Web/CSS/::after) pseudo-element;
- How to create a creative hover animation using the [`transition`](https://developer.mozilla.org/en-US/docs/Web/CSS/transition) property.
  <br />

---

<h4><u>The 3 pillars to writing good HTML and CSS</u></h4>

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

<h4><u>The Cascade and Specificity</u></h4>

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

<h4><u>How CSS values are processed</u></h4>

- Each property has an initial value, used if nothing is declared (and if there is no inheritance).
- Browsers specify a **root `font-size`** for each page (usually `16px`).
- Percentages and relative values are always converted to pixels.
- Percentages are measured relative to their parent's **`font-size`**, if used to specify `font-size`.
- Percentages are measured relative their parent's **`width`**, if used to spefify lengths.
- `em` are measured relative to their **parent** `font-size`, if used to specify `font-size`.
- `em` are measured relative to the **current** `font-size`, if used to specify lengths.
- `rem` are always measured relative to the **document's root** `font-size`.
- `vh` and `vw` are simply percentage measurements of the viewport's `height` and `width`.

<h4><u>Inheritance</u></h4>

- Inheritance passes the values for some specific properties from parents to children – **more maintainable code**.
- Properties related to text are inherited: `font-family`, `font-size`, `color`, etc. Other properties like `padding` and `margin` are not inherited.
- The computed value of a property is what gets inherited, **not** the declared value.
- Inheritance of a property only works if no one declares a value for that property.
- The `inherit` keyword forces inheritance on a certain property.
- The `initial` keyword resets a property to its initial value.

<h4><u>Converting a px to a rem – An effective workflow</u></h4>

- How and why to use `rem` units.
- A great workflow for converting `px` to `rem`.