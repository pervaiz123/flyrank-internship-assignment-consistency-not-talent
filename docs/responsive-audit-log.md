\# Mobile \& Responsiveness Audit Log (Week 07)



\## 1. Executive Summary

\- \*\*Tested Devices:\*\* Real physical smartphone (iOS / Android), viewport sizes 360px, 375px, 414px, and desktop (1080p).

\- \*\*Core Goal:\*\* Eliminate layout breaks, ensure WCAG AAA accessibility contrast compliance, expand tap targets, and optimize typography.



\---



\## 2. Identified \& Resolved Issues



| Section | Before Audit (Broken / Suboptimal) | After Audit (Fixed \& Verified) |

| :--- | :--- | :--- |

| \*\*Grid Layout\*\* | `minmax(360px, 1fr)` forced horizontal scrolling on mobile screens smaller than 380px wide (e.g. 360px Android devices). | Set `minmax(280px, 1fr)`, allowing cards to stack cleanly on narrow mobile viewports. |

| \*\*Tap Target Size\*\* | Buttons had variable height (`\~36px`), making them easy to mis-click on touch devices. | Set `min-height: 48px` across all CTA links and submit buttons to comply with touch accessibility guidelines. |

| \*\*iOS Input Zoom\*\* | Input fields used `font-size: 0.9rem`, causing Mobile Safari to force an unwanted page zoom on click. | Enforced `font-size: 1rem` on `input` and `textarea` elements, preventing browser auto-zoom. |

| \*\*Typography Scaling\*\* | Headings (`h1`, `h2`) used fixed `rem` sizes, causing long headings to wrap onto 3-4 lines on 360px screens. | Implemented fluid typography (`clamp(1.8rem, 5vw, 2.5rem)`), ensuring proportion across screen sizes. |

| \*\*Color Contrast\*\* | Secondary body text used `#9ca3af` (\~4.8:1 contrast ratio against dark background). | Updated secondary text to `#cbd5e1` (\~9.2:1 contrast ratio), passing WCAG AAA contrast standard. |

| \*\*Accessibility (ARIA)\*\*| Anchor links lacked explicit navigation descriptors for screen readers. | Added explicit `aria-label` attributes to all CTA buttons and external portfolio links. |



\---



\## 3. Link Verification Checklist

\- \[x] \*\*Resume / CV (`./resume.pdf`):\*\* Opens properly in new tab on mobile browser.

\- \[x] \*\*GitHub Link (`github.com/pervaiz123`):\*\* Verified active and responsive.

\- \[x] \*\*LinkedIn Link (`linkedin.com/in/pervaiz-ahmed-`):\*\* Verified active.

\- \[x] \*\*Contact Form:\*\* Tested input interaction and submission on touch interface without page overflow.

