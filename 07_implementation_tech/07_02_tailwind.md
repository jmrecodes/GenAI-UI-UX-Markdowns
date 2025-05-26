# 7.2 Tailwind CSS

Tailwind is a utility-first CSS framework. Instead of pre-designed components, it provides low-level utility classes (like `bg-blue-500`, `p-4`, `text-lg`) that can be composed directly in HTML to build custom designs. Design tokens are managed via a configuration file.

**Strengths:** Rapid styling, highly customizable via config, responsive utilities built-in.
**Considerations:** Can lead to verbose HTML, requires build process to purge unused CSS.

### Code Concept Example (Basic Button with States):

This example shows how Tailwind utility classes implement colors, spacing, states, and transitions, mapping to the principles defined in the sources. Tailwind's configuration file is where the source's color palette and spacing scale would be defined.

```html
<button class="btn bg-primary-500 text-white px-4 py-2 rounded
               hover:bg-primary-600 focus:ring focus:ring-primary-300
               active:bg-primary-700 disabled:opacity-50 disabled:cursor-not-allowed">
    Click Me
</button>

<button class="btn border border-secondary-500 text-secondary-700 px-4 py-2 rounded
               hover:bg-secondary-100 focus:ring focus:ring-secondary-300
               active:bg-secondary-200 disabled:opacity-50 disabled:cursor-not-allowed">
    Learn More
</button>

```javascript
// Conceptual Tailwind Config (Illustrative - not directly in sources, but aligns with defining colors/spacing):
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: { // Mapping to --color-primary concept
          100: '#e0f2ff',
          300: '#90cdf4', // For focus ring example
          500: '#007bff',
          600: '#0056b3', // For hover state
          700: '#004085', // For active state
        },
        secondary: { // Mapping to a secondary color concept
           100: '#f0f0f0', // For hover state
           200: '#e0e0e0', // For active state
           500: '#ced4da', // For border color
           700: '#333333', // Text color
        },
        disabled: { // Mapping to disabled color concept
           500: '#cccccc',
           700: '#666666',
        }
      },
      spacing: { // Mapping to spacing unit concept
        '1': '8px', // Example: 1 unit = 8px
        '2': '16px',
        '4': '32px',
      },
      // Transitions, Opacity, Cursor utilities are built-in but can be extended
    }
  },
  // ... other config
}

Explanation: The semantic <button> tag is used. Utility classes like bg-primary-500 directly apply background colors defined in the Tailwind config, aligning with the source's color specification. Spacing classes like px-4 and py-2 map to padding values derived from the configured spacing scale, supporting the consistent spacing principle. State variations (hover:bg-primary-600, focus:ring, disabled:opacity-50) are handled by prefixing utility classes, directly implementing the required state styles. The focus:ring utility provides a clear focus indicator for keyboard navigation.