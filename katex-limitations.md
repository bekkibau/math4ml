---
layout: default
title: KaTeX Limitations
tags: [notetaking]
---

Below is a table listing **KaTeX limitations** and their **workarounds**.

## **Table of KaTeX Limitations & Workarounds**

| **Issue**  | **❌ Does NOT Work**  | **✅ Workaround** |
|------------|----------------------|-------------------|
| **No `\text{}` support** | `` `$ \text{This is a test.} $` `` | Use `\mathrm{}` for short words:  `` `$ \mathrm{This\ is\ a\ test.} $` ``  Or move text outside math mode:  `` `$ x^2 + y^2 = z^2 $` `` |
| **Units inside equations** | `` `$ v = 20 m/s $` `` | Use `\mathrm{}` for units:  `` `$ v = 20 \mathrm{m/s} $` `` |
| **Piecewise function conditions** | `` ` \begin{cases} x^2, & \text{if } x \geq 0 \\ -x^2, & \text{if } x < 0 \end{cases} ` `` | Use `\texttt{}` for conditions:  `` ` \begin{cases} x^2, & \texttt{if } x \geq 0 \\ -x^2, & \texttt{if } x < 0 \end{cases} ` `` |
| **Spacing inside equations** | `` `$ A = B \quad and \quad C = D $` `` | Manually insert spacing:  `` `$ A = B \quad \texttt{and} \quad C = D $` `` |

---

## **Go Back**
[Return to Homepage](index.md)