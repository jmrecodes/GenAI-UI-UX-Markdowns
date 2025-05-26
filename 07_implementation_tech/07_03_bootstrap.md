# 7.3 Bootstrap

Bootstrap is a comprehensive component-based front-end framework. It provides pre-styled components (like buttons, forms, navigation) and a responsive grid system. Customization is typically done by overriding default CSS styles or using its Sass variables.

**Strengths:** Fast prototyping, pre-built components, responsive grid included, good documentation.
**Considerations:** Can be less flexible than utility-first CSS, requires overriding styles for significant design changes.

### Code Concept Example (Basic Button with States):

This example shows how Bootstrap's predefined classes are used. The customization aligns with the source's color definition principle by conceptually showing how Bootstrap's theme variables could be overridden.

```html
<button type="button" class="btn btn-primary">
  Click Me
</button>

<button type="button" class="btn btn-outline-secondary">
  Learn More
</button>

<button type="button" class="btn btn-primary" disabled>
  Disabled
</button>

```sass
// Conceptual Bootstrap Customization (Illustrative - not directly in sources, but aligns with defining variables):
/* styles.scss (using Sass to customize Bootstrap variables) */

// Override Bootstrap's default theme colors
$primary: #007bff; // Aligning with source's primary color
$secondary: #ced4da; // Aligning with source's secondary/border color
$success: #28a745; // Example functional color
$danger: #dc3545; // Example functional color (error)
$light: #f8f9fa;
$dark: #343a40;

// Override spacing scale
$spacer: 1rem; // Default Bootstrap spacer (often 16px). Can be adjusted.
$spacers: ( // Can define specific values based on source's scale
  0: 0,
  1: ($spacer * .25), // 4px if $spacer is 16px
  2: ($spacer * .5),  // 8px
  3: $spacer,         // 16px
  4: ($spacer * 1.5), // 24px
  5: ($spacer * 3)    // 48px
);

// Import Bootstrap's SCSS to compile with overrides
@import '~bootstrap/scss/bootstrap';

/* Additional custom styles if needed */
.btn:focus {
    box-shadow: 0 0 0 0.25rem rgba(0, 105, 216, 0.25); /* Ensure consistent focus visibility */
}

Explanation: Bootstrap provides classes like btn, btn-primary, btn-outline-secondary, and the disabled attribute, which encapsulate the styling and state behaviors defined in the sources. These classes handle padding (related to spacing principles), background/text colors (related to color principles), border radius, and built-in transitions and state styles (:hover, :focus, :active, :disabled). Customization aligns with defining color palettes and potentially spacing by overriding Bootstrap's default Sass variables before compiling. The focus style is often sufficiently visible by default in modern Bootstrap versions, supporting keyboard accessibility, but can be explicitly styled if needed. Semantic <button> tags are used.