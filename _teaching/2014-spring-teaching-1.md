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

> In this expression, $(\alpha)$ and \(\beta\) are complex amplitudes such that \(|/alpha|^2 + |/beta|^2 = 1\)

## MathJax 

Support for MathJax (version 3.* via [jsDelivr](https://www.jsdelivr.com/), [documentation](https://docs.mathjax.org/en/latest/)) is included in the template:

$$
\displaylines{
\nabla \cdot E= \frac{\rho}{\epsilon_0} \\\
\nabla \cdot B=0 \\\
\nabla \times E= -\partial_tB \\\
\nabla \times B  = \mu_0 \left(J + \varepsilon_0 \partial_t E \right)
}
$$

The default delimiters of `$$...$$` and `\\[...\\]` are supported for displayed mathematics, while `\\(...\\)` should be used for in-line mathematics (ex., \\(a^2 + b^2 = c^2\\))

**Note** that since Academic Pages uses Markdown which cases some interference with MathJax and LaTeX for escaping characters and new lines, although [some workarounds exist](https://math.codidact.com/posts/278763/278772#answer-278772). In some cases, such as when you are including MathJax in a `citation` field for publications, it may be necessary to use `\(...\)` for inline delineation.
---

Let me know your site structure (`Jekyll`, `custom HTML`, `pure Markdown`, etc.), and I can give you a copy-paste-ready solution for your specific case.
