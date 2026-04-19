# Launchkit — Design Scan 2026-04-16

**Date**: 2026-04-16  
**Venture stage**: Build  
**Inversion layer**: Infrastructure (product launch orchestration — narrative + visual identity)  
**Files scanned**: launchkit-summary.html  
**Changes since last scan**: `0a38536` — cross-portfolio font size fix (class-based elements). Pre-commit hook status: unresolved.

---

## Accessibility

### Font Sizes

**Partially resolved (commit `0a38536`):**

Class-based font sizes are confirmed fixed:
- `.topbar-stage` (if class-based): raised to `0.7rem` ✓
- Roadmap stage detail text (class-based `10px` → `11px`): raised ✓

**P0 — NEW — PARTIAL FIX MISS:**

The `0a38536` commit fixed class-based font sizes but **missed inline-styled topbar action buttons**. launchkit-summary.html line 278 contains:

```
<a href="https://internal.wherewithal.studio/design-scans?project=launchkit" ... font-size:0.65rem ...>Design Scan</a>
```

This "Design Scan" link button in the topbar uses `font-size:0.65rem` as an inline style — below the 0.7rem floor. This is the only remaining inline font-size violation in Launchkit.

**Fix**: Change `font-size:0.65rem` → `font-size:0.7rem` in the inline style on line 278 of launchkit-summary.html.

### Contrast & Color

- Green `#22c55e` accent: high contrast. No concerns.

### Semantic Markup

Launchkit uses hero-first single-scroll layout. No section tab pattern. No ARIA tab issues.

---

## UX Patterns

### Cold-Start Narrative

**P1 — CARRIED FROM 2026-04-15 — NOT RESOLVED:**

The tagline "Positioning, messaging, visual identity. Launch with a coherent narrative." describes inputs but not the deliverable. A user arriving cold doesn't know if Launchkit is a tool, service, or template system.

**Specific addition needed**: "Launchkit produces a brand narrative package — one brief, one visual system, zero ambiguity." (or similar). The Wherewithal thesis of "own the intelligence layer" applies here — the summary page should demonstrate Launchkit's output clarity, not describe its process.

### Architecture Compliance

Hero-first layout with 52px sticky topbar: compliant.

---

## CLI Compliance

At Build stage. No CLI applicable.

---

## Security

**P2 — CARRIED FROM 2026-04-15 — NOT RESOLVED:**

Pre-commit hook: **still not deployed** in `launchkit/.git/hooks/`. All other projects now have hooks deployed; Launchkit is the only outlier. Deploy before active development.

---

## Deployment

At Build stage; no active product deployment.

---

## Recommendations

### P0 — Accessibility Violations

1. **Inline topbar button font size** (NEW — missed by `0a38536`): `font-size:0.65rem` on "Design Scan" link in launchkit-summary.html line 278. Change to `0.7rem`. One-line fix.

### P1 — UX & Feedback

2. **Cold-start output clarity** (CARRIED FROM 2026-04-15): Add one sentence describing Launchkit's deliverable — not its process. The tagline describes what goes in; describe what comes out.

### P2 — Debt & Improvements

3. **Pre-commit hook** (CARRIED FROM 2026-04-15 — only remaining project without hook): Deploy `.githooks/pre-commit` to launchkit before active development. All other projects now covered; Launchkit is the sole outlier.

---

## Resolved This Cycle

- **Class-based font sizes** (P0 from 2026-04-15): Partially resolved by `0a38536`. Class-based sizes fixed; inline button remains.

---

## Carried Forward

**CARRIED FROM 2026-04-15:**
- Cold-start output clarity P1 — Unresolved.
- Pre-commit hook P2 — Unresolved. Launchkit is now the only project without this.

**NEW this scan:**
- Inline topbar button `0.65rem` P0 — New finding (missed by `0a38536`).
