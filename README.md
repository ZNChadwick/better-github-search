# Better GitHub Search

A zero-dependency, single-file browser utility for GitHub repository discovery—combining a visual multi-select boolean query rail, live topic/language autocomplete, DNF multi-branch API expansion, and a side-by-side README comparison workspace.

**[Launch Live Demo](https://znchadwick.github.io/better-github-search/)** · **[Download `index.html`](https://raw.githubusercontent.com/znchadwick/better-github-search/main/index.html)**


> **Scope Note:** Designed specifically for **repository discovery** (topics, descriptions, metadata, and READMEs). For fast regex or line-by-line source code search across public repositories, you may want to use **[grep.app](https://grep.app/)** or **[GitHub Code Search](https://github.com/search)**.

<img width="1608" height="1014" alt="Screenshot 2026-11-16 050900" src="https://github.com/user-attachments/assets/d1a84d0a-94d4-48f0-a9be-2e4db2c4ccde" />

## Why This Exists
GitHub's native web search falls short when researching ecosystems across multiple overlapping topics:
- Complex nested `(A OR B) AND (C OR D)` expressions are error-prone and tedious to rearrange in a single-line text box.
- It can be difficult to keep track of which repositories you have already reviewed or which ones received new commits since your last search.
- Comparing READMEs across 10+ candidate projects requires juggling dozens of browser tabs.

## Key Features
- **Visual Multi-Select Boolean Query Rail**
  - Color-paired nested `( )` brackets with distinct semantic text colors for `topic:`, `language:`, `stars:` / date ranges, `fork:` / `in:` flags, and keywords.
  - **Drag-marquee box**, `Ctrl+Click`, and `Shift+Click` multi-selection to drag groups of pills together or wrap them in `( )` with one click.
  - **Syntax-aware `Auto-Order`** that organizes operands inside every bracket level without breaking boolean logic, plus multi-step `Ctrl+Z` / `Ctrl+Y` Undo/Redo.
- **Live Topic & Qualifier Autocomplete**
  - Queries GitHub's `/search/topics` endpoint as you type `topic:...` (with session caching, 350 ms debounce, and a toggle to conserve rate limits), alongside instant local suggestions for languages and date filters.
- **DNF Multi-Branch Query Expansion**
  - Expands nested `OR` expressions into separate GitHub Search API branches, merges and deduplicates results, sorts by star velocity or recent updates, and previews exact branch counts against GitHub's rate limit before fetching.
- **Frosted Tab Groups & Commonality Workspace**
  - Organize candidate repositories into color-coded shelves, inspect full rendered READMEs side by side, highlight query matches, and auto-detect shared topics, languages, and keywords across a group to stage new search refinements.
- **Bookmarks, Saved Searches & Tag Shortcuts**
  - Save repositories into organized **Bookmark Groups** (or save entire Tab Group shelves directly as bookmarks) with dedicated JSON bookmark export/import.
  - Store complex multi-branch queries as **Saved Searches** and pin frequently used qualifiers as one-click **Saved Tag & Filter Shortcuts** above the results feed.
- **Triage & Privacy-First Local Storage**
  - Automatically flags repositories as `Seen`, `Hidden`, or `Updated` when new commits land after your last visit. All data and your optional GitHub Personal Access Token stay strictly in browser `localStorage` with full JSON backup/restore.

<img width="1854" height="998" alt="Screenshot 2026-11-16 051219" src="https://github.com/user-attachments/assets/4f36cf8f-b8cc-461a-a758-077d5dcedf9d" />

## Quick Start
1. **Use Online:** Open the **[GitHub Pages Live Demo](https://znchadwick.github.io/better-github-search/)**.
2. **Run Locally:** Download `index.html` and double-click it in any modern browser.
3. *(Optional)* Paste a read-only GitHub Personal Access Token to raise GitHub's Search API rate limit from **10** to **30 requests/minute**.

## Architecture & Development Note
Designed to be a zero-build, single-file HTML/CSS/JS application so anyone can run it offline or host it statically with zero dependencies. Designed, architected, and iteratively directed using AI-assisted code generation.

## License
[MIT](LICENSE) 
