# 📄 STRICT UI GENERATION SPEC (ASTRO + TAILWIND)

## ⚠️ HARD RULES (DO NOT BREAK)

* DO NOT invent content
* DO NOT modify text from images
* DO NOT summarize or interpret
* DO NOT redesign layout structure
* DO NOT add sections that are not visible
* DO NOT rename content

The model MUST behave like a **visual-to-code converter**, NOT a designer.

---

## 🎯 GOAL

Generate a multi-page Astro project where:

* Each image = one page
* The UI is a **pixel-approximation** of the image
* Only allowed improvement: **animations + responsiveness**

---

## 📁 SOURCE

All pages come from:

public/docs/

Each file represents a page.

---

## 🧠 EXECUTION STRATEGY (VERY IMPORTANT)

The model MUST follow this exact pipeline:

### STEP 1 — ANALYZE IMAGE

* Identify:

  * Sections
  * Text blocks
  * Layout (columns, rows)
  * Typography hierarchy
* Extract ALL visible text EXACTLY

### STEP 2 — STRUCTURE

* Convert into:

  * semantic HTML
  * sections
  * containers
* NO creative changes

### STEP 3 — STYLING

* Use Tailwind CSS
* Match:

  * spacing
  * font sizes
  * alignment
  * colors (approximate if needed)

### STEP 4 — ANIMATION (LIMITED)

Allowed ONLY:

* fade-in
* hover effects
* smooth transitions

NOT allowed:

* parallax
* complex motion
* layout shifts

---

## 🧩 ROUTING RULES

Each page MUST:

* Use filename as route
* Example:

pagina1.jpeg → /pagina1

---

## 🧭 GLOBAL STRUCTURE

### Layout.astro (MANDATORY)

Structure:

* Sidebar (fixed or sticky)
* Main content

Sidebar MUST:

* List ALL pages
* Highlight active page
* Be identical across all pages

---

## 🏠 INDEX PAGE (/)

* Simple navigation hub
* List all pages as cards or links
* NO extra content

---

## 🎨 DESIGN RULES

* Clean UI
* Respect original proportions
* Keep content priority
* Do NOT beautify beyond source

---

## 📱 RESPONSIVE RULES

* Mobile-first
* Stack columns vertically on small screens
* Keep readability

---

## 🚫 FORBIDDEN BEHAVIOR

* Adding lorem ipsum
* Changing titles
* Translating text
* Creating new sections
* Merging sections
* Ignoring spacing

---

## ✅ OUTPUT FORMAT

Project must include:

* /src/layouts/Layout.astro
* /src/pages/index.astro
* /src/pages/[generated pages].astro
* Reusable components ONLY if necessary

---

## 🧪 GENERATION MODE

Act as:

"STRICT UI REPLICATION ENGINE"

NOT:
"Creative designer"

---

## 🔥 PRIORITY ORDER

1. Content accuracy
2. Layout fidelity
3. Responsiveness
4. Animations (last)
