---
sidebar_position: 3
---

# CSS

#### CSS Box Model
- Every element has: content + padding + border + margin.
- box-sizing: border-box includes padding and border in total width/height.

#### CSS Units
- Absolute: px.
- Relative: em (to parent), rem (to root), %, vh, vw, ch.

#### CSS Variables
- Custom properties: `--main-color: #333; color: var(--main-color);`.

#### Animations
- Define with `@keyframes;` control using `animation-name, duration, iteration-count`, etc.

#### Transformations
- Modify elements (translate, rotate, scale, skew) in 2D or 3D.

#### Media Queries
- `@media (max-width: 768px) { ... }` — apply rules conditionally.

#### Fluid Typography
- Use clamp() or relative units (em, rem, vw) for scalable text.

#### CSS Functions
- min(), max(), clamp() for dynamic sizing.

#### Pseudo-classes
- Target states `(:hover, :focus, :nth-child, :not())`.

#### Pseudo-elements
- Create virtual elements `(::before, ::after)`.

#### Web Fonts
- Load with `@font-face;` always include fallback fonts.

#### Critical CSS
- Inline above-the-fold styles for faster render.

#### Minification
- Remove unnecessary spaces/comments to reduce file size.

#### CSS Architecture
- Use naming conventions (BEM, OOCSS, SMACSS) for maintainable code.

#### CSS Isolation
- Use modules or scoped styles to prevent leaks across components.

#### SASS / SCSS
- Variables, nesting, mixins, partials, and inheritance for modular CSS.

#### Styled-components / Emotion
- CSS-in-JS libraries allowing dynamic, component-scoped styling.
