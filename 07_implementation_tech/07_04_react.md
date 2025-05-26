# 7.4 React (Conceptual Component Example)

React is a JavaScript library for building user interfaces using components. In React, UI elements are typically represented as reusable components that manage their own state and render based on props. Styling can be handled in various ways (CSS, CSS Modules, Styled Components, Emotion, utility frameworks like Tailwind, etc.).

**Strengths:** Component-based architecture promotes reusability and maintainability, strong ecosystem.
**Considerations:** Requires understanding JavaScript/JSX, build process is necessary.

### Code Concept Example (Conceptual Button Component):

This example shows a functional React component for a button. It demonstrates how props could be used to handle button variants (primary, secondary), disabled state, and how styling (using conceptual CSS classes here, but could be other methods) would apply the principles from the sources. State logic like hover/focus appearance is typically handled by CSS pseudo-classes applied to the rendered element, while other states like disabled are controlled via props and conditional rendering/classes.

```javascript
import React from 'react';
// Assuming a CSS file (e.g., Button.module.css) or global CSS is used
// to define actual styles based on source principles
import styles from './Button.module.css'; // Example using CSS Modules

// Conceptual Functional Component
function Button({ variant = 'primary', disabled = false, onClick, children }) {
  // Determine base class and variant class based on props
  const baseClass = styles.btn; // Applies padding, transitions, basic font styles
  const variantClass = styles[`btn-${variant}`]; // Applies colors, borders based on variant

  // Conditional classes for states controlled by props
  const stateClasses = disabled ? styles['is-disabled'] : ''; // Example: apply disabled styles

  return (
    // Render semantic button tag
    <button
      className={`${baseClass} ${variantClass} ${stateClasses}`}
      onClick={onClick}
      disabled={disabled} // Standard disabled attribute
      // Accessibility attributes can be added if needed
    >
      {children} {/* Button text or content */}
    </button>
  );
}

// Example Usage:
// <Button variant="primary" onClick={() => alert('Primary clicked!')}>Submit</Button>
// <Button variant="secondary">Cancel</Button>
// <Button variant="primary" disabled>Processing...</Button>

```css
// Conceptual CSS Module (Button.module.css - illustrative, applies principles):
/* Use CSS Variables as defined in the brief for consistency */
/* Example variables (would typically be defined globally or imported) */
/* :root { --color-primary: #007bff; ... } */

.btn {
  display: inline-block;
  padding: var(--padding-base); /* Applying spacing from sources */
  font-size: 1rem;
  line-height: 1.5;
  text-align: center;
  text-decoration: none;
  border: 1px solid transparent;
  border-radius: var(--border-radius-base);
  cursor: pointer;
  transition: all 0.2s ease-in-out; /* Transitions for states */
  outline: none; /* Hide default outline */
  box-shadow: none;
}

.btn-primary {
  color: var(--color-text-light);
  background-color: var(--color-primary); /* Using color variable */
  border-color: var(--color-primary);
}

.btn-secondary {
  color: var(--color-primary);
  background-color: transparent;
  border-color: var(--color-secondary-border); /* Using color variable */
}

/* State styles using pseudo-classes where applicable */
.btn:hover {
  background-color: var(--color-primary-darker);
  border-color: var(--color-primary-darker);
}

.btn:focus {
  /* Clear focus indicator for keyboard navigation */
  box-shadow: 0 0 0 0.2rem rgba(0, 123, 255, 0.25);
}

.btn:active {
  background-color: var(--color-primary-active);
  border-color: var(--color-primary-active);
  transform: translateY(1px);
}

/* State style controlled by the component's `disabled` prop */
.is-disabled { /* Class applied conditionally by React component */
    opacity: 0.65;
    background-color: var(--color-disabled-bg);
    border-color: var(--color-disabled-bg);
    color: var(--color-disabled-text);
    cursor: not-allowed;
    pointer-events: none; /* Prevent interactions */
    box-shadow: none; /* No focus shadow */
}

Explanation: The React component renders a semantic <button> element. It accepts variant and disabled props to control its appearance and behavior, aligning with the concept of defining different button types and states in the brief. Styling is conceptually applied using CSS Modules, where classes like .btn, .btn-primary, and .is-disabled contain the actual CSS rules that implement color variables, spacing, transitions, and state styles. Pseudo-classes like :hover and :focus are handled directly in the CSS module, ensuring standard browser behavior and keyboard accessibility support. This approach separates structure (JSX), state logic (React component), and presentation (CSS), while collectively adhering to the design principles from the sources.