---
name: frontend-design
description: Create distinctive, production-grade frontend interfaces with high design quality. Use this skill when the user asks to build web components, pages, or applications. Generates creative, polished code that avoids generic AI aesthetics.
license: Complete terms in LICENSE.txt
---

This skill guides creation of distinctive, production-grade frontend interfaces that avoid generic "AI slop" aesthetics. Implement real working code with exceptional attention to aesthetic details and creative choices that work for everyone.

The user provides frontend requirements: a component, page, application, or interface to build. They may include context about the purpose, audience, or technical constraints.

## Design Thinking

Before coding, understand the context and commit to a BOLD aesthetic direction:

- **Purpose**: What problem does this interface solve? Who uses it? Consider the full spectrum of users including those using assistive technologies.
- **Tone**: Pick an extreme: brutally minimal, maximalist chaos, retro-futuristic, organic/natural, luxury/refined, playful/toy-like, editorial/magazine, brutalist/raw, art deco/geometric, soft/pastel, industrial/utilitarian, etc. There are so many flavors to choose from. Use these for inspiration but design one that is true to the aesthetic direction while maintaining clarity and usability.
- **Constraints**: Technical requirements (framework, performance, WCAG 2.2 AA conformance).
- **Differentiation**: What makes this UNFORGETTABLE? What's the one thing someone will remember? How can distinctive design enhance rather than hinder usability?

**CRITICAL**: Choose a clear conceptual direction and execute it with precision. Bold maximalism and refined minimalism both work - the key is intentionality, not intensity.

Then implement working code (HTML/CSS/JS, React, Vue, etc.) that is:

- Production-grade and functional for all users
- Visually striking and memorable
- Cohesive with a clear aesthetic point-of-view
- Meticulously refined in every detail including keyboard and screen reader experiences

## Frontend Aesthetics Guidelines

Focus on:

- **Typography**: Choose fonts that are beautiful, unique, interesting, AND readable. Avoid generic fonts like Arial and Inter; opt instead for distinctive choices that elevate the frontend's aesthetics while maintaining legibility. Unexpected, characterful display fonts paired with refined, readable body fonts. Ensure sufficient line height (at least 1.5) and paragraph spacing for readability. Test your font choices at various sizes - if a decorative font becomes illegible at smaller sizes, reserve it for large headings only.

- **Color & Theme**: Commit to a cohesive aesthetic that meets contrast requirements. Use CSS variables for consistency. Dominant colors with sharp accents outperform timid, evenly-distributed palettes, but always verify contrast ratios (4.5:1 for normal text, 3:1 for large text and UI components). Never convey information through color alone; pair with icons, patterns, or text labels. When creating dark themes, ensure they maintain proper contrast - pure black on white or vice versa can cause eye strain; consider off-whites and rich darks.

- **Motion**: Use animations for effects and micro-interactions that enhance rather than distract. Prioritize CSS-only solutions for HTML. Use Motion library for React when available. Focus on high-impact moments: one well-orchestrated page load with staggered reveals (animation-delay) creates more delight than scattered micro-interactions. Implement all animations with `prefers-reduced-motion` media queries - either simplify or remove motion for users who need it. Use scroll-triggering and hover states that delight without disorienting. Always provide keyboard-equivalent interactions for hover effects. Avoid parallax scrolling and large-scale viewport movements.

- **Spatial Composition**: Create unexpected layouts through semantic HTML structure. Asymmetry that maintains logical reading order. Overlap that doesn't obscure content or interactive elements. Diagonal flow using CSS transforms that preserve text readability. Grid-breaking elements that maintain predictable navigation patterns. Generous negative space OR controlled density, both can work when interactive elements maintain proper touch targets (minimum 44x44px) and clickable areas. Use CSS Grid and Flexbox to create layouts that reflow gracefully and maintain structure when zoomed to 200%.

- **Backgrounds & Visual Details**: Create atmosphere and depth that enhances rather than interferes with content. Apply creative forms like gradient meshes, noise textures, and geometric patterns, but ensure they never reduce text readability. Use CSS blend modes and opacity to maintain contrast. Layered transparencies should be tested against various content. Dramatic shadows can create depth while improving element distinction. Decorative borders and custom cursors add personality without impeding functionality (ensure custom cursors include a clear hotspot). Grain overlays at subtle opacity levels add texture without reducing clarity.

NEVER use generic AI-generated aesthetics like overused font families (Inter, Roboto, Arial, system fonts), cliched color schemes (particularly purple gradients on white backgrounds), predictable layouts and component patterns, and cookie-cutter design that lacks context-specific character.

Interpret creatively and make unexpected choices that feel genuinely designed for the context. No design should be the same. Vary between light and dark themes, different fonts, different aesthetics. NEVER converge on common choices (Space Grotesk, for example) across generations.

## Code Implementation Principles

**Semantic HTML First**: Build on a foundation of semantic HTML - use proper heading hierarchy (h1-h6), nav, main, article, section, aside elements. This provides structure for both visual design and assistive technologies. The first rule of ARIA is: don't use ARIA if native HTML elements already convey the semantics. Only add ARIA when HTML alone cannot express the interface's meaning (like aria-expanded for accordions or aria-label for icon-only buttons).

**Keyboard Navigation**: Every mouse interaction needs a keyboard equivalent. Ensure logical tab order through proper HTML structure rather than tabindex manipulation. Create visible focus indicators that match your aesthetic, custom focus rings using box-shadow or outline can be both beautiful and functional. Skip links for complex navigation. Keyboard shortcuts for frequently-used actions (with proper documentation).

**Interactive Elements**: Buttons should look and behave like buttons - use `<button>` not divs with onClick. Links should use `<a>` tags. Form inputs need associated labels (visible or aria-label for icon-only inputs). Error messages should be programmatically associated with inputs using aria-describedby. Group related form fields with fieldset and legend.

**Images and Icons**: Decorative images use empty alt="" to be skipped by screen readers. Informative images need descriptive alt text. Icon buttons require accessible names through aria-label or screen-reader-only text. SVG icons can scale perfectly while maintaining sharpness - include role="img" and aria-label for meaningful icons, or aria-hidden="true" for decorative ones.

**State Management**: Communicate state changes to all users. Loading states announced to screen readers (aria-live regions for dynamic updates). Error states with clear messaging and recovery instructions. Success confirmations that don't rely solely on color. Expanded/collapsed states using aria-expanded.

**Responsive and Zoom-Friendly**: Design for 200% browser zoom without horizontal scrolling. Use relative units (rem, em, %) for sizing. Ensure touch targets remain accessible on mobile. Test that decorative elements don't break layout at different zoom levels.

**IMPORTANT**: Match implementation complexity to the aesthetic vision. Maximalist designs need elaborate code with extensive animations and effects that gracefully degrade. Minimalist or refined designs need restraint, precision, and careful attention to spacing, typography, and subtle details. Elegance comes from executing the vision well while ensuring everyone can experience it.

Remember: Claude is capable of extraordinary creative work. Don't hold back, show what can truly be created when thinking outside the box and committing fully to a distinctive vision that includes everyone. Accessibility is not a limitation - it's a design constraint that sparks creativity. The most memorable interfaces are both stunning AND usable by all.
