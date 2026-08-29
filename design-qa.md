# Design QA

final result: passed

## Evidence

- Source visual: `/Users/ccsert/.codex/generated_images/01a04bac-b605-7043-a0d0-007b7cd2bece/exec-5a561903-43ac-4f00-924b-253f09050143.png`
- Source dimensions: 1487 × 1058
- Implementation URL: `https://github.com/ccsert`
- Implementation screenshot: `/Users/ccsert/Documents/ChatGPT/profile/design-references/design-qa-implementation-final.png`
- Implementation dimensions and viewport: 1280 × 720
- Combined comparison: `/Users/ccsert/Documents/ChatGPT/profile/design-references/design-qa-comparison.png`
- State: GitHub dark theme, signed-out public view, desktop viewport, profile overview at the top of the page

## Full-view comparison

The full README flow was inspected in three contiguous viewport captures: header,
all four project rows, and the through-line/toolbox footer. The selected green,
blue, lavender, and orange accents repeat through the entire module, while the
transparent signal-garden artwork stays integrated with the header instead of
forming a separate full-width banner.

## Focused comparison

The source and the live first viewport were normalized to 1280 × 720 and placed
side by side in the combined comparison image. The implementation preserves the
reference hierarchy, two-column header, organic infrastructure illustration,
four-color project system, and compact technology labels. Native GitHub link
colors and table borders are retained instead of relying on unsupported custom
CSS.

## Findings and resolution history

1. P1 — The toolbox initially rendered only the Go icon because commas inside a
   `srcset` URL were parsed as candidate separators. Resolved by percent-encoding
   the icon list and escaping the query separator. Reverified on the live page;
   all nine icons now render.
2. P2 — The generated reference uses custom-colored project links and a drawn
   vertical rail. Native GitHub Markdown cannot reproduce those details without
   fragile generated artwork or unsupported CSS. The implementation carries the
   same mapping through colored number markers and matching technology badges;
   this keeps the page accessible, maintainable, and visually coherent.
3. No P0 or remaining P1 issues found. Header balance, color continuity, image
   transparency, link availability, and dark-theme contrast passed visual QA.
