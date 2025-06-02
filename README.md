---
description: cursor rule for usage of the web design brief for UI / UX related tasks
globs: 
alwaysApply: true
---
# Web Design System Brief for AI Code Generation

This repository contains a comprehensive and actionable Web Design System Brief, specifically tailored to serve as a direct input and central reference for AI code generators like Cursor. Its purpose is to ensure that generated code adheres to consistent, user-centric, and accessible design principles.

By organizing the brief into modular Markdown files, we aim to provide AI models with clear, precise, and targeted information, optimizing the accuracy and quality of code generation.

## Purpose & Philosophy

This brief goes beyond abstract design theory, translating fundamental web design concepts into measurable guidelines that are directly translatable into HTML, CSS, and UI/UX patterns. It prioritizes:

* **Simplicity & Consistency:** Streamlining design to focus on core purpose and maintaining standardized elements across the web presence.
* **Usability & Clarity:** Making information easy to see, process, and use, and ensuring logical content flow.
* **Accessibility (WCAG Compliance):** Adhering to Web Content Accessibility Guidelines (WCAG 2.0 Level AA as a baseline, striving for AAA) to ensure content is perceivable, operable, understandable, and robust for all users.
* **Actionable Specifications:** Providing concrete values, examples, and code concept notes to guide AI in generating precise and functional code.

## How to Use This Brief with AI Code Generators

To maximize the effectiveness of this brief, reference specific Markdown files or sections based on the code you need the AI to generate. This helps the AI focus on the most relevant design principles and specifications.

**General Approach:**

1.  **Identify the Component/Section:** Determine which part of the website or app you want to generate code for (e.g., a button, a navigation bar, a hero section).
2.  **Select Relevant Files:** Refer the AI to the specific Markdown files that contain the design guidelines for that component or section.
3.  **Specify Requirements:** Clearly state your requirements for the specific code (e.g., "Generate a primary button with a 'click' action using vanilla HTML/CSS").

**Example AI Prompt Snippet:**

```
"Generate a responsive navigation bar component.
Adhere to the design principles outlined in the given UI UX brief.

Ensure:
- It's a sticky header.
- Uses the specified font families.
- Collapses into a hamburger menu below 768px as described.
- All navigation links are keyboard accessible."
```

## Brief Structure & Table of Contents

This brief is organized into the following logical sections, each within its dedicated Markdown file(s):

* **`README.md`**: (You are here) Overview, purpose, and guide to using the brief.
* **`01_aesthetic_brand.md`**: Defines the overarching visual style, brand personality, and consistency principles.
* **`02_color_palette.md`**: Specifies color usage, defining primary, utility, secondary, and accent colors, along with accessibility contrast requirements and hex code documentation.
* **`03_typography_system.md`**: Details font selection, text styles, sizing, scaling (using relative units like `em`, `rem`), line spacing, letter spacing, alignment, emphasis, and hierarchy.
* **`/04_layout_whitespace/`**
    * **`04_00_overview.md`**: Covers fundamental whitespace functions, consistent spacing values, code organization for flow, and the use of grid systems (e.g., 12-column grid).
    * **`04_01_responsive.md`**: Details core principles of responsive layout, explicit breakpoint strategies (e.g., below 768px, below 600px), adaptation of navigation and grids, and general documentation practices for responsiveness.
* **`/05_ui_elements/`**
    * **`05_00_overview.md`**: (Contains general introduction for UI Elements & Interactions).
    * **`05_01_buttons.md`**: Defines specific appearance and transition details for Normal, Hover, Focus, Active, and Disabled states of buttons.
    * **`05_02_forms.md`**: Details states (Normal, Placeholder, Hover, Focus, Error, Disabled, Filled) for text inputs and textareas, emphasizing label association for accessibility.
    * **`05_03_navigation.md`**: Outlines states (Normal, Hover, Focus, Active/Current, Visited, Disabled) for navigation links, including visual cues and semantic markup.
    * **`05_04_js_behavior.md`**: Describes implied JavaScript behaviors like mobile menu toggles and dropdowns/accordions, focusing on class changes, CSS implementation, and ARIA attributes for accessibility.
    * **`05_05_variants.md`**: Introduces the concept of component variants beyond interaction states, providing examples like Card Component Variants (Default, Shadow, Primary/Brand, Image) and Input Field Variants (Error Message, Input with Icon, Inline Input).
* **`06_accessibility_hierarchy.md`**: Reinforces WCAG compliance, semantic HTML/ARIA roles, keyboard navigation, visual and code hierarchy, and language declarations.
* **`/07_implementation_tech/`**
    * **`07_00_overview.md`**: General introduction to implementation considerations and common principles for various tech stacks.
    * **`07_01_vanilla.md`**: Conceptual implementation examples for Vanilla HTML/CSS/JS.
    * **`07_02_tailwind.md`**: Conceptual implementation examples for Tailwind CSS.
    * **`07_03_bootstrap.md`**: Conceptual implementation examples for Bootstrap.
    * **`07_04_react.md`**: Conceptual implementation examples for React components.
* **`08_subtle_visual_details.md`**: Defines consistent guidelines for aesthetic elements like icons, shadows, and border-radius, supporting the overall minimalist aesthetic. (Note: This section includes external suggestions not found in the original source material, but aligns with design principles for consistency and usability.)

## Factors to consider when to include folder context and its files as referenced below

Make sure to base your decision on the factors below before deciding to include the detailed folder context after at **Folder location context**.

**Factors**

1. Will the prompted task benefit from the Web Design System Brief as overviewed above?
2. Did I discover a better approach or a good addition based on all of my interactions with the existing project to the current Web Design System Brief?
3. Based on the brief structure and table of contents provided, can I pinpoint at least one file being useful for me to access in order to give better results to the task at hand?

**Folder location context**

@folder /GenAI-UI-UX-Markdowns