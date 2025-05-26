# 5.3 Navigation (Links)

Navigation elements, particularly links, guide users through the site. [cite: 153] Consistent cues for orientation and navigation are key. [cite: 154] Links should be easy to identify visually, in code, and through interaction. [cite: 155] States help users understand what is clickable, which link is currently active (current page), and which links they have previously visited. [cite: 156] Semantic markup (like `<nav>`, `role="navigation"`) is important for structure and accessibility. [cite: 156]

### Normal State:

* **Appearance:** Standard styling for a navigation link. [cite: 157] Can vary based on location (e.g., primary navigation vs. footer navigation). [cite: 158] Primary navigation links might be bold or a specific brand color, while footer links are less emphasized. [cite: 159] Underlining is often used for links in body text but can be omitted in navigation menus where location and context provide sufficient cues, though preserving underlines or using color/shape cues helps identification. [cite: 160] Text color and weight are defined here. [cite: 160]
* **Transitions:** None from a static state. [cite: 161]

### Hover State:

* **Appearance:** Visual feedback when the mouse cursor is over the link. [cite: 162]
* **Specifics:** Text color changes (e.g., to a darker or lighter shade of the normal color or a highlight color). [cite: 163] An underline might appear if not present normally. [cite: 164] Background color or a subtle background element might appear or change. [cite: 164]
* **Transitions:** `transition: color 0.2s ease-in-out, text-decoration-color 0.2s ease-in-out, background-color 0.2s ease-in-out;` [cite: 164]

### Focus State:

* **Appearance:** Indicates the navigation link with keyboard focus. [cite: 165] Essential for keyboard navigation. [cite: 165]
* **Specifics:** Uses a clear outline or `box-shadow` (e.g., `outline: 2px solid #007bff;` or `box-shadow: 0 0 0 0.2rem rgba(0, 123, 255, 0.25);`). [cite: 166] Hover effects are often also applied on focus. [cite: 166]
* **Transitions:** `transition: color 0.2s ease-in-out, text-decoration-color 0.2s ease-in-out, background-color 0.2s ease-in-out, outline 0.2s ease-in-out, box-shadow 0.2s ease-in-out;` [cite: 167]

### Active/Current Page State:

* **Appearance:** Indicates the link corresponding to the page the user is currently viewing. [cite: 168] Helps users know where they are within the site's structure. [cite: 169]
* **Specifics:** Text color might be a primary brand color. [cite: 170] Can include a visual indicator such as a thicker bottom border (`border-bottom: 2px solid #007bff;`), a change in font weight (e.g., `font-weight: bold;`), or a different background color. [cite: 171] Style changes for selected menu items are explicitly recommended. [cite: 171]
* **Transitions:** `transition: color 0.2s ease-in-out, border-bottom-color 0.2s ease-in-out, font-weight 0.2s ease-in-out, background-color 0.2s ease-in-out;` [cite: 172]

### Visited State:

* **Appearance:** For links in content areas (less common in main navigation), this indicates the user has previously visited the linked page. [cite: 173] Preserving this distinction is useful. [cite: 173]
* **Specifics:** Text color changes to a specific visited link color (e.g., `#6610f2` - a purple hue), distinct from the normal and active link colors. [cite: 174]
* **Transitions:** `transition: color 0.2s ease-in-out;` [cite: 174]

### Disabled State (less common for navigation):

* **Appearance:** If a navigation link is temporarily unavailable. [cite: 175]
* **Specifics:** Muted text color and `pointer-events: none;`. [cite: 175]
* **Transitions:** None. [cite: 175]