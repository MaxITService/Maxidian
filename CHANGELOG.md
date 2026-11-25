# Changelog

Each release has a `## v<VERSION>` section. `tools/release.mjs` copies the section of the
current `VERSION` into `RELEASE_NOTES.md` of the release repo and uses it as the GitHub release notes.

## v1.6.6

### Fixed
- A remembered vault that the browser no longer answers for (seen in Edge) no longer leaves an empty window: the start screen says so, and opening it offers **Choose folder…**.
- Choosing a folder is no longer blocked by other remembered vaults that do not answer; **Add / open vault…** and the vault list work again. Such old entries stay in the list, so a vault may be listed twice.

### New
- `maxidian.min.html`: the same app, minified to a smaller file.

## v1.6.5

### New
- **On-page Find & Replace** (`Ctrl+F` / `Ctrl+H`): live match counter, case (`Aa`), whole word (`ab`) and regex (`.*`) toggles, Fuzzy mode, smooth scrolling and an adjustable highlight color. The card floats over the note, so the text never jumps. Regex replace supports `$1`, `$<name>`, lookarounds and anchors.
- **List dragging changes the nesting level**: drag a list item by its bullet or checkbox and move sideways (one level per 32 px) to nest or outdent it. Nested items move along, a drop line shows the new level, and one `Ctrl+Z` undoes it all.
- **Settings > Help**: documents hidden features (`Ctrl+D`, `Ctrl+Alt+G`, `Ctrl+G` / `Ctrl+Shift+G` / `F3`, double `Ctrl`, list dragging, selection wrap, URL paste, split panes, sidebar auto-hide).
- Renaming a note shows the new name at once with a small spinner while links are rewritten, and rolls back cleanly on failure.

### Fixed
- Zero-length regex over emoji no longer hangs; accent folding keeps match offsets correct; whole-word regex finds overlapping matches.
- The active match is revealed in Live Preview inside bullets, checkboxes, rules, tables, callouts and code blocks; folded headings open when they contain the match.
- `Esc` in rename, Suggest, tree filter, split pane and Reading view no longer closes the Find card by accident.
- Rename and move keep correct labels in the split title, filtered tree and across tab switches.
- Removed dead multi-cursor shortcuts (Maxidian is single-cursor); `Ctrl+D` still selects the word under the cursor.

## v1.6.4

- Deleted notes and folders are removed from favorites.
