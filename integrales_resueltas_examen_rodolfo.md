# Resolución de Integrales

## 1. $\int x^3 \sin(x) dx$

**Método:** Integración por partes (aplicada dos veces)

Sea $u = x^3$, $dv = \sin(x)dx$
Entonces $du = 3x^2dx$, $v = -\cos(x)$

$\int x^3 \sin(x) dx = -x^3\cos(x) + 3\int x^2\cos(x)dx$

Para $\int x^2\cos(x)dx$, usamos integración por partes nuevamente:
Sea $u = x^2$, $dv = \cos(x)dx$
Entonces $du = 2xdx$, $v = \sin(x)$

$\int x^2\cos(x)dx = x^2\sin(x) - 2\int x\sin(x)dx$

Para $\int x\sin(x)dx$:
Sea $u = x$, $dv = \sin(x)dx$
Entonces $du = dx$, $v = -\cos(x)$

$\int x\sin(x)dx = -x\cos(x) + \int \cos(x)dx = -x\cos(x) + \sin(x)$

Sustituyendo hacia atrás:
$\int x^2\cos(x)dx = x^2\sin(x) - 2(-x\cos(x) + \sin(x)) = x^2\sin(x) + 2x\cos(x) - 2\sin(x)$

**Resultado final:**
$$\int x^3 \sin(x) dx = -x^3\cos(x) + 3x^2\sin(x) + 6x\cos(x) - 6\sin(x) + C$$

## 2. $\int e^x \cos(3x) dx$

**Método:** Integración por partes (aplicada dos veces)

Sea $u = e^x$, $dv = \cos(3x)dx$
Entonces $du = e^x dx$, $v = \frac{1}{3}\sin(3x)$

$\int e^x \cos(3x) dx = \frac{1}{3}e^x\sin(3x) - \frac{1}{3}\int e^x\sin(3x)dx$

Para $\int e^x\sin(3x)dx$:
Sea $u = e^x$, $dv = \sin(3x)dx$
Entonces $du = e^x dx$, $v = -\frac{1}{3}\cos(3x)$

$\int e^x\sin(3x)dx = -\frac{1}{3}e^x\cos(3x) + \frac{1}{3}\int e^x\cos(3x)dx$

Sustituyendo:
$\int e^x \cos(3x) dx = \frac{1}{3}e^x\sin(3x) - \frac{1}{3}(-\frac{1}{3}e^x\cos(3x) + \frac{1}{3}\int e^x\cos(3x)dx)$

$\int e^x \cos(3x) dx = \frac{1}{3}e^x\sin(3x) + \frac{1}{9}e^x\cos(3x) - \frac{1}{9}\int e^x\cos(3x)dx$

Resolviendo para la integral:
$\int e^x \cos(3x) dx + \frac{1}{9}\int e^x\cos(3x)dx = \frac{1}{3}e^x\sin(3x) + \frac{1}{9}e^x\cos(3x)$

$\frac{10}{9}\int e^x \cos(3x) dx = \frac{1}{3}e^x\sin(3x) + \frac{1}{9}e^x\cos(3x)$

**Resultado final:**
$$\int e^x \cos(3x) dx = \frac{e^x}{10}(3\sin(3x) + \cos(3x)) + C$$

## 3. $\int \cos^3(4x) dx$

$\cos^3(4x) = \cos^2(4x)\cos(4x) = (1-\sin^2(4x))\cos(4x)$

$\int \cos^3(4x) dx = \int (1-\sin^2(4x))\cos(4x) dx$

Sea $u = \sin(4x)$, entonces $du = 4\cos(4x)dx$, por lo que $\cos(4x)dx = \frac{1}{4}du$

$\int \cos^3(4x) dx = \int (1-u^2)\frac{1}{4}du = \frac{1}{4}\int (1-u^2)du$

$= \frac{1}{4}(u - \frac{u^3}{3}) = \frac{1}{4}(\sin(4x) - \frac{\sin^3(4x)}{3})$

**Resultado final:**
$$\int \cos^3(4x) dx = \frac{1}{4}\sin(4x) - \frac{1}{12}\sin^3(4x) + C$$

## 4. $\int \tan^3(2\theta)\sec^4(2\theta) d\theta$


$\tan^3(2\theta)\sec^4(2\theta) = \tan^3(2\theta)\sec^2(2\theta)\sec^2(2\theta) = \tan^3(2\theta)(1+\tan^2(2\theta))\sec^2(2\theta)$

Sea $u = \tan(2\theta)$, entonces $du = 2\sec^2(2\theta)d\theta$, por lo que $\sec^2(2\theta)d\theta = \frac{1}{2}du$

$\int \tan^3(2\theta)\sec^4(2\theta) d\theta = \int u^3(1+u^2)\frac{1}{2}du = \frac{1}{2}\int (u^3 + u^5)du$

$= \frac{1}{2}(\frac{u^4}{4} + \frac{u^6}{6}) = \frac{u^4}{8} + \frac{u^6}{12}$

**Resultado final:**
$\int \tan^3(2\theta)\sec^4(2\theta) d\theta = \frac{\tan^4(2\theta)}{8} + \frac{\tan^6(2\theta)}{12} + C$

## 5. $\int \frac{dx}{x \sqrt{\ln^2(x)+4}}$

Sea $u = \ln(x)$, entonces $du = \frac{1}{x}dx$

$\int \frac{dx}{x \sqrt{\ln^2(x)+4}} = \int \frac{du}{\sqrt{u^2+4}}$

Esta es una integral estándar de la forma $\int \frac{du}{\sqrt{u^2+a^2}} = \ln|u + \sqrt{u^2+a^2}| + C$

Con $a = 2$:

**Resultado final:**
$$\int \frac{dx}{x \sqrt{\ln^2(x)+4}} = \ln|\ln(x) + \sqrt{\ln^2(x)+4}| + C$$

## 6. $\int \frac{dx}{x^{\frac{1}{3}} (x^{\frac{2}{3}}+4)}$

Sea $u = x^{\frac{1}{3}}$, entonces $x = u^3$ y $dx = 3u^2 du$

También $x^{\frac{1}{3}} = u$ y $x^{\frac{2}{3}} = u^2$

$\int \frac{dx}{x^{\frac{1}{3}} (x^{\frac{2}{3}}+4)} = \int \frac{3u^2 du}{u(u^2+4)} = 3\int \frac{u du}{u^2+4}$

Para $\int \frac{u du}{u^2+4}$, sea $v = u^2+4$, entonces $dv = 2u du$, por lo que $u du = \frac{1}{2}dv$

$3\int \frac{u du}{u^2+4} = 3 \cdot \frac{1}{2}\int \frac{dv}{v} = \frac{3}{2}\ln|v| = \frac{3}{2}\ln|u^2+4|$

**Resultado final:**
$$\int \frac{dx}{x^{\frac{1}{3}} (x^{\frac{2}{3}}+4)} = \frac{3}{2}\ln|x^{\frac{2}{3}}+4| + C$$

## 7. $\int (e^{7x}+1)^3 e^{7x} dx$

**Método:** Sustitución

Sea $u = e^{7x}+1$, entonces $du = 7e^{7x}dx$, por lo que $e^{7x}dx = \frac{1}{7}du$

$\int (e^{7x}+1)^3 e^{7x} dx = \int u^3 \frac{1}{7}du = \frac{1}{7}\int u^3 du = \frac{1}{7} \cdot \frac{u^4}{4} = \frac{u^4}{28}$

**Resultado final:**
$$\int (e^{7x}+1)^3 e^{7x} dx = \frac{(e^{7x}+1)^4}{28} + C$$

## 8. $\int \tan^5(2x)\sec^2(2x) dx$

**Método:** Sustitución trigonométrica

Sea $u = \tan(2x)$, entonces $du = 2\sec^2(2x)dx$, por lo que $\sec^2(2x)dx = \frac{1}{2}du$

$\int \tan^5(2x)\sec^2(2x) dx = \int u^5 \frac{1}{2}du = \frac{1}{2}\int u^5 du = \frac{1}{2} \cdot \frac{u^6}{6} = \frac{u^6}{12}$

**Resultado final:**
$$\int \tan^5(2x)\sec^2(2x) dx = \frac{\tan^6(2x)}{12} + C$$