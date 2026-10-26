
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


### Test 5 — Font Fallback

**Condition:** Temporarily replaced the preferred body font (Arial) with "MissingFontTest" in styles.css and refreshed the page in Chrome.

**Expected Result:** The browser should use the next available font in the stack. Text should remain readable without clipping or breaking the layout.

**Observed Result:** The webpage remained readable after the preferred font was made unavailable. Headings, paragraphs, and cards continued displaying correctly. No obvious clipping was observed.

**Evidence:** Missing-Font-Test.png

**Revision:** No revision was required based on the visible fallback test. The original Arial font stack was restored after testing.

**Final Font Stack:** Arial, "Segoe UI", sans-serif.


### Test 6 — HTML and CSS Validation

**Condition:** Uploaded index.html to the Nu HTML Checker
and styles.css to the W3C CSS Validator.

**Expected Result:** HTML and CSS should contain no
validation errors caused by my code.

**Observed Result:** The HTML checker reported zero errors
and zero warnings. The CSS validator reported zero errors
and seven warnings related to CSS custom properties.
The warnings explain that dynamic CSS variables cannot
be fully checked statically.

**Evidence:**
- html-validation-pass.png
- css-validation-pass.png
- css-validation-waenings.png

**Revision:** No code revision was required because
both files passed validation without errors.


### Test 7 — Published Website

**Condition:** Opened the GitHub Pages website in a
Chrome Incognito window while signed out of GitHub.

**Expected Result:** The public website should load
without authentication. All sections, styles, fonts,
media, links, and interactive controls should work.

**Observed Result:** The website opened successfully
without requiring a login. Sections S1–S6 displayed
correctly, styles and fonts loaded, and the enabled
links and controls worked as intended.

**Evidence:** publication-test.png

**Revision:** No revision was necessary.

**Repository:**
https://github.com/blamowatkins/GIT337-Design-System-specimen

**Published Website:**
https://blamowatkins.github.io/GIT337-Design-System-specimen/

### Test 7 — Published Website

**Condition:** Opened the GitHub Pages website in a Chrome
Incognito window while signed out of GitHub.

**Expected Result:** The website should load without
requiring a login. All sections, styles, fonts, links,
and controls should work correctly.

**Observed Result:** The website loaded successfully
without requiring a login. Sections S1–S6 displayed
correctly, and the styles and interactive controls worked.

**Evidence:** publication-test.png

**Revision:** No revision was necessary.

## Code Defense

### 1. Selective CSS Reset

I used a selective CSS reset to make the website display consistently across browsers without removing useful default accessibility features. I removed unnecessary body margins and applied `box-sizing: border-box` to help control element sizing. I kept the natural meaning of headings, lists, buttons, and form controls instead of removing all browser defaults.

### 2. Design Token Hierarchy

I organized my design tokens using CSS custom properties inside `:root`. These include colors, typography, spacing, and component measurements. Using variables helps keep the design consistent because multiple elements can share the same values. If I need to change a color or spacing value, I can update the token instead of changing every individual component.

### 3. Alternate Theme Override

I created an alternate theme using the `.theme-alt` class. This class overrides selected color variables, including primary, accent, background, surface, text, border, and focus colors. The components continue using the same CSS structure while displaying different colors. This demonstrates how one design system can support multiple visual themes without duplicating component styles.


### 4. Evidence-Based Testing and Revision

During keyboard accessibility testing, I reviewed how
the focus outline appeared around interactive elements.

I improved the focus indicator spacing in styles.css
by changing the outline-offset from 3px to 4px.

After making the change, I tested keyboard navigation
using the Tab key and confirmed that the orange focus
outline remained visible without being cut off.

This revision improved the separation between the
focus indicator and the focused element, making
keyboard focus easier to identify.

**Before:** outline-offset: 3px;

**After:** outline-offset: 4px;

**Evidence:** Keyboard focus screenshots and the
GitHub commit "Improve keyboard focus outline spacing."


DID NOT USED AI
