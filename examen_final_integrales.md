---
title: "Título del Tema"
subtitle: "Subtítulo o Capítulo"
author: "Prof. Arnoldo Del Toro Peña"
date: \today
subject: "Matemáticas"
grade: "Grado: [X° Año]"
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
  - \fancyhead[L]{Matemáticas - [Tema]}
  - \fancyhead[R]{[Grado]}
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

# Solución Examen Final - Integrales

## Problema 1: Volumen de sólido de revolución

**Enunciado:** Calcular el volumen del sólido de revolución que se genera al hacer girar la región acotada por las gráficas: $y=x^2+1$ y la recta $y=-x+3$.

**Solución:**

Primero encontramos los puntos de intersección:

$x^2 + 1 = -x + 3$

$x^2 + x - 2 = 0$

$(x+2)(x-1) = 0$

Por lo tanto: $x = -2$ y $x = 1$

Verificamos cuál función está arriba en el intervalo $[-2, 1]$:

- En $x = 0$: $y_1 = 0^2 + 1 = 1$ y $y_2 = -0 + 3 = 3$

- Por tanto, $y = -x + 3$ está arriba de $y = x^2 + 1$

Usando el método de discos (revolución alrededor del eje x):

$$V = \pi \int_{-2}^{1} [(-x+3)^2 - (x^2+1)^2] dx$$

Expandiendo:

- $(-x+3)^2 = x^2 - 6x + 9$

- $(x^2+1)^2 = x^4 + 2x^2 + 1$

$$V = \pi \int_{-2}^{1} [x^2 - 6x + 9 - x^4 - 2x^2 - 1] dx$$

$$V = \pi \int_{-2}^{1} [-x^4 - x^2 - 6x + 8] dx$$

Integrando:

$$V = \pi \left[-\frac{x^5}{5} - \frac{x^3}{3} - 3x^2 + 8x\right]_{-2}^{1}$$

Evaluando en los límites:

- En $x = 1$: $-\frac{1}{5} - \frac{1}{3} - 3 + 8 = -\frac{1}{5} - \frac{1}{3} + 5 = \frac{-3-5+75}{15} = \frac{67}{15}$

- En $x = -2$: $-\frac{-32}{5} - \frac{-8}{3} - 12 - 16 = \frac{32}{5} + \frac{8}{3} - 28 = \frac{96+40-420}{15} = \frac{-284}{15}$


$$V = \pi \left(\frac{67}{15} - \frac{-284}{15}\right) = \pi \cdot \frac{351}{15} = \frac{117\pi}{5}$$

## Problema 2: Área entre curvas

**Enunciado:** Calcular el área de la región acotada por las gráficas: $y=x^4-4x^2+4$ y $y=x^2+4$

**Solución:**

Encontramos los puntos de intersección:

$x^4 - 4x^2 + 4 = x^2 + 4$

$x^4 - 5x^2 = 0$

$x^2(x^2 - 5) = 0$

Por lo tanto: $x = 0, x = \pm\sqrt{5}$

Verificamos cuál función está arriba:

- En $x = 1$: $y_1 = 1 - 4 + 4 = 1$ y $y_2 = 1 + 4 = 5$

- Por tanto, $y = x^2 + 4$ está arriba de $y = x^4 - 4x^2 + 4$

Por simetría, calculamos el área de $0$ a $\sqrt{5}$ y multiplicamos por 2:

$$A = 2\int_{0}^{\sqrt{5}} [(x^2 + 4) - (x^4 - 4x^2 + 4)] dx$$

$$A = 2\int_{0}^{\sqrt{5}} [5x^2 - x^4] dx$$

$$A = 2\left[\frac{5x^3}{3} - \frac{x^5}{5}\right]_{0}^{\sqrt{5}}$$

$$A = 2\left[\frac{5(\sqrt{5})^3}{3} - \frac{(\sqrt{5})^5}{5}\right]$$

$$A = 2\left[\frac{5 \cdot 5\sqrt{5}}{3} - \frac{25\sqrt{5}}{5}\right]$$

$$A = 2\left[\frac{25\sqrt{5}}{3} - 5\sqrt{5}\right]$$

$$A = 2\sqrt{5}\left[\frac{25}{3} - 5\right] = 2\sqrt{5} \cdot \frac{10}{3} = \frac{20\sqrt{5}}{3}$$

## Problema 3: Longitud de arco

**Enunciado:** Encontrar la longitud de arco de la gráfica: $y = \frac{x^3}{12} + \frac{1}{x}$ en $[1,4]$

**Solución:**

Calculamos la derivada:

$$\frac{dy}{dx} = \frac{x^2}{4} - \frac{1}{x^2}$$

La fórmula de longitud de arco es:

$$L = \int_{1}^{4} \sqrt{1 + \left(\frac{dy}{dx}\right)^2} dx$$

$$\left(\frac{dy}{dx}\right)^2 = \left(\frac{x^2}{4} - \frac{1}{x^2}\right)^2 = \frac{x^4}{16} - \frac{1}{2} + \frac{1}{x^4}$$

$$1 + \left(\frac{dy}{dx}\right)^2 = 1 + \frac{x^4}{16} - \frac{1}{2} + \frac{1}{x^4} = \frac{x^4}{16} + \frac{1}{2} + \frac{1}{x^4}$$

Notamos que esto es un cuadrado perfecto:

$$\frac{x^4}{16} + \frac{1}{2} + \frac{1}{x^4} = \left(\frac{x^2}{4} + \frac{1}{x^2}\right)^2$$

Por lo tanto:

$$L = \int_{1}^{4} \left(\frac{x^2}{4} + \frac{1}{x^2}\right) dx$$

$$L = \left[\frac{x^3}{12} - \frac{1}{x}\right]_{1}^{4}$$

$$L = \left(\frac{64}{12} - \frac{1}{4}\right) - \left(\frac{1}{12} - 1\right)$$

$$L = \frac{16}{3} - \frac{1}{4} - \frac{1}{12} + 1$$

$$L = \frac{64 - 3 - 1 + 12}{12} = \frac{72}{12} = 6$$

## Problema 4: Integral indefinida

**Enunciado:** $\int \frac{x^3}{\sqrt{x^2-49}} dx$

**Solución:**

Usamos la sustitución trigonométrica $x = 7\sec\theta$, entonces $dx = 7\sec\theta\tan\theta d\theta$

$$\sqrt{x^2-49} = \sqrt{49\sec^2\theta - 49} = 7\sqrt{\sec^2\theta - 1} = 7\tan\theta$$

Sustituyendo:
$\int \frac{(7\sec\theta)^3}{7\tan\theta} \cdot 7\sec\theta\tan\theta d\theta$
$= \int \frac{343\sec^3\theta}{7\tan\theta} \cdot 7\sec\theta\tan\theta d\theta$
$= \int \frac{343\sec^3\theta \cdot 7\sec\theta\tan\theta}{7\tan\theta} d\theta$
$= \int 343\sec^4\theta d\theta$

Para $\int \sec^4\theta d\theta$, usamos la identidad $\sec^2\theta = 1 + \tan^2\theta$:
$\int \sec^4\theta d\theta = \int \sec^2\theta \cdot \sec^2\theta d\theta = \int (1 + \tan^2\theta)\sec^2\theta d\theta$

Con la sustitución $u = \tan\theta$, $du = \sec^2\theta d\theta$:
$= \int (1 + u^2) du = u + \frac{u^3}{3} + C = \tan\theta + \frac{\tan^3\theta}{3} + C$

Por lo tanto:
$343\int \sec^4\theta d\theta = 343\left(\tan\theta + \frac{\tan^3\theta}{3}\right) + C$

Regresando a la variable original donde $\tan\theta = \frac{\sqrt{x^2-49}}{7}$:

$\int \frac{x^3}{\sqrt{x^2-49}} dx = 343\left(\frac{\sqrt{x^2-49}}{7} + \frac{1}{3}\left(\frac{\sqrt{x^2-49}}{7}\right)^3\right) + C$

$= 49\sqrt{x^2-49} + \frac{343}{3} \cdot \frac{(\sqrt{x^2-49})^3}{343} + C$

$= 49\sqrt{x^2-49} + \frac{(\sqrt{x^2-49})^3}{3} + C$

$= 49\sqrt{x^2-49} + \frac{(x^2-49)^{3/2}}{3} + C$

$= \frac{\sqrt{x^2-49}}{3}(147 + x^2 - 49) + C$

$= \frac{\sqrt{x^2-49}}{3}(x^2 + 98) + C$

## Problema 5: Integral por fracciones parciales

**Enunciado:** $\int \frac{2x^4-2x^3+6x^2-5x+1}{x^3-x^2+x-1} dx$

**Solución:**

Primero factorizamos el denominador:

$$x^3-x^2+x-1 = x^2(x-1) + 1(x-1) = (x^2+1)(x-1)$$

Como el grado del numerador es mayor que el del denominador, realizamos división larga:

$$\frac{2x^4-2x^3+6x^2-5x+1}{x^3-x^2+x-1} = 2x + \frac{4x^2-3x+1}{(x^2+1)(x-1)}$$

Descomponemos la fracción restante:

$$\frac{4x^2-3x+1}{(x^2+1)(x-1)} = \frac{Ax+B}{x^2+1} + \frac{C}{x-1}$$

Multiplicando por $(x^2+1)(x-1)$:

$$4x^2-3x+1 = (Ax+B)(x-1) + C(x^2+1)$$

Expandiendo y comparando coeficientes:

$$4x^2-3x+1 = Ax^2 - Ax + Bx - B + Cx^2 + C$$

$$4x^2-3x+1 = (A+C)x^2 + (-A+B)x + (-B+C)$$

Sistema de ecuaciones:

- $A + C = 4$

- $-A + B = -3$

- $-B + C = 1$

Resolviendo: $A = 1$, $B = -2$, $C = 3$

Por lo tanto:

$$\int \frac{2x^4-2x^3+6x^2-5x+1}{x^3-x^2+x-1} dx = \int 2x dx + \int \frac{x-2}{x^2+1} dx + \int \frac{3}{x-1} dx$$

$$= x^2 + \frac{1}{2}\ln(x^2+1) - 2\arctan(x) + 3\ln|x-1| + C$$