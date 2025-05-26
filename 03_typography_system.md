# 3. Typography System

* **Font Selection:** Use a clean typography style. Limit the design to one or two font families. Prefer sans serif typefaces for websites. [cite: 23, 24]
* **Text Styles:** Define a limited set of text styles (headers, body copy, captions, etc.) for consistency and improved user experience. [cite: 25] Use semantic naming conventions for text styles.
* **Sizing & Scaling:** Use relative sizes for text (e.g., em, rem), not absolute sizes (e.g., px). [cite: 26] Define a base font size (e.g., 16px) and a typographic scale for headings and other elements. [cite: 27] Ensure text can be resized up to 200% without loss of content or functionality (WCAG 2.0 Level AA). [cite: 28]
* **Line Spacing & Letter Spacing:** Provide enough space between lines of text (leading/line-height) for readability. [cite: 29] Set line-height proportionally (e.g., 1.4 or 1.6). [cite: 29] Use letter-spacing effectively, avoiding condensed or tightened adjustments that hinder readability. [cite: 30] Vertical divisions in layout grids should be based on the baseline grid composed from type size and leading. [cite: 30] Add letter-spacing to uppercase text for polish. [cite: 31]
* **Alignment:** Left-align body text for readability. [cite: 32] Text alignment creates stability and defines relationships. [cite: 32]
* **Emphasis:** Use typographic emphasis (bold, italics, color) sparingly to draw attention. [cite: 33] Convey emphasis in code using semantic tags like `<strong>` and `<em>` so it's available to software. [cite: 33] Use underlining only for links. [cite: 34] Differentiate content areas using varying weights or sizes of the same typeface while maintaining uniformity. [cite: 34] Font weight is a parameter to limit choices on. [cite: 35]
* **Hierarchy:** Use different typefaces, sizes, or styles to establish hierarchy and distinguish content. [cite: 36] Headings should be visually closer to the text that follows them than the text that precedes them. [cite: 37]

### Code Concept Notes:

* Define text styles using CSS classes or mixins: `.body-text { font-size: 1rem; line-height: 1.6; }`[cite: 38], `h1 { font-size: 2.5rem; line-height: 1.2; margin-bottom: ...; margin-top: ...; }`[cite: 39].
* Use semantic HTML tags like `<p>`, `<h1>` to `<h6>`, `<strong>`, `<em>`, `<li>`. [cite: 39]
* Apply letter spacing: `letter-spacing: 0.1em;` for uppercase text. [cite: 40]
* Ensure styles cascade correctly based on semantic structure. [cite: 40]