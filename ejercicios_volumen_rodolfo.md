---
title: "Integrales"
subtitle: "Vólumenes"
author: "Prof. Arnoldo Del Toro Peña"
date: \today
subject: "Métodos-Vólumenes"
grade: "Grado: X"
geometry: margin=1in
fontsize: 12pt
lang: es
documentclass: article
header-includes:
  - \usepackage{amsmath}
  - \usepackage{amssymb}
  - \usepackage{mathtools}
  - \everymath{\displaystyle}
  - \everydisplay{\displaystyle}
  - \usepackage{xcolor}
  - \usepackage{tcolorbox}
  - \usepackage{fancyhdr}
  - \pagestyle{fancy}
  - \fancyhead[L]{Integrales - [Vólumenes]}
  - \fancyhead[R]{[X grado]}
  - \fancyfoot[C]{\thepage}
  - \tcbuselibrary{most}
  - \newtcolorbox{objetivo}{colback=green!5!white,colframe=green!75!black,title=OBJETIVO}
  - \newtcolorbox{definicion}{colback=yellow!5!white,colframe=orange!75!black,title=DEFINICIÓN}
  - \newtcolorbox{ejemplo}{colback=blue!5!white,colframe=blue!75!black,title=EJEMPLO}
  - \newtcolorbox{ejercicio}{colback=cyan!5!white,colframe=cyan!75!black,title=EJERCICIO}
  - \newtcolorbox{formula}{colback=gray!5!white,colframe=gray!75!black,title=FÓRMULA}
  - \newtcolorbox{nota}{colback=red!5!white,colframe=red!75!black,title=NOTA IMPORTANTE}
---
 <!-- pandoc file.md -o file.pdf --pdf-engine=xelatex, puedes usar los begin con: objetivo, definicion, ejemplo, ejercicio, formula, nota-->

# Fórmulas Clave
\begin{formula}
\textbf{Método de Discos (revolución alrededor del eje x):}
$\displaystyle V = \pi \int_a^b [f(x)]^2 dx$
\end{formula}
\begin{formula}
\textbf{Método de Arandelas (revolución alrededor del eje x):}
$V = \pi \int_a^b [R(x)]^2 - [r(x)]^2 dx$
\end{formula}
Donde:

$R(x)$ = radio exterior (función superior)
$r(x)$ = radio interior (función inferior)
$[a,b]$ = intervalo de integración

\begin{nota}
Es fundamental identificar correctamente cuál función está "arriba" y cuál está "abajo" en el intervalo de integración.
\end{nota}

# Solución de Volúmenes de Sólidos de Revolución

## Problema 1: $y = x^2$, $y = 4x - x^2$

**Paso 1:** Encontrar los puntos de intersección

$x^2 = 4x - x^2$

$2x^2 = 4x$

$2x^2 - 4x = 0$

$2x(x - 2) = 0$

$x = 0$ o $x = 2$

**Paso 2:** Determinar cuál función está arriba

Para $x = 1$: $y_1 = 1^2 = 1$, $y_2 = 4(1) - 1^2 = 3$

Por lo tanto, $4x - x^2 > x^2$ en el intervalo $[0, 2]$

**Paso 3:** Aplicar la fórmula del volumen (método de discos)

$V = \pi \int_0^2 [(4x - x^2)^2 - (x^2)^2] dx$

$V = \pi \int_0^2 [(4x - x^2)^2 - x^4] dx$

$V = \pi \int_0^2 [16x^2 - 8x^3 + x^4 - x^4] dx$

$V = \pi \int_0^2 [16x^2 - 8x^3] dx$

$V = \pi \left[\frac{16x^3}{3} - \frac{8x^4}{4}\right]_0^2$

$V = \pi \left[\frac{16x^3}{3} - 2x^4\right]_0^2$

$V = \pi \left[\frac{16(8)}{3} - 2(16)\right]$

$V = \pi \left[\frac{128}{3} - 32\right] = \pi \left[\frac{128 - 96}{3}\right] = \frac{32\pi}{3}$

---

## Problema 2: $y = \sqrt{2x - 5}$, $y = 0$, $x = 4$

**Paso 1:** Encontrar el dominio

$2x - 5 \geq 0 \Rightarrow x \geq \frac{5}{2}$

**Paso 2:** Determinar los límites de integración

La región está entre $x = \frac{5}{2}$ y $x = 4$

**Paso 3:** Aplicar la fórmula del volumen

$V = \pi \int_{5/2}^4 (\sqrt{2x - 5})^2 dx$

$V = \pi \int_{5/2}^4 (2x - 5) dx$

$V = \pi \left[x^2 - 5x\right]_{5/2}^4$

$V = \pi \left[(16 - 20) - \left(\frac{25}{4} - \frac{25}{2}\right)\right]$

$V = \pi \left[-4 - \left(\frac{25}{4} - \frac{50}{4}\right)\right]$

$V = \pi \left[-4 - \left(-\frac{25}{4}\right)\right]$

$V = \pi \left[-4 + \frac{25}{4}\right] = \pi \left[\frac{-16 + 25}{4}\right] = \frac{9\pi}{4}$

---

## Problema 3: $y = x^{3/2}$, $y = 8$, $x = 0$

**Paso 1:** Encontrar el punto de intersección

$x^{3/2} = 8$

$x = 8^{2/3} = (2^3)^{2/3} = 2^2 = 4$

**Paso 2:** Determinar los límites de integración

La región está entre $x = 0$ y $x = 4$

**Paso 3:** Aplicar la fórmula del volumen (método de arandelas)

$V = \pi \int_0^4 [8^2 - (x^{3/2})^2] dx$

$V = \pi \int_0^4 [64 - x^3] dx$

$V = \pi \left[64x - \frac{x^4}{4}\right]_0^4$

$V = \pi \left[64(4) - \frac{4^4}{4}\right]$

$V = \pi \left[256 - \frac{256}{4}\right]$

$V = \pi [256 - 64] = 192\pi$

---

## Problema 4: $y = 4x^2$, $x = 0$, $y = 4$

**Paso 1:** Encontrar el punto de intersección

$4x^2 = 4 \Rightarrow x^2 = 1 \Rightarrow x = 1$ (tomamos el valor positivo)

**Paso 2:** Resolver usando el método de discos perpendiculares al eje y

Despejamos $x$ en función de $y$: $x = \frac{\sqrt{y}}{2}$

**Paso 3:** Aplicar la fórmula del volumen

$V = \pi \int_0^4 \left(\frac{\sqrt{y}}{2}\right)^2 dy$

$V = \pi \int_0^4 \frac{y}{4} dy$

$V = \frac{\pi}{4} \int_0^4 y dy$

$V = \frac{\pi}{4} \left[\frac{y^2}{2}\right]_0^4$

$V = \frac{\pi}{4} \cdot \frac{16}{2} = \frac{\pi}{4} \cdot 8 = 2\pi$

---

## Problema 5: $y = \sqrt{x + 2}$, $y = x$, $y = 0$

**Paso 1:** Encontrar los puntos de intersección

Para $y = \sqrt{x + 2}$ y $y = x$:

$x = \sqrt{x + 2}$

$x^2 = x + 2$

$x^2 - x - 2 = 0$

$(x - 2)(x + 1) = 0$

$x = 2$ o $x = -1$

Como $y = x$ y $y \geq 0$, tomamos $x = 2$.

Para $y = \sqrt{x + 2}$ y $y = 0$:

$0 = \sqrt{x + 2} \Rightarrow x = -2$

**Paso 2:** Analizar la región

- Entre $x = -2$ y $x = -1$: solo $y = \sqrt{x + 2}$

- Entre $x = -1$ y $x = 2$: $y = \sqrt{x + 2}$ está arriba de $y = x$

**Paso 3:** Aplicar la fórmula del volumen

$V = \pi \int_{-2}^{-1} (\sqrt{x + 2})^2 dx + \pi \int_{-1}^2 [(\sqrt{x + 2})^2 - x^2] dx$

$V = \pi \int_{-2}^{-1} (x + 2) dx + \pi \int_{-1}^2 [(x + 2) - x^2] dx$

Primera integral:

$\pi \int_{-2}^{-1} (x + 2) dx = \pi \left[\frac{x^2}{2} + 2x\right]_{-2}^{-1}$

$= \pi \left[\left(\frac{1}{2} - 2\right) - \left(\frac{4}{2} - 4\right)\right]$

$= \pi \left[-\frac{3}{2} - (-2)\right] = \pi \left[-\frac{3}{2} + 2\right] = \frac{\pi}{2}$

Segunda integral:

$\pi \int_{-1}^2 (x + 2 - x^2) dx = \pi \left[\frac{x^2}{2} + 2x - \frac{x^3}{3}\right]_{-1}^2$

$= \pi \left[\left(\frac{4}{2} + 4 - \frac{8}{3}\right) - \left(\frac{1}{2} - 2 + \frac{1}{3}\right)\right]$

$= \pi \left[\left(2 + 4 - \frac{8}{3}\right) - \left(\frac{1}{2} - 2 + \frac{1}{3}\right)\right]$

$= \pi \left[6 - \frac{8}{3} - \frac{1}{2} + 2 - \frac{1}{3}\right]$

$= \pi \left[8 - 3 - \frac{1}{2}\right] = \pi \left[5 - \frac{1}{2}\right] = \frac{9\pi}{2}$

**Volumen total:**

$V = \frac{\pi}{2} + \frac{9\pi}{2} = 5\pi$

---

## Resumen de Resultados

1. $V = \frac{32\pi}{3}$
2. $V = \frac{9\pi}{4}$
3. $V = 192\pi$
4. $V = 2\pi$
5. $V = 5\pi$
