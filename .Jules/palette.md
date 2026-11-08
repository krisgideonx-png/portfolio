# Palette's Journal

## 2026-03-30 - Live Feedback for Modal Actions
**Learning:** In single-page dynamic interfaces where modal forms or inline card deletions modify content, screen reader users and visual users can feel disoriented when the modal abruptly closes without immediate feedback on whether their action succeeded.
**Action:** Provide an accessible toast notification with `role="status"` and `aria-live="polite"` alongside smooth entry/exit animations (honoring `prefers-reduced-motion`) to announce additions and removals immediately.

## 2026-04-05 - Resilient Online Sync with Optimistic UI
**Learning:** Moving from browser-only storage (`localStorage`) to cloud/online synchronization can introduce network latency or potential failure points if the UI blocks waiting for network responses.
**Action:** Use an optimistic UI pattern: immediately render new items and cache locally in `localStorage`, then asynchronously sync to the cloud endpoint with non-blocking error handling and informative toast feedback so the user experience feels instantaneous and robust across devices.
