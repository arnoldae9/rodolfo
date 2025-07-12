# Guía de Sustitución Trigonométrica en Integrales

## 1. Identificar el tipo de expresión en la integral

Dependiendo de la expresión dentro de la raíz, elegimos una sustitución trigonométrica adecuada:

| **Expresión en la integral** | **Sustitución trigonométrica** | **Identidad útil**                  |
| ---------------------------- | ------------------------------ | ----------------------------------- |
| $\sqrt{a^2 - x^2}$           | $x = a \sin \theta$            | $1 - \sin^2 \theta = \cos^2 \theta$ |
| $\sqrt{x^2 + a^2}$           | $x = a \tan \theta$            | $1 + \tan^2 \theta = \sec^2 \theta$ |
| $\sqrt{x^2 - a^2}$           | $x = a \sec \theta$            | $\sec^2 \theta - 1 = \tan^2 \theta$ |

---

## 2. Pasos detallados para aplicar la sustitución

### Ejemplo 1: $\int \frac{dx}{\sqrt{a^2 - x^2}}$

1. **Sustitución**:  
   $x = a \sin \theta$  
   $dx = a \cos \theta \, d\theta$

2. **Reemplazar en la integral**:  
   $\int \frac{a \cos \theta \, d\theta}{\sqrt{a^2 - (a \sin \theta)^2}} = \int \frac{a \cos \theta \, d\theta}{\sqrt{a^2 (1 - \sin^2 \theta)}}$
   
   Simplificamos usando la identidad $1 - \sin^2 \theta = \cos^2 \theta$:  
   $= \int \frac{a \cos \theta \, d\theta}{a \cos \theta} = \int d\theta = \theta + C$

3. **Volver a la variable original**:  
   Como $x = a \sin \theta$, entonces $\theta = \arcsin\left(\frac{x}{a}\right)$.  
   
   **Resultado**:  
   $\arcsin\left(\frac{x}{a}\right) + C$

---

### Ejemplo 2: $\int \frac{dx}{x^2 \sqrt{x^2 + a^2}}$

1. **Sustitución**:  
   $x = a \tan \theta$  
   $dx = a \sec^2 \theta \, d\theta$

2. **Reemplazar en la integral**:  
   $\int \frac{a \sec^2 \theta \, d\theta}{(a \tan \theta)^2 \sqrt{a^2 \tan^2 \theta + a^2}} = \int \frac{a \sec^2 \theta \, d\theta}{a^2 \tan^2 \theta \cdot a \sec \theta}$
   
   Simplificamos usando $\sqrt{\tan^2 \theta + 1} = \sec \theta$:  
   $= \frac{1}{a^2} \int \frac{\sec \theta}{\tan^2 \theta} \, d\theta = \frac{1}{a^2} \int \frac{\cos \theta}{\sin^2 \theta} \, d\theta$

3. **Resolver la nueva integral**:  
   Hacemos otra sustitución: $u = \sin \theta$, $du = \cos \theta \, d\theta$:  
   $= \frac{1}{a^2} \int \frac{du}{u^2} = -\frac{1}{a^2 u} + C = -\frac{1}{a^2 \sin \theta} + C$

4. **Volver a la variable original**:  
   Del triángulo rectángulo asociado a $x = a \tan \theta$:  
   $\sin \theta = \frac{x}{\sqrt{x^2 + a^2}}$
   
   **Resultado**:  
   $-\frac{\sqrt{x^2 + a^2}}{a^2 x} + C$

---

## 3. Consejos

- **Visualiza con triángulos**: Dibuja triángulos rectángulos para relacionar $\theta$ con las variables originales.  
  Ejemplo para $x = a \tan \theta$:  
  $\text{Opuesto} = x, \quad \text{Adyacente} = a, \quad \text{Hipotenusa} = \sqrt{x^2 + a^2}$

- **Practica con variedad de ejercicios**: Empieza con integrales simples y luego avanza a casos más complejos (como los que incluyen $x^2$ en el denominador).

- **Revisa las derivadas de funciones trigonométricas inversas**:  
  Esto ayuda a entender los resultados finales (por ejemplo, $\int \frac{dx}{\sqrt{a^2 - x^2}} = \arcsin\left(\frac{x}{a}\right) + C$).

- **No olvides la constante $a$**: Muchos errores vienen de ignorar $a$ en la sustitución.

---

## Ejemplo adicional rápido

**Integral**: $\int \sqrt{x^2 - 9} \, dx$  

1. Sustitución: $x = 3 \sec \theta$, $dx = 3 \sec \theta \tan \theta \, d\theta$.  

2. La integral se convierte en:  
   $\int 3 \tan \theta \cdot 3 \sec \theta \tan \theta \, d\theta = 9 \int \sec \theta \tan^2 \theta \, d\theta$

3. Usa identidades y integra por partes si es necesario.

---

## Triángulos de referencia para las sustituciones

### Para $x = a \sin \theta$:
- Cateto opuesto: $x$
- Cateto adyacente: $\sqrt{a^2 - x^2}$
- Hipotenusa: $a$

### Para $x = a \tan \theta$:
- Cateto opuesto: $x$
- Cateto adyacente: $a$
- Hipotenusa: $\sqrt{x^2 + a^2}$

### Para $x = a \sec \theta$:
- Cateto opuesto: $\sqrt{x^2 - a^2}$
- Cateto adyacente: $a$
- Hipotenusa: $x$

---