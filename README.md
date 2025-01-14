
# Notebook-Themed Marp Slide Deck

## Contribution to Marp Ecosystem

This project introduces a custom **notebook-inspired theme** for Marp slide decks, tailored for creating visually appealing and structured academic presentations. The theme prioritizes readability, clean aesthetics, and unique styles for specific slide components like title slides, pseudocode blocks, and KaTeX-rendered mathematics. Below is an outline of the core contributions made through this theme:

### Key Features of the Theme

1. **Typography Customization**
   - Utilizes two unique Google Fonts: **Patrick Hand** for the main content and **Concert One** for headings, offering a playful and handwritten notebook aesthetic.
   - Ensures consistent font sizes, spacing, and styles across different slide elements for a polished presentation.

2. **Title Slide Design**
   - Features a **lined paper background** with customizable title blocks, adding a visually distinct "notebook feel."
   - Includes customizable sticky-note elements for subtitles and placeholders for branding (e.g., institutional logos).

3. **Custom Components**
   - **Pseudo-code blocks** styled with a handwritten look, pastel colors, and subtle rotation to simulate notebook-style notes.
   - **KaTeX integration** seamlessly styled with notebook-style fonts to keep equations consistent with the overall theme.
   - **Pagination** using styled arrow markers for intuitive navigation through the slide deck.

4. **Color and Aesthetic Enhancements**
   - Themed background colors for both title slides and regular slides (e.g., pastel greens and whites).
   - Custom-styled table rows for structured data, with alternate row coloring for better readability.
   - Inline support for colored text using predefined CSS classes like `.text-green` and `.text-red`.

5. **Flexibility for Academic Use**
   - **Two-column layouts** for splitting content, supporting both textual and visual (e.g., image) elements side-by-side.
   - **TOC slide styling** to present structured overviews with a multi-column format.
   - Designed with academic users in mind, enabling clean integration of algorithms, charts, and data structures.

### CSS Innovations in the Theme

- **Notebook Style:** 
  - Implemented a dotted background for content slides to resemble notebook pages, enhancing the "notebook" aesthetic.
  - Borders and shadow effects for tables, sticky notes, and pseudocode blocks to match academic presentation needs.

- **Advanced Features:** 
  - Support for multiple custom backgrounds like lined paper, sticky notes, and colored elements.
  - Built-in support for responsive layouts to handle varying content sizes.

### Usage

1. Import the `notebook.css` theme in your Marp slide deck:
   ```yaml
   ---
   marp: true
   theme: notebook
   math: katex
   paginate: true
   ---
   ```

2. Include the theme's CSS:
   ```html
   <link rel="stylesheet" href="path/to/notebook.css">
   ```

3. Use the predefined classes for consistent styles:
   - **Tables:** Wrap tables with `cute-table-container` for styling.
   - **Two Columns:** Use `.columns` with `.left-col` and `.right-col` for content splitting.
   - **Custom Colors:** Use `.text-green` and `.text-red` for color-coding elements.

### Screenshot Previews

#### Title Slide
![Title Slide](/assets/tiltle_example.png)
*(Example: Notebook-style title page with sticky note subtitle)*

#### Pseudocode Block
![Pseudocode Block](/assets/tiltle_example.png)
*(Notebook-themed pseudocode with pastel background and dashed border)*

#### KaTeX Integration
```css
/* KaTeX styling overrides to use Patrick Hand. */
.katex {
    font-family: 'Patrick Hand', cursive, sans-serif !important;
}

.katex .mathnormal,
.katex .mathrm,
.katex .mathit {
    font-family: 'Patrick Hand', cursive, sans-serif !important;
    font-weight: normal !important;
    font-size: 1em !important;
    line-height: 1.2 !important;
}

.katex .mbin,
.katex .mrel {
    font-family: 'Patrick Hand', cursive, sans-serif !important;
}

.katex .mop {
    margin-left: 0.2em;
}

.katex .mopen,
.katex .mclose {
    margin: 0 0.08em;
}

/* Smaller subscripts & superscripts */
.katex .scriptstyle .mord,
.katex .scriptscriptstyle .mord,
.katex .scriptstyle .mord *,
.katex .scriptscriptstyle .mord *,
.katex .scriptstyle .vlist *,
.katex .scriptscriptstyle .vlist * {
    font-family: 'Patrick Hand', cursive, sans-serif !important;
    font-size: 0.8em !important;
    line-height: 1.2 !important;
    margin-left: 0.05em !important;
}

.katex .operatorname {
    font-family: 'Patrick Hand', cursive, sans-serif !important;
}

.katex .textstyle {
    font-family: 'Patrick Hand', cursive, sans-serif !important;
}

/* Adjust vertical offset for KaTeX's vlist (often used for superscripts) */
.katex .vlist>span {
    margin-top: -0.1em !important;
}

.katex .msupsub .vlist>span[style*="top:-2.55em"] {
    top: -2.3em !important;
}
```

---

This theme is designed to enhance the Marp experience, especially for educational and academic presentations. Let me know if you'd like further refinements!
