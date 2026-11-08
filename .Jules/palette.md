# Palette's Journal

## 2026-03-30 - Live Feedback for Modal Actions
**Learning:** In single-page dynamic interfaces where modal forms or inline card deletions modify content, screen reader users and visual users can feel disoriented when the modal abruptly closes without immediate feedback on whether their action succeeded.
**Action:** Provide an accessible toast notification with `role="status"` and `aria-live="polite"` alongside smooth entry/exit animations (honoring `prefers-reduced-motion`) to announce additions and removals immediately.

## 2026-04-11 - Cryptographic Client-Side Authentication Modals
**Learning:** Adding front-end cryptographic verification (e.g. salted SHA-256 via Web Crypto API) to lock administrative actions requires clear visual trust indicators, accessible live error announcements (`role="alert"`), timing feedback for rate-limiting lockouts, and focus management ensuring screen readers and keyboard users transition seamlessly between authentication and action dialogs.
**Action:** Maintain a standalone focus-trapped authentication modal with live alerts and clear hints, and automatically hand over focus to the target action modal upon verified authentication.
