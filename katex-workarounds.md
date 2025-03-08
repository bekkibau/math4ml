---
layout: default
title: KaTeX Workarounds
---

# KaTeX Workarounds for Limitations

<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.0/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.0/dist/contrib/auto-render.min.js"
        onload="renderMathInElement(document.body);"></script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.0/dist/katex.min.css">

## 1️⃣ No  Support in KaTeX

**Problem:** In MathJax, you can use  inside math mode to write normal text. KaTeX does **not** support this.

### ❌ Does NOT work in KaTeX:
`$\text{This is a test.}$`

### ✅ Workaround 1: Use  for short words
`$\mathrm{This\ is\ a\ test.}$`

### ✅ Workaround 2: Keep Text Outside Math Mode
`$x^2 + y^2 = z^2$\ where this is known as the **Pythagorean theorem**.

---

## 2️⃣ Handling Units in KaTeX

**Problem:** If you need units inside equations, KaTeX doesn’t handle spacing well.

### ❌ Does NOT work well:
`$ v = 20 m/s $`

### ✅ Workaround: Use  for Units:
`$ v = 20 \mathrm{m/s} $`

---

## 3️⃣ Writing Conditions in Piecewise Functions

**Problem:** In MathJax,  makes piecewise function conditions look correct. In KaTeX, we must avoid it.

### ❌ Does NOT work in KaTeX:
`$
f(x) =
\begin{cases}
x^2, & \text{if } x \geq 0 \
-x^2, & \text{if } x < 0
\end{cases}
$`

### ✅ Workaround: Use  or Keep Text Outside Math
`$
f(x) =
\begin{cases}
x^2, & \texttt{if } x \geq 0 \
-x^2, & \texttt{if } x < 0
\end{cases}
$`

---

## 4️⃣ Ensuring Spacing Inside Equations

**Problem:** KaTeX **ignores spaces** in math mode unless explicitly added.

### ❌ Does NOT render spaces:
`$ A = B \quad and \quad C = D $`

### ✅ Workaround: Manually Insert Spacing
`$ A = B \quad \texttt{and} \quad C = D $`

---

## 5️⃣ Go Back

[Return to Homepage](index.md)
