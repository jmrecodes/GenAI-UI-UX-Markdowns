# 5.1 Buttons

Buttons are critical calls-to-action and interactive elements. [cite: 102] Their design should clearly indicate what is interactive and how to interact with it. [cite: 103] Consistency in button styles and states throughout the site is essential for usability and recognition. [cite: 104] Different types of buttons (primary, secondary, tertiary) should visually communicate their place in the page's hierarchy. [cite: 105]

### Normal State:

* **Appearance:** Defined by the specific button type (primary, secondary, etc.). [cite: 106] For instance, a primary button might have a solid, high-contrast background color (e.g., `#007bff` - a bright blue). [cite: 107] Secondary buttons might use outline styles or lower contrast backgrounds (e.g., `border: 1px solid #007bff`, `background: transparent`). [cite: 108] Text should have sufficient color contrast against the background. Font style, weight, and size should be consistent with defined text styles. [cite: 109]
* **Transitions:** None from a static state.

### Hover State:

* **Appearance:** Provides a visual cue when a mouse cursor is over the button, indicating interactivity. [cite: 110] This state helps users identify clickable elements, especially important as cursor changes don't work on touchscreens. [cite: 111]
* **Specifics:** Background color darkens (e.g., primary button background changes from `#007bff` to `#0056b3` - 10% darker blue). [cite: 112] Outline borders might become solid or thicker. Text color might change slightly for contrast, if needed. [cite: 113] A subtle `box-shadow` can be added or changed to give a sense of elevation. [cite: 113]
* **Transitions:** `transition: all 0.2s ease-in-out;` [cite: 114] (A common setting for smooth, quick feedback on hover).

### Focus State:

* **Appearance:** Indicates which element currently has keyboard focus. [cite: 115] This is critical for keyboard navigation accessibility. [cite: 116] The focus indicator should be clearly visible and easy for users to track. [cite: 117] It's often recommended to provide the same visual cue as the hover state or a stronger one. [cite: 118]
* **Specifics:** A distinct outline (e.g., `outline: 2px solid #0056b3;` or `box-shadow: 0 0 0 0.2rem rgba(0, 123, 255, 0.25);`) around the button. [cite: 119] The hover effects (background/text color change) could also be applied on focus for consistency. [cite: 119]
* **Transitions:** `transition: all 0.2s ease-in-out;` [cite: 120] (Allows the outline/shadow to appear smoothly).

### Active State:

* **Appearance:** Indicates the moment the button is pressed or activated (e.g., during a mouse click or keyboard press). [cite: 121] Provides immediate feedback to the user. [cite: 121]
* **Specifics:** Background color becomes even darker (e.g., `#004085` - 15% darker than normal). [cite: 122] Can include a slight downward vertical transform (`transform: translateY(1px);`) and a reduced `box-shadow` or no shadow to simulate being pressed down. [cite: 123]
* **Transitions:** `transition: all 0.1s ease-in-out;` [cite: 124] (A faster transition for instantaneous feedback).

### Disabled State:

* **Appearance:** Indicates the button is not currently interactive. [cite: 125] These elements should not be accessible via keyboard navigation. [cite: 125]
* **Specifics:** Reduced opacity (e.g., `opacity: 0.5;`). [cite: 126] Background and text colors might be muted (e.g., `background: #cccccc`, `text: #666666`). [cite: 126] Cursor changes to `not-allowed`. [cite: 126] No hover, focus, or active effects are applied. [cite: 126]
* **Transitions:** None. [cite: 127]