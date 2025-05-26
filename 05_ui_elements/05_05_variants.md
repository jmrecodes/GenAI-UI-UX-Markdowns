# 5.5 Advanced UI Patterns

### Concept of Variants:

Beyond interaction states, components often require different base appearances depending on their role or prominence on the page. [cite: 195] These distinct appearances are called variants. [cite: 195] Defining these variants systematically ensures consistency across the web presence and helps communicate the component's purpose or hierarchy visually. [cite: 196] This is analogous to defining different button types (primary, secondary, tertiary) or styling navigation links differently based on their location (primary nav vs. footer). [cite: 197]

### Examples of Component Variants:

* **a. Card Component Variants (Component not explicitly detailed in sources, but variants concept applied using source principles):** While 'cards' are not specifically listed as a UI element in the sources like buttons or forms, they are a common web pattern. [cite: 198] We can define variants based on the brief's principles of using layout and whitespace to organize content, establishing visual hierarchy, and maintaining brand alignment. [cite: 199]
    * **Default Card:** A standard container for a block of content (e.g., text, image, link). [cite: 200]
        * **Appearance:** Defined border (e.g., `1px solid #cccccc`) or a subtle `box-shadow`, solid background (e.g., `#ffffff`). [cite: 201] Consistent padding internally using base unit scale (e.g., `16px` padding). [cite: 202]
        * **Use Case:** General content grouping. [cite: 202]
    * **Card with Shadow Variant (as requested):** Highlights specific content or interactive elements more prominently. [cite: 203]
        * **Appearance:** Adds a more pronounced `box-shadow` compared to the Default Card. Border might be omitted. Background remains consistent. [cite: 204]
        * **Use Case:** Featured content, clickable items like product previews, or cards in a grid where separation is needed. [cite: 205]
    * **Primary/Brand Card Variant:** Used for key calls-to-action or essential information blocks, aligning with the use of primary colors for calls to action and reflecting brand identity. [cite: 206]
        * **Appearance:** Could use a background color from the defined primary palette, with text color ensuring sufficient contrast (WCAG AA/AAA). [cite: 207] Might omit border and rely solely on background color and whitespace for separation. [cite: 208]
        * **Use Case:** Important alerts, featured services, or main calls-to-action presented in a card format. [cite: 209]
    * **Card with Image Variant:** A structural variant designed to accommodate media alongside text content. [cite: 210]
        * **Appearance:** Divides the internal layout using grid or flexbox to place an image on one side (top, left, or right) and text content on the other. [cite: 211] Maintains consistent padding. [cite: 212]
        * **Use Case:** Blog post previews, team member profiles, product listings. [cite: 212]
* **b. Input Field Variants (Extending from Forms):** The sources detail states for text inputs and textareas, including Normal, Placeholder, Hover, Focus, Error, Disabled, and Filled. [cite: 213] We can build upon this by defining structural or context-based variants. [cite: 214]
    * **Default Input:** The standard text input field as described in the sources. [cite: 215]
        * **Appearance:** Border, background color, text color as per Normal State. [cite: 216] Associated label positioned correctly. [cite: 217]
        * **Use Case:** Standard text entry in forms. [cite: 217]
    * **Error Message Variant for Input (as requested):** This isn't just a state applied to the input, but can be considered a variant of the form group itself or a component that includes the input and its associated error feedback. [cite: 217]
        * **Appearance:** The input field adopts the Error State styling (red border, potentially red label/text). [cite: 218] Crucially, an associated error message element is present and styled with a red text color, positioned near the input (preferably below). [cite: 219] An error icon might also be part of this variant. [cite: 220] This variant combines visual cues (color, icon) with textual feedback (message) for accessibility. [cite: 221]
        * **Use Case:** Displayed when form validation fails for a specific input field. [cite: 222]
    * **Input with Icon Variant:** Includes a leading or trailing icon within or alongside the input field. [cite: 223]
        * **Appearance:** Uses internal padding and potentially flexbox layout within the input's container to place an icon without overlapping text. [cite: 224] Icon color should have sufficient contrast. [cite: 225]
        * **Use Case:** Search inputs (magnifying glass icon), password fields (eye icon to toggle visibility), or inputs requiring specific data format (e.g., calendar icon for date pickers). [cite: 226]
    * **Inline Input Variant:** A more compact style suitable for forms embedded within text blocks or tables. [cite: 227]
        * **Appearance:** Reduced padding and margin compared to the Default Input. Border style might change (e.g., only a bottom border). [cite: 228]
        * **Use Case:** Filtering interfaces, small forms in headers or footers. [cite: 229]