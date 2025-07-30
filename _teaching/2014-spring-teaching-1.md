---
title: "Teaching experience 1"
collection: teaching
type: "Undergraduate course"
permalink: /teaching/2014-spring-teaching-1
venue: "University 1, Department"
date: 2014-01-01
location: "City, Country"
---

Great observation, Raye — this is a **common gotcha** when working with LaTeX math in Markdown across different GitHub environments.

---

## ✅ TL;DR: Why it works in GitHub *preview* but not on GitHub Pages (`github.io`)

GitHub supports `$$...$$` and `\(...\)` inline in its **repository Markdown preview** (like in `README.md`) using built-in rendering.

But **GitHub Pages (`username.github.io`) does *not* support LaTeX math out of the box**. You need to **enable MathJax manually** in your Jekyll-based site.

---

## ✅ How to Fix It on `github.io` (Enable MathJax)

To render LaTeX properly on GitHub Pages, follow these steps:

---

### 🔧 1. Add MathJax to your `_config.yml` (if using Jekyll)

```yaml
markdown: kramdown
kramdown:
  math_engine: mathjax
  input: GFM
```

---

### 🔧 2. Insert MathJax script into your HTML layout

In your main layout (e.g., `_layouts/default.html`), add this in `<head>` or before the closing `</body>` tag:

```html
<script type="text/javascript" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>
```

If you're using **a static `README.md`** for a GitHub Pages home page (without Jekyll), insert this manually at the bottom of your Markdown:

```html
<script type="text/javascript" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>
```

---

### ✅ 3. Then, use `$$ ... $$` for block equations:


$$
|\psi\rangle = \alpha |0\rangle + \beta |1\rangle
$$


Or inline math with `\( ... \)`:


This is a quantum state: \( |\psi\rangle = \alpha |0\rangle + \beta |1\rangle \)


---

### Example Live Usage (Markdown with MathJax):


## Quantum State

$$
|\psi\rangle = \alpha |0\rangle + \beta |1\rangle
$$

$
|\psi\rangle = \alpha |0\rangle + \beta |1\rangle
$

> In this expression, $(\alpha)$ and \(\beta\) are complex amplitudes such that $(|\alpha|^2 + |\beta|^2 = 1)$.


---

Let me know your site structure (`Jekyll`, `custom HTML`, `pure Markdown`, etc.), and I can give you a copy-paste-ready solution for your specific case.
