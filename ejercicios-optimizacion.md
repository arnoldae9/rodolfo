# Problemas de Optimización

---

## Problema 1: Caja sin tapa

**Enunciado:**  
Se desea construir una caja sin tapa a partir de una hoja cuadrada de cartón de 1 metro de lado, recortando cuadrados iguales de las esquinas y doblando los lados hacia arriba.  

**¿Qué tamaño deben tener los cuadrados recortados para que el volumen de la caja sea máximo?**

**Solución:**

Sea $x$ el lado del cuadrado recortado.  
Dimensiones de la base: $(1 - 2x) \times (1 - 2x)$  
Altura de la caja: $x$

Volumen:

$V(x) = (1 - 2x)^2 \cdot x = x(1 - 2x)^2$

Derivamos:

$V'(x) = (1 - 2x)^2 - 4x(1 - 2x)$

Igualamos a cero y resolvemos:
$(1 - 2x)(1 - 6x) = 0 \Rightarrow x = \frac{1}{2}, \frac{1}{6}$

Pero $x = \frac{1}{2}$ haría que la base desaparezca, entonces:

**Respuesta:**  
El volumen es máximo cuando  
$x = \frac{1}{6} \, \text{m}$

---

## Problema 2: Minimizar el costo de un cilindro

**Enunciado:**  
Una lata cilíndrica con volumen de 500 cm³ tiene la tapa y base más costosas (el doble del lateral).  
**¿Qué dimensiones minimizan el costo de fabricación?**

**Solución:**

Volumen:
$V = \pi r^2 h = 500 \Rightarrow h = \frac{500}{\pi r^2}$

Costo:
- Área lateral: $2\pi rh$
- Área tapa y base: $2\pi r^2$
- Costo total:  
$C(r) = 2\pi r h + 2(2\pi r^2) = \frac{1000}{r} + 4\pi r^2$

Derivamos y resolvemos:
$C'(r) = -\frac{1000}{r^2} + 8\pi r = 0
\Rightarrow 8\pi r^3 = 1000 \Rightarrow r = \sqrt[3]{\frac{125}{\pi}} \approx 3.42 \, \text{cm}$

Luego:
$h = \frac{500}{\pi r^2} \approx 13.65 \, \text{cm}$

**Respuesta:**  
Radio $r \approx 3.42 \, \text{cm}$, altura $h \approx 13.65 \, \text{cm}$

---

## Problema 3: Punto más cercano a una parábola

**Enunciado:**  
Encuentra el punto en la parábola $y = x^2$ más cercano al punto $(0, 1)$.

**Solución:**

Distancia al punto $(x, x^2)$ desde $(0, 1)$:
$D^2 = x^2 + (x^2 - 1)^2
\Rightarrow D^2 = x^2 + x^4 - 2x^2 + 1 = x^4 - x^2 + 1$

Derivamos:
$D^2{}'(x) = 4x^3 - 2x = 2x(2x^2 - 1)
\Rightarrow x = 0, \pm \frac{1}{\sqrt{2}}$

Evaluamos:
- $x = 0 \rightarrow D = 1$
- $x = \pm \frac{1}{\sqrt{2}} \rightarrow D > 1$

**Respuesta:**  
El punto más cercano es $(0, 0)$, con una distancia mínima de $1$.

---

## Problema 4: Corral contra un muro

**Enunciado:**  
Con 100 m de cerca se quiere construir un corral rectangular, usando un muro como uno de los lados largos.  
**¿Cuáles son las dimensiones de área máxima?**

**Solución:**

Sean:
- $x$: ancho (los dos lados vallados)
- $y$: largo (frente al muro)

Restricción:
$2x + y = 100 \Rightarrow y = 100 - 2x$

Área:
$A = x \cdot y = x(100 - 2x) = 100x - 2x^2$

Derivamos:
$A'(x) = 100 - 4x = 0 \Rightarrow x = 25
\Rightarrow y = 50$

**Respuesta:**  
Dimensiones de área máxima:  
**Ancho $x = 25 \, \text{m}$, largo $y = 50 \, \text{m}$**

---

## Problema 5: Triángulo con lados fijos

**Enunciado:**  
Dos lados del triángulo miden 8 cm y 5 cm, el ángulo entre ellos puede variar.  
**¿Qué ángulo maximiza el área?**

**Solución:**

Área del triángulo:
$A = \frac{1}{2}ab\sin(\theta) = \frac{1}{2}(8)(5)\sin(\theta) = 20\sin(\theta)$

El máximo valor de $\sin(\theta)$ es 1 cuando $\theta = 90^\circ$

**Respuesta:**  
El área máxima se obtiene cuando  
**$\theta = 90^\circ$**

---
