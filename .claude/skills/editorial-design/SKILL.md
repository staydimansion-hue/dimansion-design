---
name: editorial-design
description: Apply solid editorial/graphic design fundamentals (hierarchy, whitespace, alignment, grid, Korean typography specifics) when creating or reviewing print or brand design materials — house rules, posters, cards, brochures, welcome cards. Load before laying out any print-style or brand document.
---

# Editorial / Graphic Design Fundamentals

General-purpose design judgment distilled from standard graphic design theory, plus concrete numeric patterns proven in this project's own work (see `../../CLAUDE.md` at the repo root for STAY DIMANSION's specific brand values — this file is the reusable, brand-agnostic version).

## The six core principles

Every layout decision should trace back to one of these. If you can't name which principle a design choice serves, it's probably arbitrary.

- **Contrast** — size, weight, or color differences that make important things pop and prevent monotony. Weak contrast = everything looks equally (un)important.
- **Repetition** — reuse the same type sizes, colors, spacing values, and treatments across a piece. This is what makes a document feel designed rather than assembled ad hoc.
- **Alignment** — every element sits on a shared edge or axis. Nothing "just floats" at an arbitrary position. Misalignment is the fastest way to look amateur.
- **Proximity** — things that belong together sit close; things that don't belong together get more space. Proximity IS grouping — viewers read spatial closeness as relatedness before they read any label.
- **Hierarchy** — a clear order of "read this first, then this, then this," built from size/weight/color/position/whitespace working together, not any single one alone.
- **Balance** — visual weight is distributed so the page doesn't feel lopsided. Doesn't require symmetry — asymmetric balance is often more interesting.

## Whitespace is not empty space

Whitespace (margins, gaps, breathing room around a headline) is a positive design element, not leftover space to be filled. It:
- lets the eye rest between reading tasks
- frames content the way a picture frame does
- is one of the strongest signals of "professional" vs. "amateur" — cramped layouts read as cheap or rushed regardless of the actual content quality

**Default toward more whitespace, not less.** When a layout feels tight, the fix is almost never "shrink the whitespace to fit more in" — it's "cut content" or "make the frame bigger." Whitespace is usually the first thing to sacrifice under pressure and the first thing viewers notice being sacrificed.

## Hierarchy without abusing emphasis

Hierarchy needs exactly ONE dominant element per view (the title/headline). Everything else should read as "body" at a consistent, calm baseline. A common failure mode: reaching for bold, color, or a highlight box to make an important-feeling body item stand out — the moment more than one thing is "emphasized," none of them are, and the page reads as noisy.

**Rule of thumb: emphasis (bold, accent color, highlight background) belongs to the title/headline tier ONLY.** If a body item feels like it deserves more visual weight than its siblings, that's a sign it should either become its own section with its own title, or it doesn't actually need special treatment — trust the reader to notice content that matters when everything around it is calm and consistent.

Concretely, watch for these creeping-emphasis patterns in body content and remove them:
- Bolding a data value next to its label (a password, a room number, a price) while sibling values in the same list stay regular weight
- Coloring one phrase inside a sentence with the brand accent color
- Putting a background/highlight box behind just one item in an otherwise plain list

## Grid systems

The more content there is, the more a grid matters. A grid breaks information into "bite-sized" units aligned to a shared column/row structure, making dense content scannable instead of overwhelming. Sparse, headline-driven pieces (posters, single-message cards) often don't need a visible grid at all — one strong axis of alignment is enough.

## A numeric spacing scale (starting point, not gospel)

Pick ONE of these per piece based on content density — never mix scales within one document.

**Dense / information-heavy** (rules, brochures, spec sheets, multi-item lists) — 8px grid:
| value | use |
|---|---|
| 8px | caption/translation line under its parent line |
| 12px | icon+text pairs, tight inline groups |
| 16px | item-to-item within a section |
| 24px | block-to-block within a section |
| 32px+ | headline to body (never less) |
| 48px | section-to-section |

**Sparse / brand-forward** (posters, cards, single-message pieces) — 1.6× scale:
| value | use |
|---|---|
| 10px | inline group |
| 16px | item-to-item |
| 26px | subhead to content |
| 42px+ | headline to body (never less) |
| 68px | major section break / poster top margin |

If a document feels cramped, the headline-to-body gap is almost always the first place that's too tight — check it first.

## Korean-specific typography rules

These matter for any Korean-language print/brand material, not just this brand:

- **`word-break: keep-all;` on any element containing Korean body text.** Without it, browsers can break a line in the middle of an 어절 (word + attached particle/ending), producing garbage like "루프탑에서 드시" / "고, 쓰레기는" split across two lines — the particle gets orphaned from its word. `keep-all` only allows breaks at whitespace between 어절, matching how a human would actually break the line. Pair it with `overflow-wrap: break-word;` as a safety net for genuinely unbreakable strings (long URLs, etc.).
- **No italics for Korean OR Latin text in the same piece.** Most Korean typefaces have no real italic glyphs; browsers fake it with a synthetic oblique (just slanting the upright glyph), which visibly mangles Hangul strokes. Banning italics for Latin text too keeps the two scripts visually consistent within one document — use size + muted color for de-emphasis instead (see below).
- **Slightly negative letter-spacing (~`-0.02em`) tightens most Korean webfonts** (Noto Sans KR and similar default to fairly open tracking). Apply it at the shared Korean-text class level so per-element overrides (like tracked-out small-caps labels) still win.
- **De-emphasis (translations, fine print, captions) = smaller size + muted color, never italic, never a lighter weight that hurts legibility.**

## Process checklist before calling a layout done

1. Does exactly one element read as "the headline"? Everything else calm?
2. Is every emphasis (bold/color/highlight) on that headline tier only — none leaked into body items?
3. Is the headline-to-body gap at or above the scale's minimum?
4. Does spacing come from one scale, applied consistently, not ad hoc numbers?
5. For Korean text: `word-break: keep-all` present, no italics anywhere, tracking checked?
6. If it's a fixed-size print piece, has it actually been rendered and measured (not just eyeballed in markup) to confirm nothing overflows the frame?
