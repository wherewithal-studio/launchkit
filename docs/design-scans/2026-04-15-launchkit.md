# Launchkit — Design Scan 2026-04-15

**Date**: 2026-04-15  
**Venture stage**: Build  
**Inversion layer**: Infrastructure (product launch orchestration — narrative + visual identity)  
**Files scanned**: launchkit-summary.html (first direct file read in scan history)  
**Changes since last scan**: Commit `a6ed71c` standardized breadcrumb nav; stage now Build.

---

## Accessibility

### Font Sizes

**P0 — First direct scan confirms assumed P0:**
- `.topbar-stage`: `0.52rem` (8.3px) — below even the `0.55rem` used in the shared template. Launchkit uses a newer venture page variant that copies the badge class but sets a slightly smaller size. This is the lowest topbar badge size in the portfolio.
- `section-label`: `11px` — at the practical minimum. Acceptable.
- `.road-stage .stage-outcome` equivalent (line 159): `10px` — below floor. This appears to be a small detail caption under roadmap stage cards.
- `.road-stage .stage-name`: `12px` — acceptable.

**Cross-portfolio note**: Launchkit's `0.52rem` topbar badge suggests the newer venture page template variant is drifting to even smaller sizes than the shared template baseline.

### Contrast & Color

- Accent: green `#22c55e` — high contrast on dark. No concerns.
- `var(--text-muted)`: standard floor verification needed.

### Semantic Markup

- Hero-first layout with 52px sticky topbar — compliant with architecture standard.
- No section tabs visible in Launchkit's layout — it uses a single scrolling content page structure. ARIA tab gap from the shared template does not apply here.
- Standard heading hierarchy: h1 → h2 → content. No issues.

---

## UX Patterns

### Cold-Start Narrative

**Adequate.** The tagline "Positioning, messaging, visual identity. Launch with a coherent narrative." is concise and benefit-focused. The kicker gives context about what "coherent narrative" means in practice.

However, Launchkit at Build stage could be clearer about what it *outputs* — the tagline describes the inputs/components but not the deliverable. A user arriving cold wouldn't immediately understand whether Launchkit is a tool, a service, a template system, or something else.

**Recommendation**: Add a clarifying sentence about the output format: e.g., "Launchkit produces a brand narrative package — one brief, zero ambiguity about what you're launching and why."

### Architecture Compliance

Hero-first layout with 52px sticky topbar. Compliant with the venture page standard. No section submenu — appropriate for a product still defining its surface structure.

---

## CLI Compliance

Launchkit is at Build stage; CLI development not yet begun. No audit applicable.

---

## Security

- No hardcoded secrets in scanned HTML.
- Pre-commit hook: unverified. Should be deployed before active development.

---

## Deployment

At Build stage; no active product deployment. Internal summary page served via worker.

---

## Recommendations

### P0 — Accessibility Violations

1. **Topbar badge font size**: `.topbar-stage` at `0.52rem` is below even the floor used in the shared template (`0.55rem`). Raise to `0.7rem` minimum. This is worse than the cross-portfolio P0.
2. **Roadmap stage detail text**: `10px` font on roadmap card detail/outcome text — below practical minimum. Raise to `11px`+.

### P1 — UX & Feedback

3. **Cold-start output clarity**: Add a sentence describing what Launchkit *produces* (the deliverable), not just what it contains. Users need to know if this is a tool, package, service, or template.

### P2 — Debt & Improvements

4. **Pre-commit hook**: Deploy `.githooks/pre-commit` before active development.

---

## Inspiration Applied

- **Cold-start patterns**: Launchkit's tagline is on-brand but output-ambiguous. The Huntr model (clear "what it does, what you get") is the target.
- **Transparency**: Launchkit's whole value is helping ventures communicate clearly — the summary page should exemplify that clarity.

---

## Carried Forward

**From Q1 2026 (2026-03-30)**: No issues found — passing. Font size and pre-commit hook now confirmed as first-scan findings.

**NEW this scan (first direct read)**:
- Topbar badge `0.52rem` P0 — New finding.
- Roadmap detail `10px` P0 — New finding.
- Cold-start output clarity P1 — New finding.
- Pre-commit hook P2 — New finding.
