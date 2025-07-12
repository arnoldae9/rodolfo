# Guía de Integración por Fracciones Parciales

## 1. Identificar el tipo de fracción y factorización

Para aplicar fracciones parciales, primero debemos factorizar completamente el denominador y clasificar los factores:

| **Tipo de factor**            | **Forma general**   | **Descomposición en fracciones parciales**                                         |
| ----------------------------- | ------------------- | ---------------------------------------------------------------------------------- |
| Factor lineal simple          | $(x - a)$           | $\frac{A}{x - a}$                                                                  |
| Factor lineal repetido        | $(x - a)^n$         | $\frac{A_1}{x - a} + \frac{A_2}{(x - a)^2} + \cdots + \frac{A_n}{(x - a)^n}$       |
| Factor cuadrático irreducible | $(ax^2 + bx + c)$   | $\frac{Ax + B}{ax^2 + bx + c}$                                                     |
| Factor cuadrático repetido    | $(ax^2 + bx + c)^n$ | $\frac{A_1x + B_1}{ax^2 + bx + c} + \frac{A_2x + B_2}{(ax^2 + bx + c)^2} + \cdots$ |

---

## 2. Método general para aplicar fracciones parciales

### Paso 1: Verificar que el grado del numerador sea menor que el del denominador
Si $\text{grado}(P(x)) \geq \text{grado}(Q(x))$, realizar división polinomial primero.

### Paso 2: Factorizar completamente el denominador
Buscar factores lineales y cuadráticos irreducibles.

### Paso 3: Escribir la descomposición en fracciones parciales
Según la tabla anterior.

### Paso 4: Encontrar las constantes desconocidas
Usar el método de coeficientes indeterminados o valores específicos de $x$.

### Paso 5: Integrar cada fracción parcial
Aplicar las técnicas básicas de integración.

---

## 3. Ejemplos detallados

### Ejemplo 1: Factor lineal simple
**Integral**: $\int \frac{5x + 1}{x^2 + x - 2} dx$

1. **Factorizar el denominador**:  
   $x^2 + x - 2 = (x + 2)(x - 1)$

2. **Descomposición en fracciones parciales**:  
   $\frac{5x + 1}{(x + 2)(x - 1)} = \frac{A}{x + 2} + \frac{B}{x - 1}$

3. **Encontrar las constantes**:  
   $5x + 1 = A(x - 1) + B(x + 2)$
   
   Para $x = 1$: $5(1) + 1 = B(1 + 2) \Rightarrow 6 = 3B \Rightarrow B = 2$
   
   Para $x = -2$: $5(-2) + 1 = A(-2 - 1) \Rightarrow -9 = -3A \Rightarrow A = 3$

4. **Integrar**:  
   $\int \frac{5x + 1}{x^2 + x - 2} dx = \int \frac{3}{x + 2} dx + \int \frac{2}{x - 1} dx$
   
   **Resultado**: $3 \ln|x + 2| + 2 \ln|x - 1| + C$

---

### Ejemplo 2: Factor lineal repetido
**Integral**: $\int \frac{2x + 1}{x^2(x - 1)} dx$

1. **Identificar la factorización**:  
   El denominador ya está factorizado: $x^2(x - 1)$

2. **Descomposición en fracciones parciales**:  
   $\frac{2x + 1}{x^2(x - 1)} = \frac{A}{x} + \frac{B}{x^2} + \frac{C}{x - 1}$

3. **Encontrar las constantes**:  
   $2x + 1 = Ax(x - 1) + B(x - 1) + Cx^2$
   
   Para $x = 0$: $1 = B(-1) \Rightarrow B = -1$
   
   Para $x = 1$: $2(1) + 1 = C(1)^2 \Rightarrow C = 3$
   
   Para $x = 2$: $2(2) + 1 = A(2)(1) + (-1)(1) + 3(4)$
   $5 = 2A - 1 + 12 \Rightarrow A = -3$

4. **Integrar**:  
   $\int \frac{2x + 1}{x^2(x - 1)} dx = \int \frac{-3}{x} dx + \int \frac{-1}{x^2} dx + \int \frac{3}{x - 1} dx$
   
   **Resultado**: $-3 \ln|x| + \frac{1}{x} + 3 \ln|x - 1| + C$

---

### Ejemplo 3: Factor cuadrático irreducible
**Integral**: $\int \frac{x + 1}{(x - 1)(x^2 + 1)} dx$

1. **Identificar la factorización**:  
   $x^2 + 1$ es irreducible (no tiene raíces reales)

2. **Descomposición en fracciones parciales**:  
   $\frac{x + 1}{(x - 1)(x^2 + 1)} = \frac{A}{x - 1} + \frac{Bx + C}{x^2 + 1}$

3. **Encontrar las constantes**:  
   $x + 1 = A(x^2 + 1) + (Bx + C)(x - 1)$
   
   Para $x = 1$: $1 + 1 = A(1 + 1) \Rightarrow A = 1$
   
   Expandiendo: $x + 1 = x^2 + 1 + Bx^2 - Bx + Cx - C$
   $x + 1 = (1 + B)x^2 + (-B + C)x + (1 - C)$
   
   Comparando coeficientes:
   - $x^2$: $0 = 1 + B \Rightarrow B = -1$
   - $x^1$: $1 = -B + C = 1 + C \Rightarrow C = 0$
   - $x^0$: $1 = 1 - C$ ✓

4. **Integrar**:  
   $\int \frac{x + 1}{(x - 1)(x^2 + 1)} dx = \int \frac{1}{x - 1} dx + \int \frac{-x}{x^2 + 1} dx$
   
   $= \ln|x - 1| - \frac{1}{2} \ln(x^2 + 1) + C$

---

## 4. Técnicas especiales de integración

### Para términos de la forma $\frac{A}{x - a}$:
$\int \frac{A}{x - a} dx = A \ln|x - a| + C$

### Para términos de la forma $\frac{A}{(x - a)^n}$ con $n > 1$:
$\int \frac{A}{(x - a)^n} dx = \frac{A}{1-n} \cdot \frac{1}{(x - a)^{n-1}} + C$

### Para términos de la forma $\frac{Ax + B}{x^2 + px + q}$:
1. Separar en dos partes: $\frac{Ax + B}{x^2 + px + q} = \frac{A}{2} \cdot \frac{2x + p}{x^2 + px + q} + \frac{B - \frac{Ap}{2}}{x^2 + px + q}$

2. La primera parte se integra como $\frac{A}{2} \ln|x^2 + px + q|$

3. La segunda parte requiere completar el cuadrado y usar $\arctan$

---

## 5. Consejos prácticos

- **Siempre verifica tu factorización**: Un error aquí afecta todo el problema.

- **Usa el método de valores específicos**: Es más rápido para encontrar constantes cuando hay factores lineales simples.

- **Verifica tu respuesta**: Deriva el resultado para confirmar que obtienes el integrando original.

- **Práctica con factores cuadráticos**: Son los más difíciles, pero siguen patrones predecibles.

- **Memoriza las integrales básicas**: $\int \frac{dx}{x^2 + a^2} = \frac{1}{a} \arctan\left(\frac{x}{a}\right) + C$

---

## 6. Casos especiales comunes

### Cuando el grado del numerador es mayor o igual al del denominador:
Realizar división polinomial primero.

**Ejemplo**: $\int \frac{x^3 + 1}{x^2 - 1} dx$

Dividir: $\frac{x^3 + 1}{x^2 - 1} = x + \frac{x + 1}{x^2 - 1}$

Luego aplicar fracciones parciales a $\frac{x + 1}{x^2 - 1}$.

### Cuando aparecen factores cuadráticos repetidos:
$\frac{f(x)}{(x^2 + ax + b)^2}$ requiere términos adicionales en la descomposición.

---