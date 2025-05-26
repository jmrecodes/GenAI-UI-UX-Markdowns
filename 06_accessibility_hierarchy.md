# 6. Accessibility & Hierarchy

* **WCAG Compliance:** Design and code should adhere to WCAG 2.0 guidelines (Perceivable, Operable, Understandable, Robust)[cite: 229]. Ensure content can be interpreted reliably by a wide variety of user agents, including assistive technologies[cite: 230]. Aim for AA conformance as a baseline, striving for AAA where possible[cite: 231].
* **Semantic Structure:** Use semantic HTML and WAI-ARIA roles to convey information, structure, and relationships in code (WCAG 1.3.1 Level A)[cite: 232]. Ensure the reading sequence is programmatically determinable where meaning is affected (WCAG 1.3.2 Level A)[cite: 233]. Use standard web technologies and code to standards[cite: 234]. Ensure elements have complete start/end tags, are nested correctly, have unique IDs, etc. (WCAG 4.1.1 Level A)[cite: 234]. Name, role, and value of UI components must be programmatically determinable (WCAG 4.1.2 Level A)[cite: 235].

    ### Example Code Concept (Semantic Structure):

    ```html
    <article>
      <h1>Article Title</h1>
      <p>Introduction...</p>
      <section>
        <h2>Section Heading</h2>
        <p>Section content...</p>
      </section>
    </article>
    ```

* **Keyboard Navigation:** Ensure all content and interactive elements are accessible and usable via keyboard (WCAG 2.0 Guideline 2.1 - Keyboard Accessible, Level A)[cite: 237]. Include skip links to bypass blocks of content[cite: 238]. Ensure focus indicators are visible[cite: 238].

    ### Example Code Concept (Focus Indicator - ensure this is visible/styled):

    ```css
    *:focus {
      outline: 2px solid blue; /* Example style */
      outline-offset: 2px;
    }
    ```

* **Visual Hierarchy:** Establish a clear visual hierarchy to guide users through content[cite: 240]. Use a combination of scale, space, position, typography, color, and contrast to indicate importance and relationships[cite: 241]. Elements higher in the hierarchy can be larger, bolder, in a distinctive color, set off by more whitespace, or placed nearer the top[cite: 242].
* **Code Hierarchy:** Separate visual hierarchy (CSS) from document hierarchy (HTML tags)[cite: 243]. Use headings (`<h1>` through `<h6>`) for logical document structure, not just visual styling[cite: 244]. Headings should form a clear outline[cite: 244]. Visually style headings with CSS[cite: 245].

    ### Example Code Concept (Separating Structure and Style):

    ```html
    <h1>Main Page Title</h1>
    <section>
      <h2>Section One</h2>
      <p>...</p>
    </section>
    <section>
      <h2>Section Two</h2>
      <h3>Subsection A</h3>
      <p>...</p>
    </section>
    ```

    ```css
    /* CSS for visual styling */
    h1 { font-size: 3rem; color: var(--color-text-heading); }
    h2 { font-size: 2rem; color: var(--color-text-heading); margin-top: 40px; margin-bottom: 10px; } /* Example spacing relative to surrounding text */
    h3 { font-size: 1.5rem; color: var(--color-text-heading); margin-top: 20px; margin-bottom: 5px; }
    ```

* **Language:** Ensure the human language of the page and significant passages can be programmatically determined (WCAG 3.1.1/3.1.2 Level A/AA)[cite: 249]. Write content in plain language appropriate for the audience (WCAG 3.1 Understandable Principle)[cite: 250]. Provide definitions for unusual words or abbreviations (Level AAA)[cite: 250].

    ### Example Code Concept (Language Declaration):

    ```html
    <html lang="en">
      <body>
        <p>Some text in English.</p>
        <p><span lang="es">Algún texto en español.</span></p>
      </body>
    </html>
    ```

* **Accessibility Requirements Documentation:** Capture requirements for implementing an accessible component or pattern[cite: 251].
* **Integrated Process:** Accessibility should be integral to the practice of every member of the product team, not just a final step ("peanut butter")[cite: 252]. Include people with disabilities in usability work[cite: 252].
* **Testing:** Test sites often and continually smooth out confusing parts[cite: 253]; this is one of the most effective ways to make them more accessible[cite: 254]. Conduct usability testing for accessibility[cite: 254].