# How I write each page

A note to myself so every page in these notes reads the same way. It's deliberately light — the structure should stay out of the way of the content.

## The shape of a page

```markdown
# NN · Section Title

> A short, personal intro: where this fits and why I care about it.

**On this page:** [topic](#topic) · [topic](#topic) · [topic](#topic)

---

## A plain descriptive heading
Prose in my own words. When a diagram helps, it goes **right after the paragraph
that introduces the idea** — not parked at the top or dumped at the end.

![alt text that says what the diagram shows](images/thing.svg)

More prose. Every command sits in a code block with its **real output** underneath.

## The next idea
...

---

**What tripped me up:** the one thing that genuinely confused me on this topic,
in my own words — only when there was a real one.

---

[⬅ previous](../NN/README.md) · [🏠 Index](../README.md) · [next ➡](../NN/README.md)
```

## The rules I hold myself to

- **Plain English, short sentences** — the way I'd explain it to a friend.
- **All output is real.** Git runs on my own machine, so every command's output shown is what my terminal actually printed, never illustrative.
- **Depth over brevity.** These are my relearn-from-it notes, so I keep the detail — I'd rather have it and not need it.
- **Write for future me**, not for a stranger taking a course. First person, honest about what confused me.
- **No fixed ritual.** I only add a note, a gotcha, or a "what tripped me up" when the page actually has one — I don't force the same sections onto every page.
- **One idea in bold** per section, commands in `code`.

## The diagrams

A hand-made **SVG** for the bigger pictures, **Mermaid** (which GitHub renders natively) for smaller flows. All of them share one visual language so the repo looks like one set:

- Canvas ~820–900 wide, rounded white frame (`rx=18`, stroke `#DDE3EC`), a centered bold navy title (`#16233B`) with a monospace grey subtitle (`#5A6B85`) beneath.
- Shared palette, used consistently: teal `#19857C` / `#D9EEEB` (primary / safe / committed), terracotta `#DD7A38` / `#F7E6D6` (in-progress / caution / feature), purple `#6B4FD8` / `#E8E2FB` (a distinct actor — remote, HEAD), neutral grey `#9AA3AF` / `#F3F4F6` (inert), navy for text.
- Monospace for anything code-like (hashes, flags, labels); simple grey arrows (`#5A6B85`).
