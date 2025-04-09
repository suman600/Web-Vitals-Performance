### 🔹 What is CLS?

- **CLS** = Cumulative Layout Shift
- Measures **unexpected movement** of elements on the screen.
- Indicates **visual stability** during load and interaction.
- Calculated based on **impact × distance** of layout shifts.

---

### 🔹 Why It Matters

- Shifting elements cause users to misclick or lose context.
- Affects **user trust**, especially on mobile or slow networks.

---

### 🔹 CLS Score Guide

| UX Quality | CLS Score |
|------------|-----------|
| ✅ Good     | ≤ 0.1     |
| ⚠️ Okay     | 0.1–0.25  |
| ❌ Poor     | > 0.25    |

---

### 🔹 Common Causes

- No `width/height` on images or iframes
- Ads/embeds loading late without space reserved
- Fonts loading late and shifting text
- DOM injected above existing content
- CSS animations affecting layout (e.g. `top`, `margin`)

---

### 🔹 Fixes (with Best Practices)

| Problem               | Fix / Technique                                   |
|------------------------|--------------------------------------------------|
| Image or video shift   | Add `width` and `height` or use `aspect-ratio`   |
| Ad causes shift        | Reserve space using `min-height` or container    |
| Font swap shifts text  | Preload fonts + use `font-display: swap`         |
| Late DOM injection     | Avoid inserting content above-the-fold          |
| Layout animation shift | Use `transform`, not `margin` or `top`           |

---

### 🔹 Tools to Measure CLS

- **PageSpeed Insights**
- **Chrome DevTools → Performance tab**
- **Web Vitals Extension**
- **Google Search Console (CWV report)**

---

Let me know if you want similar notes for INP or want to build a clean README section from this!