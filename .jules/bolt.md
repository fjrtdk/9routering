## 2025-05-18 - Memoizing Recharts in dashboard
**Learning:** Usage charts rendered by Recharts are expensive and can re-render frequently if their parent receives live updates (e.g. SSE stream).
**Action:** Wrap these components with React.memo() when their props are simple primitives (like 'period') to prevent unnecessary redraws during live updates.
