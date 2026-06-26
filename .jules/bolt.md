## 2024-06-26 - Intl.NumberFormat Instantiation Overhead
**Learning:** Instantiating `Intl.NumberFormat` on every function call (e.g., `new Intl.NumberFormat().format(n)`) is surprisingly slow and creates significant performance overhead, particularly when formatting hundreds or thousands of table cells in rendering loops.
**Action:** Always cache and reuse `Intl.NumberFormat` and `Intl.DateTimeFormat` instances outside of render cycles or formatting utility functions.
