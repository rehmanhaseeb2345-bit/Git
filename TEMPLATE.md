# My page template

I copy this structure for every new topic, so every page in these notes reads the same way. It's the same template I use across my other notes repos, with two tweaks for a command-heavy tool like Git (marked 🆕).

## The structure

````markdown
<div align="center">

# NN · Section Title

**Part X — Name** · ✅ Done

</div>

> A short, personal intro: where this fits and why it matters.

### 📌 What's in here
<!-- a small table linking to each topic on the page -->

<p align="center"><img src="images/hero.svg" alt="..." width="820"></p>

## 1. What it is
Plain-English definition. One or two sentences.

## 2. Why it exists
The problem it solves.

## 3. Key points
The core ideas, broken into small labelled chunks, with tables where they help.
Every command shown in a `code block` **with its real output**.

## Visual
A hand-made SVG in images/ for the hero; Mermaid (flowchart / gitGraph) for supporting diagrams.

## ⚠️ Watch out
Bullets of mistakes and misconceptions.

## 🔧 Fix it   🆕
One line: "if you hit this, run that." The recovery reflex for this topic.

## 🧪 Try it
A small exercise, with the answer in a <details> block.

## 🤔 What confused me
The thing that tripped me up, in a quote block, so future-me remembers.

**One-line recap:** the whole page in a sentence.

<!-- nav footer: previous · index · next -->
````

## My rules for writing

- Plain English and short sentences, the way I'd explain it to a friend.
- One consistent structure on every page.
- **🆕 All output is real.** Git runs on my own machine, so every command's output
  shown is what my terminal actually printed — never illustrative. (That's the
  whole point of a Git notes repo: I can test everything.)
- **🆕 Every page carries a `🔧 Fix it`** line — the recovery move for that topic —
  so the "get out of trouble" theme runs through the whole repo, not just the
  recovery appendix.
- Diagrams render on GitHub: a hand-made **SVG** for the hero, **Mermaid**
  (`flowchart`, `gitGraph`) for supporting visuals.
- Commands in `code`, the one idea to remember in **bold**.
- Every page ends with **What confused me** — the honest part.

## The diagram style (so every SVG matches)

- Canvas `width="820"`, rounded white frame (`rx=16`, stroke `#d0d7de`), title
  (21px bold `#1f2328`) + plain subtitle (14px `#57606a`) at top-left.
- Semantic colors, used consistently: blue `#1971c2`/`#e7f0fb` (primary/you/main),
  purple `#8b5cf6`/`#f3e8ff` (distinct actor/remote), orange `#c2410c`/`#fff7ed`
  (feature/caution), green `#1a7f52`/`#edfbf3` (destination/success/merge), amber
  `#f59e0b` (callout).
- `#1971c2` arrows (shared marker); dashed grey for return/parent paths; a
  `#f6f8fa` **summary bar** along the bottom with an UPPERCASE label and colored
  `<tspan>`s tying back to the boxes.
