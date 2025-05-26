# 7.1 Vanilla HTML/CSS/JS

This approach uses the fundamental building blocks of the web. It requires direct implementation of all styles, layouts, and interactions using HTML for structure, CSS for presentation and states, and JavaScript for dynamic behavior and complex interactions.

**Strengths:** Full control, no framework overhead, direct application of web standards.
**Considerations:** Requires manual implementation of design system elements, potentially more CSS to manage for large projects.

### Code Concept Example (Basic Button with States):

This example shows how CSS variables (aligning with source color/spacing principles) and state pseudo-classes (`:hover`, `:focus`) with transitions (aligning with source UI interaction principles) would be used.

```html
<button class="btn btn-primary">Click Me</button>
<button class="btn btn-secondary">Learn More</button>
<button class="btn btn-primary" disabled>Disabled</button>

```css
/* CSS: Using variables for colors and spacing */
:root {
    --color-primary: #007bff; /* Example primary color from sources */
    --color-primary-darker: #0056b3; /* Example darker shade for hover/focus */
    --color-primary-active: #004085; /* Example darker shade for active */
    --color-text-light: #ffffff;    /* Example light text for primary button */
    --color-secondary-border: #007bff; /* Example border color for secondary */
    --color-text-dark: #333333;      /* Example dark text */
    --color-disabled-bg: #cccccc;    /* Example disabled background */
    --color-disabled-text: #666666;  /* Example disabled text */
    --spacing-unit: 8px;             /* Example base spacing unit */
    --padding-base: var(--spacing-unit) calc(var(--spacing-unit) * 2); /* Example padding */
    --border-radius-base: 4px;
}

.btn {
    display: inline-block;
    padding: var(--padding-base); /* Applying spacing principle */
    font-size: 1rem; /* Example font size, relative unit principle */
    line-height: 1.5; /* Example line height */
    text-align: center;
    text-decoration: none; /* No underline unless it's a link */
    border: 1px solid transparent;
    border-radius: var(--border-radius-base);
    cursor: pointer;
    /* Transition for states */
    transition: background-color 0.2s ease-in-out, border-color 0.2s ease-in-out, color 0.2s ease-in-out, opacity 0.2s ease-in-out;
    /* Focus outline for accessibility */
    outline: none; /* Hide default outline */
    box-shadow: none;
}

/* Primary button styling */
.btn-primary {
    color: var(--color-text-light);
    background-color: var(--color-primary); /* Using color variable */
    border-color: var(--color-primary);
}

/* Secondary button styling */
.btn-secondary {
    color: var(--color-primary);
    background-color: transparent;
    border-color: var(--color-secondary-border); /* Using color variable */
}

/* Hover state */
.btn:hover {
    background-color: var(--color-primary-darker); /* Apply darker shade for primary */
    border-color: var(--color-primary-darker);
    text-decoration: none;
}

.btn-secondary:hover {
     color: var(--color-text-light);
     background-color: var(--color-secondary-border); /* Fill background for secondary */
}


/* Focus state - must be visible and distinct for keyboard navigation */
.btn:focus {
    /* Use a clear outline or box-shadow as recommended */
    box-shadow: 0 0 0 0.2rem rgba(0, 123, 255, 0.25); /* Example focus indicator */
    /* Often combine with hover effects for consistency */
    background-color: var(--color-primary-darker);
    border-color: var(--color-primary-darker);
}

.btn-secondary:focus {
     color: var(--color-text-light);
     background-color: var(--color-secondary-border);
     box-shadow: 0 0 0 0.2rem rgba(0, 123, 255, 0.25);
}

/* Active state */
.btn:active {
     background-color: var(--color-primary-active); /* Apply even darker shade */
     border-color: var(--color-primary-active);
     transform: translateY(1px); /* Simulate press */
}

.btn-secondary:active {
     background-color: var(--color-primary-active);
     border-color: var(--color-primary-active);
     transform: translateY(1px);
}

/* Disabled state */
.btn:disabled {
    opacity: 0.65; /* Reduce opacity */
    background-color: var(--color-disabled-bg); /* Muted background */
    border-color: var(--color-disabled-bg);
    color: var(--color-disabled-text); /* Muted text */
    cursor: not-allowed; /* Indicate non-interactivity */
    pointer-events: none; /* Ensure no hover/focus/active effects */
    box-shadow: none; /* No focus shadow when disabled */
}

Explanation: This uses semantic <button> tags and defines styles directly in CSS. CSS variables (--color-primary, --spacing-unit, etc.) are used to centralize design tokens, supporting the brief's emphasis on defined colors and consistent spacing. State styles (:hover, :focus, :active, :disabled) are applied using CSS pseudo-classes, implementing the specified interaction feedback. Transitions are added for smooth visual changes. The focus state styling ensures keyboard accessibility is supported.