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

Here are a few more famous equations, similar to the Pythagorean theorem, with brief descriptions:

* **Einstein's Mass-Energy Equivalence:** $E=mc^2$
    * This iconic equation, part of Albert Einstein's theory of special relativity, states that energy (E) and mass (m) are interchangeable and directly proportional to each other, with the constant of proportionality being the speed of light (c) squared. It's fundamental to understanding nuclear energy and the universe.

* **Newton's Second Law of Motion:** $F=ma$
    * Formulated by Isaac Newton, this law describes the relationship between an object's mass (m), its acceleration (a), and the net force (F) acting upon it. It's a cornerstone of classical mechanics, explaining how forces cause objects to move or change their motion.

* **The Golden Ratio (Phi):** $\phi = \frac{1+\sqrt{5}}{2}$
    * Often approximated as 1.618, the golden ratio is an irrational number that has fascinated mathematicians, artists, and architects for centuries. It appears in various natural phenomena and is believed to represent aesthetic harmony and balance in design.

* **Euler's Identity:** $e^{i\pi} + 1 = 0$
    * Considered one of the most beautiful equations in mathematics, Euler's identity elegantly connects five fundamental mathematical constants: $e$ (Euler's number, the base of the natural logarithm), $i$ (the imaginary unit), $\pi$ (pi), 1, and 0. It's a remarkable example of mathematical unity.

* **The Ideal Gas Law:** $PV=nRT$
    * This equation relates the pressure (P), volume (V), temperature (T), and amount (n) of an ideal gas. R is the ideal gas constant. It's a fundamental equation in chemistry and physics for describing the behavior of gases under various conditions.

Do any of these pique your interest for further exploration?

Okay, I understand! You're looking for 10 different equations presented in a similar format to the Pythagorean theorem, using LaTeX for mathematical notation.

Here are 10 different equations from various fields, all formatted using LaTeX:

1.  **Pythagorean Theorem:** $a^2 + b^2 = c^2$
    * Relates the sides of a right-angled triangle.

2.  **Einstein's Mass-Energy Equivalence:** $E = mc^2$
    * Describes the relationship between energy (E), mass (m), and the speed of light (c).

3.  **Newton's Second Law of Motion:** $F = ma$
    * Relates force (F), mass (m), and acceleration (a).

4.  **Ohm's Law:** $V = IR$
    * Describes the relationship between voltage (V), current (I), and resistance (R) in an electrical circuit.

5.  **Quadratic Formula:** $x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$
    * Solves for the roots of a quadratic equation $ax^2 + bx + c = 0$.

6.  **Euler's Identity:** $e^{i\pi} + 1 = 0$
    * A profound relationship connecting five fundamental mathematical constants.

7.  **Ideal Gas Law:** $PV = nRT$
    * Relates pressure (P), volume (V), moles of gas (n), ideal gas constant (R), and temperature (T) for an ideal gas.

8.  **Wavelength-Frequency Relationship:** $c = \lambda f$
    * Relates the speed of light (c), wavelength ($\lambda$), and frequency (f) of an electromagnetic wave.

9.  **Law of Universal Gravitation:** $F = G\frac{m_1 m_2}{r^2}$
    * Describes the gravitational force (F) between two masses ($m_1$, $m_2$) separated by a distance (r), with G as the gravitational constant.

10. **Area of a Circle:** $A = \pi r^2$
    * Calculates the area (A) of a circle given its radius (r).

Got it, my apologies. You want only the LaTeX code for the equations, without the dollar signs or the markdown code block.

Here are 10 equations:

$a^2 + b^2 = c^2$
$E = mc^2$
$F = ma$
$V = IR$
$P = \frac{W}{t}$
$\lambda = \frac{h}{p}$
$K = \frac{1}{2}mv^2$
$U = mgh$
$Q = mc\Delta T$
$s = ut + \frac{1}{2}at^2$


a^2 + b^2 = c^2 \\  
E = mc^2 \\  
F = ma \\  
V = IR \\  
P = \frac{W}{t} \\  
\lambda = \frac{h}{p} \\  
K = \frac{1}{2}mv^2 \\  
U = mgh \\  
Q = mc\Delta T \\  
s = ut + \frac{1}{2}at^2

Let me know your site structure (`Jekyll`, `custom HTML`, `pure Markdown`, etc.), and I can give you a copy-paste-ready solution for your specific case.
