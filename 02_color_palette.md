# 2. Color Palette

* **Purpose:** Use color to separate foreground from background and as an organizational tool[cite: 13]. Define primary, utility, and secondary/accent colors[cite: 13]. Utility colors should be used for copy and headers[cite: 13]. Use functional colors (e.g., red for errors, green for success)[cite: 14]. Define acceptable use cases for each color[cite: 14]. Calls to action should use primary colors[cite: 15].
* **Accessibility - Contrast:** Ensure sufficient color contrast for legibility[cite: 16]. Meet WCAG 2.0 Level AA contrast ratio: 4.5:1 for normal text and 3:1 for large text[cite: 16]. Aim for Level AAA (7:1 / 4.5:1) where possible[cite: 17]. Avoid small, low-contrast type[cite: 17]. Avoid gray text on colored backgrounds[cite: 17].
* **Avoid Color Alone:** Never rely on color alone to convey functional meaning (e.g., for sections)[cite: 18]. Combine colors with borders, rules, or whitespace where necessary[cite: 19].
* **Specification:** Document hex values (e.g., #RRGGBB), names, and acceptable use cases for each color[cite: 20]. Include guidelines (do's and don'ts) for each color[cite: 20].

### Code Concept Notes:

* Define colors using CSS variables for consistency: `--color-primary: #HEXCODE; --color-text: #HEXCODE;` etc[cite: 21].
* Apply colors using these variables: `color: var(--color-text); background-color: var(--color-primary);`[cite: 22].
* Use tools to check contrast ratios during development[cite: 22].