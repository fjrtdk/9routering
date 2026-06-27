## 2026-06-27 - ReactFlow Node Re-renders

**Learning:** Frequent intervals (`setInterval`) generating new state that forces `ReactFlow` to re-calculate layout elements causes all custom nodes to re-render, even if their data contents haven't changed.
**Action:** Always wrap custom ReactFlow nodes in `memo()` when the application logic requires rapid layout invalidation to prevent excessive cascading re-renders.
