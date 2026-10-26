
# GIT 337 — Design System Specimen
## Test Record

### Test 1 — Responsive Design

**Condition:** Tested the website at 320px, 768px, and 1280px viewport widths using Chrome DevTools.

**Expected Result:** The website should adjust to each screen width, keep text readable, and avoid horizontal page overflow.

**Observed Result:** At 320px, content stacks vertically. At 768px and 1280px, the layout expands and the service cards appear side by side. Text and controls remain readable.

**Evidence:** 320px.png, 768px.png, 1280px.png

**Revision:** No revision was required based on the responsive screenshots reviewed.

### Test 2 — Browser Zoom

**Condition:** Tested the website at 200% browser zoom in Chrome.

**Expected Result:** Text, headings, links, buttons, and form controls should remain readable and usable without horizontal page overflow.

**Observed Result:** In the S4 section, the text and buttons remained readable, and the visible buttons were not cut off. The remaining sections and page-level overflow still need to be confirmed.

**Evidence:** `evidence 1/200%-zoom.png`

**Revision:** No revision identified in the S4 section tested.

### Test 3 — Keyboard Navigation

**Condition:** Tested all interactive elements using the
keyboard only in Chrome.

**Expected Result:** Links, buttons, and form controls should
be keyboard accessible, with visible focus indicators.
Disabled controls should not be activated.

**Observed Result:** Keyboard focus moved through the links,
buttons, and form controls. Focus indicators remained visible,
and the disabled button could not be activated.

**Evidence:** Focus-visible.png, S4-primary-focus.png,
S4-secondary-focus.png, S6-text-focus.png

**Revision:** No revision was necessary.

### Test 4 — Color Contrast

**Condition:** Tested the default and alternate theme
colors using the WebAIM Contrast Checker.

**Expected Result:** Essential text should meet WCAG AA
contrast requirements. Focus indicators and controls
should remain distinguishable.

**Observed Result:**
- White on dark blue: 13.09:1 — Pass
- Purple on lavender: 10.23:1 — Pass
- Orange focus color on lavender: 5.86:1 — Pass

All three tested color combinations passed their
applicable contrast thresholds.

**Evidence:** WebAIM contrast checker screenshots
for the default theme, alternate theme, and focus color.

**Revision:** No revision was required for these
three tested combinations.

