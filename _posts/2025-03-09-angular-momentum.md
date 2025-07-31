---
title: 'Angular Momentum'
date: 2025-03-09
permalink: /posts/2025/09/angular-momentum/
tags:
  - quantum
  - math
  - physics
---

This is one of the key postulates of **Bohr’s atomic model**, stating that the **angular momentum** $L$ of an electron in a stable orbit is **quantized**, i.e., it can only take specific discrete values depending on an integer $n$.

$$
L = n \cdot \frac{h}{2\pi}
$$

---

### 🧠 Goal of the Explanation:

We’ll explain:

1. **What this equation represents** (in terms of physics)
2. **Why it’s important** (Bohr’s postulate)
3. **How it came to be** (historical + mathematical reasoning)
4. **What math/physics concepts it uses**

---

## 🧪 1. What does the equation mean?

* $L$ is the **angular momentum** of an electron orbiting the nucleus.
* $h$ is **Planck’s constant**:

  $$
  h \approx 6.626 \times 10^{-34} \, \text{Js}
  $$
* $2\pi$ appears because we’re dealing with **circular motion**.
* $\frac{h}{2\pi}$ is often written as $\hbar$ (pronounced "h-bar"):

  $$
  \hbar = \frac{h}{2\pi}
  $$
* $n \in \mathbb{Z^+}$ is the **principal quantum number**: 1, 2, 3, …

Thus, Bohr said:

> “The angular momentum of an electron in orbit is quantized and must be an integer multiple of $\hbar$.”

---

## 🔁 2. Why quantize angular momentum?

Bohr’s atomic model was built to explain **why electrons don’t spiral into the nucleus** and why **hydrogen has a discrete line spectrum**.

In classical physics:

* An electron in orbit should emit radiation continuously.
* It should lose energy and spiral inward — but atoms are stable!
* So Bohr postulated: **Electrons can only exist in orbits where their angular momentum is quantized**.

That’s where the equation:

$$
L = n \cdot \frac{h}{2\pi}
$$

comes in — it’s a **quantization condition**.

---

## ⚙️ 3. How did Bohr come up with it?

Bohr didn’t derive it purely mathematically — it was a **bold postulate** inspired by the new ideas of **quantum theory**, particularly **Planck's** and **Einstein’s** work on **quantized energy**.

But later it was justified using **de Broglie’s hypothesis** and **wave mechanics**.

---

## 🔁 4. Deeper Mathematical Justification (via de Broglie)

After Bohr, in 1924, **Louis de Broglie** suggested that **electrons have wave properties**, and their **orbits must fit whole wavelengths**:

$$
\text{Circumference of orbit} = n \lambda
\Rightarrow 2\pi r = n \lambda
$$

Since de Broglie said:

$$
\lambda = \frac{h}{p} = \frac{h}{mv}
$$

Substitute:

$$
2\pi r = n \cdot \frac{h}{mv}
\Rightarrow mvr = \frac{nh}{2\pi}
\Rightarrow L = mvr = n \cdot \frac{h}{2\pi}
$$

🧠 **So from de Broglie’s wave-particle duality**, we get Bohr’s angular momentum quantization as a **natural result of standing waves**!

---

## 📐 5. What is Angular Momentum? (Quick Refresher)

In circular motion:

$$
L = m v r
$$

Where:

* $m$ = mass of electron
* $v$ = orbital speed
* $r$ = radius of orbit

Bohr said this quantity $L$ can **only** be $n \cdot \hbar$, not just anything.

---

## 🔢 Summary:

| Concept           | Meaning                                                                                         |
| ----------------- | ----------------------------------------------------------------------------------------------- |
| **Equation**      | $L = n \cdot \frac{h}{2\pi}$                                                                    |
| **Describes**     | Quantized angular momentum of electrons in Bohr orbits                                          |
| **Postulated by** | Niels Bohr (1913)                                                                               |
| **Supported by**  | de Broglie’s wave hypothesis (1924)                                                             |
| **Key idea**      | Electron orbit must accommodate a whole number of de Broglie wavelengths — standing waves only! |

---

## step-by-step derivations 

1. **Radius of Bohr orbit $r_n$**
2. **Energy of electron in $n^\text{th}$ orbit $E_n$**
3. **(Bonus)**: Visual of the **standing wave condition** (why angular momentum is quantized)

---

## 🔷 1. Derivation of Radius $r_n$

We’ll derive the **Bohr radius** formula starting from physics principles:

### 🔹 Step 1: Use centripetal force = electrostatic force

An electron moves in a circular orbit, so:

$$
\text{Centripetal force} = \text{Coulomb (electrostatic) force}
$$

$$
\frac{mv^2}{r} = \frac{k e^2}{r^2}
$$

Where:

* $m$ = electron mass
* $v$ = velocity
* $r$ = orbit radius
* $e$ = electron charge
* $k = \frac{1}{4\pi\varepsilon_0}$ (Coulomb constant)

---

### 🔹 Step 2: Use Bohr’s angular momentum quantization

$$
L = mvr = n \cdot \frac{h}{2\pi}
\Rightarrow v = \frac{n h}{2\pi m r}
$$

---

### 🔹 Step 3: Substitute velocity $v$ into force equation

$$
\frac{m}{r} \left(\frac{n h}{2\pi m r}\right)^2 = \frac{k e^2}{r^2}
$$

Simplify:

$$
\frac{n^2 h^2}{4\pi^2 m r^3} = \frac{k e^2}{r^2}
$$

Multiply both sides by $r^3$:

$$
\frac{n^2 h^2}{4\pi^2 m} = k e^2 r
$$

Solve for $r$:

$$
r = \frac{n^2 h^2}{4\pi^2 m k e^2}
$$

This is the **Bohr radius formula**. For hydrogen ($Z = 1$):

$$
r_n = n^2 \cdot a_0
$$

Where $a_0 = \frac{h^2}{4\pi^2 m k e^2} \approx 0.529 \times 10^{-10} \, \text{m}$

---

## 🔷 2. Derivation of Energy $E_n$

Total energy of the electron is:

$$
E = \text{Kinetic Energy} + \text{Potential Energy}
$$

### 🔹 Step 1: Kinetic energy

From above:

$$
\frac{mv^2}{r} = \frac{ke^2}{r^2} \Rightarrow mv^2 = \frac{ke^2}{r}
$$

So:

$$
K.E. = \frac{1}{2} mv^2 = \frac{1}{2} \cdot \frac{ke^2}{r}
$$

---

### 🔹 Step 2: Potential energy

Potential energy in a Coulomb field:

$$
U = - \frac{ke^2}{r}
$$

---

### 🔹 Step 3: Total energy

$$
E = K.E. + U = \frac{1}{2} \cdot \frac{ke^2}{r} - \frac{ke^2}{r} = -\frac{ke^2}{2r}
$$

Now substitute $r$ from radius formula:

$$
r = \frac{n^2 h^2}{4\pi^2 m k e^2}
\Rightarrow \frac{1}{r} = \frac{4\pi^2 m k e^2}{n^2 h^2}
$$

So:

$$
E_n = -\frac{1}{2} ke^2 \cdot \frac{4\pi^2 m k e^2}{n^2 h^2}
= -\frac{2\pi^2 m k^2 e^4}{n^2 h^2}
$$

This gives the **energy levels** of the hydrogen atom:

$$
E_n = -\frac{13.6\, \text{eV}}{n^2}
$$

---

## 🌀 3. Diagram: Standing Wave Condition

Let’s describe how **standing wave = quantized orbits**:

### ⚛ De Broglie Hypothesis:

Electron has **wavelength**:

$$
\lambda = \frac{h}{mv}
$$

For a **stable orbit**, the circumference must fit a whole number of wavelengths:

$$
2\pi r = n \lambda
$$

Otherwise, the wave interferes destructively and **cancels itself**.

This directly leads to:

$$
mvr = n \cdot \frac{h}{2\pi}
\Rightarrow L = n\hbar
$$

✅ This matches Bohr’s postulate!

---

### 📊 Visualization (text-based)

| Orbit Number | Wave Fit Around Orbit                     |
| ------------ | ----------------------------------------- |
| $n = 1$      | One full wave around the circle — 🔁🌊    |
| $n = 2$      | Two full waves around the circle — 🔁🌊🌊 |
| $n = 3$      | Three full waves — 🔁🌊🌊🌊               |

In each case, the wave **constructively interferes**, making a **stable standing wave**.

---

## ✅ Summary

| Concept                    | Formula                                          |
| -------------------------- | ------------------------------------------------ |
| Radius of orbit            | $r_n = \frac{n^2 h^2}{4\pi^2 m k e^2} = n^2 a_0$ |
| Bohr radius                | $a_0 = 0.529 \times 10^{-10} \, \text{m}$        |
| Angular momentum quantized | $L = n \cdot \frac{h}{2\pi}$                     |
| Energy of orbit            | $E_n = -\frac{13.6}{n^2} \, \text{eV}$           |

---
