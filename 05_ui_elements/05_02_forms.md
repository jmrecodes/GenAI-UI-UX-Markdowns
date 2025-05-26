# 5.2 Forms (Text Inputs, Textareas)

Form inputs and their associated labels are components that require clear styling and state indication to ensure users understand what information is required and the current status of the input. [cite: 128] Labels must be correctly associated with inputs for accessibility, allowing screen readers to understand the form structure. [cite: 129] Visual space should clearly relate labels to their corresponding inputs. [cite: 130]

### Normal State:

* **Appearance:** A standard visual style for an empty or filled input field. [cite: 131] Typically includes a border (e.g., `border: 1px solid #ced4da;`), a background color (e.g., `background-color: #ffffff;`), and text color (e.g., `#333333`). [cite: 132] Labels (outside the input field) should be clearly associated using `<label>` tags and positioned consistently (e.g., above the input with less space below the label than above the input to visually group them). [cite: 133]
* **Transitions:** None from a static state. [cite: 134]

### Placeholder State (Input only):

* **Appearance:** Text inside the input indicating the expected input format or example value. [cite: 135]
* **Specifics:** Text color is lighter than the normal text color (e.g., `color: #6c757d;`). [cite: 135]
* **Transitions:** None. [cite: 136]

### Hover State:

* **Appearance:** Visual feedback when the mouse cursor is over the input or textarea. [cite: 137]
* **Specifics:** Border color might subtly change (e.g., `border-color: #a0a0a0;`). [cite: 138] Background color remains the same. [cite: 138]
* **Transitions:** `transition: border-color 0.2s ease-in-out;` [cite: 138]

### Focus State:

* **Appearance:** Indicates the input field that currently has keyboard focus. [cite: 139] Crucial for keyboard users. [cite: 139]
* **Specifics:** A prominent outline or `box-shadow` is applied (e.g., `border-color: #80bdff; box-shadow: 0 0 0 0.2rem rgba(0, 123, 255, 0.25);`). [cite: 140] The normal border might also change color. [cite: 140] This state clearly draws attention to the active input field. [cite: 141]
* **Transitions:** `transition: border-color 0.2s ease-in-out, box-shadow 0.2s ease-in-out;` [cite: 141]

### Error State:

* **Appearance:** Indicates that the input contains invalid data. [cite: 142] Should be visually distinct and communicated in more than one way (not just color) for accessibility. [cite: 143] Associated error messages should be provided near the input field, ideally below it, not in modal pop-ups. [cite: 144]
* **Specifics:** Border color changes to a red hue (e.g., `border-color: #dc3545;`). [cite: 145] An error icon might appear inside the input or next to it. [cite: 146] The label text associated with the input might also turn red (e.g., `color: #dc3545;`). [cite: 147] Error messages below the field are styled in red text. [cite: 147]
* **Transitions:** `transition: border-color 0.2s ease-in-out;` [cite: 148]

### Disabled State:

* **Appearance:** Indicates the input field is not currently editable. [cite: 149]
* **Specifics:** Background color changes to a light gray (e.g., `background-color: #e9ecef;`). [cite: 150] Text color is muted (e.g., `color: #6c757d;`). [cite: 150] Cursor changes to `not-allowed`. [cite: 150] No hover, focus, or error effects are applied. [cite: 150]
* **Transitions:** None.

### Filled State:

* **Appearance:** Indicates the input field contains data. [cite: 151] This is typically the same as the Normal state, unless specific design patterns require different styling (e.g., a clear indicator that the field is populated). [cite: 152]
* **Specifics:** Text color is the standard text color (e.g., `#333333`). [cite: 152] Placeholder text is no longer visible. [cite: 152]
* **Transitions:** None. [cite: 152]