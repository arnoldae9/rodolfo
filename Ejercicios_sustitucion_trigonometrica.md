# Ejercicios de Sustitución Trigonométrica - Soluciones

## 1. $\int \frac{x}{\sqrt{x^2 + 4}} dx$

**Sustitución:** $x = 2\tan\theta$, entonces $dx = 2\sec^2\theta \, d\theta$

$\sqrt{x^2 + 4} = \sqrt{4\tan^2\theta + 4} = \sqrt{4(\tan^2\theta + 1)} = 2\sec\theta$

**Integral:**
$$\int \frac{x}{\sqrt{x^2 + 4}} dx = \int \frac{2\tan\theta}{2\sec\theta} \cdot 2\sec^2\theta \, d\theta$$

$$= \int 2\tan\theta \sec\theta \, d\theta = 2\int \tan\theta \sec\theta \, d\theta$$

$$= 2\sec\theta + C$$

**Regresando a x:** Como $x = 2\tan\theta$, entonces $\tan\theta = \frac{x}{2}$

En el triángulo rectángulo: $\sec\theta = \frac{\sqrt{x^2 + 4}}{2}$

**Respuesta:** $\int \frac{x}{\sqrt{x^2 + 4}} dx = \sqrt{x^2 + 4} + C$

---

## 2. $\int \frac{x}{\sqrt{x^2 - 1}} dx$

**Sustitución:** $x = \sec\theta$, entonces $dx = \sec\theta \tan\theta \, d\theta$

$\sqrt{x^2 - 1} = \sqrt{\sec^2\theta - 1} = \tan\theta$

**Integral:**
$$\int \frac{x}{\sqrt{x^2 - 1}} dx = \int \frac{\sec\theta}{\tan\theta} \cdot \sec\theta \tan\theta \, d\theta$$

$$= \int \sec^2\theta \, d\theta = \tan\theta + C$$

**Regresando a x:** Como $x = \sec\theta$, entonces $\tan\theta = \sqrt{x^2 - 1}$

**Respuesta:** $\int \frac{x}{\sqrt{x^2 - 1}} dx = \sqrt{x^2 - 1} + C$

---

## 3. $\int \frac{dx}{(1-x^2)^{3/2}}$

**Sustitución:** $x = \sin\theta$, entonces $dx = \cos\theta \, d\theta$

$(1-x^2)^{3/2} = (1-\sin^2\theta)^{3/2} = (\cos^2\theta)^{3/2} = \cos^3\theta$

**Integral:**
$$\int \frac{dx}{(1-x^2)^{3/2}} = \int \frac{\cos\theta}{\cos^3\theta} d\theta = \int \sec^2\theta \, d\theta$$

$$= \tan\theta + C$$

**Regresando a x:** Como $x = \sin\theta$, entonces $\tan\theta = \frac{x}{\sqrt{1-x^2}}$

**Respuesta:** $\int \frac{dx}{(1-x^2)^{3/2}} = \frac{x}{\sqrt{1-x^2}} + C$

---

## 4. $\int \frac{\sqrt{16-x^2}}{x^2} dx$

**Sustitución:** $x = 4\sin\theta$, entonces $dx = 4\cos\theta \, d\theta$

$\sqrt{16-x^2} = \sqrt{16-16\sin^2\theta} = 4\cos\theta$

**Integral:**
$$\int \frac{\sqrt{16-x^2}}{x^2} dx = \int \frac{4\cos\theta}{16\sin^2\theta} \cdot 4\cos\theta \, d\theta$$

$$= \int \frac{16\cos^2\theta}{16\sin^2\theta} d\theta = \int \cot^2\theta \, d\theta$$

$$= \int (\csc^2\theta - 1) d\theta = -\cot\theta - \theta + C$$

**Regresando a x:** Como $x = 4\sin\theta$:
- $\sin\theta = \frac{x}{4}$
- $\theta = \arcsin\left(\frac{x}{4}\right)$
- $\cot\theta = \frac{\sqrt{16-x^2}}{x}$

**Respuesta:** $\int \frac{\sqrt{16-x^2}}{x^2} dx = -\frac{\sqrt{16-x^2}}{x} - \arcsin\left(\frac{x}{4}\right) + C$

---

## 5. $\int \frac{\sqrt{3+x^2}}{x} dx$

**Sustitución:** $x = \sqrt{3}\tan\theta$, entonces $dx = \sqrt{3}\sec^2\theta \, d\theta$

$\sqrt{3+x^2} = \sqrt{3+3\tan^2\theta} = \sqrt{3}\sec\theta$

**Integral:**
$$\int \frac{\sqrt{3+x^2}}{x} dx = \int \frac{\sqrt{3}\sec\theta}{\sqrt{3}\tan\theta} \cdot \sqrt{3}\sec^2\theta \, d\theta$$

$$= \sqrt{3} \int \sec^3\theta \, d\theta$$

La integral de $\sec^3\theta$ es: $\frac{1}{2}(\sec\theta\tan\theta + \ln|\sec\theta + \tan\theta|)$

**Regresando a x:** Como $x = \sqrt{3}\tan\theta$:
- $\tan\theta = \frac{x}{\sqrt{3}}$
- $\sec\theta = \frac{\sqrt{3+x^2}}{\sqrt{3}}$

**Respuesta:** $\int \frac{\sqrt{3+x^2}}{x} dx = \frac{\sqrt{3+x^2}}{2} \cdot \frac{x}{\sqrt{3}} + \frac{\sqrt{3}}{2}\ln\left|\frac{\sqrt{3+x^2} + x}{\sqrt{3}}\right| + C$

---

## 6. $\int \frac{x}{\sqrt{x^2+4x+8}} dx$

**Completando el cuadrado:**
$x^2 + 4x + 8 = (x+2)^2 + 4$

**Sustitución:** $u = x + 2$, entonces $x = u - 2$ y $dx = du$

$$\int \frac{x}{\sqrt{x^2+4x+8}} dx = \int \frac{u-2}{\sqrt{u^2+4}} du$$

$$= \int \frac{u}{\sqrt{u^2+4}} du - 2\int \frac{1}{\sqrt{u^2+4}} du$$

**Primera integral:** $\int \frac{u}{\sqrt{u^2+4}} du = \sqrt{u^2+4} + C_1$

**Segunda integral:** $\int \frac{1}{\sqrt{u^2+4}} du = \ln|u + \sqrt{u^2+4}| + C_2$

**Regresando a x:**
$$\int \frac{x}{\sqrt{x^2+4x+8}} dx = \sqrt{x^2+4x+8} - 2\ln|x+2+\sqrt{x^2+4x+8}| + C$$

---

## 7. Asociación de funciones con sustituciones trigonométricas

### $f(x) = \sqrt{1-e^{2x}}$
- **Forma:** $\sqrt{a^2 - u^2}$ con $a = 1$ y $u = e^x$
- **Sustitución:** $e^x = \sin\theta$ o $u = \sin\theta$
- **Triángulo:** Cateto opuesto = $e^x$, hipotenusa = 1, cateto adyacente = $\sqrt{1-e^{2x}}$

### $g(x) = 1 + x^2$
- **Forma:** $a^2 + u^2$ con $a = 1$ y $u = x$
- **Sustitución:** $x = \tan\theta$
- **Triángulo:** Cateto opuesto = $x$, cateto adyacente = 1, hipotenusa = $\sqrt{1+x^2}$

### $h(x) = \sqrt{(\ln(x))^2 - \sqrt{3}}$
- **Forma:** $\sqrt{u^2 - a^2}$ con $u = \ln(x)$ y $a = \sqrt[4]{3}$
- **Sustitución:** $\ln(x) = \sec\theta$ o $u = \sec\theta$
- **Triángulo:** Hipotenusa = $\ln(x)$, cateto adyacente = $\sqrt[4]{3}$, cateto opuesto = $\sqrt{(\ln(x))^2 - \sqrt{3}}$