# CLAUDE.md

## Output Rules

Never produce partial outputs. A partial output is a broken output.

Banned patterns in code: `// ...`, `// rest of code`, `// implement here`, `// TODO`, `/* ... */`, `// similar to above`, bare `...` standing in for omitted code.

Banned patterns in prose: "Let me know if you want me to continue", "for brevity", "the rest follows the same pattern", "and so on" when replacing actual content.

If approaching the token limit, write at full quality to a clean breakpoint (end of a function, file, or section), then output:
```
[PAUSED — X of Y complete. Send "continue" to resume from: section name]
```
Resume exactly where you stopped. No recap.

## Non-Negotiables (All Projects)

- Never use Inter, Roboto, Arial, Open Sans, or Helvetica.
- Never use generic thick-stroke Lucide, FontAwesome, or Material Icons. Prefer Phosphor Icons.
- Never animate `top`, `left`, `width`, or `height`. Use `transform` and `opacity` only.
- Never use `height: 100vh` for full-screen sections. Use `min-height: 100dvh`.
- Never use `window.addEventListener('scroll')` for scroll effects. Use `IntersectionObserver`.
- Never use placeholder copy: "Lorem Ipsum", "John Doe", "Acme Corp". Write realistic content.
- Never use AI copy clichés: "Elevate", "Seamless", "Unleash", "Next-Gen", "Game-changer", "Delve".
- Verify every import exists in `package.json` before writing it.
- Use semantic HTML throughout: `<nav>`, `<main>`, `<article>`, `<aside>`, `<section>`.

## Code Quality

- All styling in the project's styling system. No mixed inline styles.
- Relative units for layout (`rem`, `%`, `max-width`). No hardcoded pixel widths on containers.
- Meaningful `alt` text on all content images.
- Clean z-index scale. Never `z-index: 9999`.
- No commented-out dead code in deliverables.
- If the project uses Tailwind, confirm v3 vs v4 before modifying config.

## Frontend & UI Work

Before writing any UI code, read `ui-design.md` in full. It defines the design system, component patterns, motion rules, and the pre-output checklist. Do not guess at design decisions covered there.
