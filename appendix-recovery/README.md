<div align="center">

# A · Recovery Guide — I Screwed Up, Now What?

**Appendix** · 🚧 Being written

</div>

> The reference you reach for when something goes wrong at the terminal. Pick your disaster, get the exact fix. Every answer comes back to one question: is it shared yet?

### 📌 What's in here

| # | Topic | In one line |
|:-:|---|---|
| 1 | Bad commit message | `--amend` |
| 2 | Forgot a file | `add` + `--amend --no-edit` |
| 3 | Committed a secret | `rm --cached` + rotate it |
| 4 | Reset too hard | `reflog` recovery |
| 5 | Wrong branch | branch + reset move |
| 6 | Pushed a bad commit | `revert`, never reset |
| 7 | Lost a commit/branch | `reflog` + new branch |

<!-- hero diagram: images/recovery-map.svg — to be drawn (see BUILD-PLAN.md, Part B) -->
<p align="center"><em>🖼️ hero diagram coming: recovery-map.svg</em></p>

---

## 🚧 This page is scaffolded

The structure and plan are set. Content for each topic above will be filled in following the [TEMPLATE](../TEMPLATE.md) — plain-English explanation, real tested commands, a `> [!NOTE]` where it helps, **⚠️ Watch out**, **🔧 Fix it**, **🧪 Try it**, and **🤔 What confused me**.

---

[⬅ 10 · Rewriting History](../10-rewriting-history/README.md) · [🏠 Index](../README.md)
