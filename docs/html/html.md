---
sidebar_position: 2
---

# HTML

## `<!DOCTYPE>` Declaration
The `<!DOCTYPE>` declaration represents the document type, and helps browsers to display web pages correctly.
- `<article>` available on HTML5 but not on HTML4

## HTML `<link>` Element
The `<link>` element defines the relationship between the current document and an external resource.

## `<meta>` Element
The `<meta>` element is typically used to specify the character set, page description, keywords, author of the document, and viewport settings.

- `<meta charset="UTF-8">`
  - UTF-8 covers almost all of the characters and symbols in the world!
- `<meta name="author" content="John Doe">`
- `<meta http-equiv="refresh" content="30">`
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
  - This will set the viewport of your page, which will give the browser instructions on how to control the page's dimensions and scaling.

## Web Content Accessibility Guidelines (WCAG)

### Semantic HTML
Use semantic elements to give meaning to your content.
- ✅ Use `<header>, <nav>, <main>, <footer>, <article>, <section>, and <aside>` correctly.
- ✅ Use `<button>, <ul>, <ol>, <li>, <table>, <form>, <label>, <fieldset>`, etc., instead of `<div> or <span>` for structure or interaction.
- ❌ Avoid using `<div> or <span>` for interactive elements like buttons or links.

### Hierarchy of tags
- ✅ Use heading tags `<h1> to <h6>` in logical order to create a content hierarchy.
- ✅ Only one `<h1>` per page (usually the main title).
- ❌ Don’t skip heading levels (e.g., jumping from `<h1> to <h4>`).

### Text Alternatives
- ✅ Always provide descriptive alt text for images that convey meaning.
- ✅ Use `empty alt=""` for decorative images (so screen readers skip them).
- ✅ Use `<figure> and <figcaption>` for complex images or charts.

### Accessible Rich Internet Applications (ARIA)
- ✅ Use ARIA roles only when native HTML doesn’t provide the same semantics.
- ✅ Common examples:
- `role="alert"` for live alerts.
- `aria-expanded, aria-controls` for collapsible menus.
- `aria-label or aria-labelledby` for custom controls.
- ❌ Don’t use ARIA to fix bad HTML — use semantic elements first.

### Keyboard Accessibility
- ✅ All interactive elements (`links, buttons, inputs, custom components`) must be reachable and operable via `Tab, Enter, and Space` keys.
- ✅ Use `tabindex="0"` to make custom elements focusable.
- ❌ Avoid tabindex values greater than 0 — it breaks natural tab order.
- ✅ Provide clear focus styles (`:focus-visible`) for all focusable elements.

### Forms Accessibility
- ✅ Always pair `<label>` with form controls (for attribute).
- ✅ Use aria-describedby for helper or error text.
- ✅ Use `<fieldset> and <legend>` for grouped inputs (like radio buttons).
- ✅ Provide clear error messages and instructions.
- ✅ Include `required, min, max`, and pattern attributes for validation.

### Color Contrast
- 4.5:1 contrast ratio for normal text.
- 3:1 for large text (≥18pt or 14pt bold).
- ✅ Don’t rely solely on color to convey meaning (e.g., use icons or text too).
- ✅ Check color contrast with tools like WebAIM Contrast Checker.

### Focus Management
- ✅ Ensure keyboard focus is visible and logical.
- ✅ Move focus appropriately for dynamic content (e.g., after modal opens).
- ✅ Use aria-live for dynamically updating sections (like notifications).
- ❌ Avoid removing outline styles — customize them instead.

### Links and Buttons
- ✅ Use `<a>` for navigation and `<button>` for actions.
- ✅ Link text must be meaningful (avoid “Click here” or “Read more”).
- ✅ Provide aria-label if link text isn’t descriptive enough (e.g., icon-only links).

### Page Landmarks
- ✅ Use `<main>, <nav>, <header>, <footer>, <aside>, <section>` to create landmarks.
- ✅ Screen reader users can jump between landmarks easily.

### Responsive & Zoom Accessibility
- ✅ Ensure layout and text scale properly up to 200% zoom.
- ✅ Avoid fixed heights or widths that cut off content.
- ✅ Test with browser zoom and mobile devices.

### Dynamic Content & Modals
- ✅ When a modal opens, trap focus inside and return focus to the trigger when closed.
- ✅ Hide background content from screen readers (`aria-hidden="true"`) when modal is open.
- ✅ Use aria-modal="true" and appropriate roles.

### Motion & Animation
- ✅ Avoid animations that flash more than 3 times per second.
- ✅ Respect prefers-reduced-motion media query.
- ✅ Provide users with a way to disable auto-playing media.

### Tables
- ✅ Use `<th>` for headers and `<td>`for data.
- ✅ Add `scope="col"` or `scope="row"` for clarity.
- ✅ Use `<caption>` to describe the table’s purpose.

### Skip Links
- ✅ Provide a “Skip to main content” link at the top of the page for keyboard users.