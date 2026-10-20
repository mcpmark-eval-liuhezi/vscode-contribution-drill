# VS Code Contribution Drill — Research Digest

_Prepared for a first-time contributor weekend. All data gathered from live queries against `microsoft/vscode` on the day of the drill._

## 1. Top open issues by comment count

Out of 19,024 open issues, the most-commented are:

| # | Issue | Comments | What it's about |
|---|-------|----------|------------------|
| 1 | [#519](https://github.com/microsoft/vscode/issues/519) | 604 | Workbench UI font size/family customization |
| 2 | [#3130](https://github.com/microsoft/vscode/issues/3130) | 453 | Customizable mouse shortcuts |
| 3 | [#40239](https://github.com/microsoft/vscode/issues/40239) | 437 | Enable/disable extensions from a config file |
| 4 | [#28795](https://github.com/microsoft/vscode/issues/28795) | ~430 | Editor scroll jumps randomly (Linux/Electron upstream) |

### Detail on the top two

**#519 — Allow to change the font size and font of the workbench.** The single most-commented open issue (604 comments, ~4,800 reactions). Only `editor.fontSize` and whole-window zoom exist today; every other piece of UI (Explorer, sidebar, chat) inherits hard-coded sizes. The thread is active right now: AI coding-agent sidebars render in webviews that ignore editor font settings entirely, users are trading custom-CSS hacks to enlarge Explorer text, and community PR #340334 has landed in review covering the sidebar portion only. Mirrored as practice issue #1 in this repo.

**#3130 — Allow customization of mouse shortcuts.** Opened in 2016 by VS Code team member Tyriar. Mouse+modifier gestures such as `alt+click` (add cursor) and `ctrl+click` (follow link) are hard-coded and cannot be rebound like keyboard shortcuts. Ten years on, it is assigned to hediet and parked on the Backlog milestone, still collecting occasional "+1" traffic. Requires a keybinding-layer design rather than a spot fix. Mirrored as practice issue #2 in this repo.

### What this tells a new contributor

The loudest open threads in VS Code are long-lived customization gaps that the team has deliberately deferred — not crashers. A weekend-sized entry point is more likely to be found near active review work (e.g. the `workbench-fonts` label, where PR #340334 is being reviewed) than in the mega-threads themselves. Note also that many high-comment issues (like #28795) are labeled `upstream` and live outside the repo's control entirely.

## 2. Practice issues filed in this repo

- Issue #1 — mirrors microsoft/vscode#519 (workbench fonts)
- Issue #2 — mirrors microsoft/vscode#3130 (mouse shortcuts)
