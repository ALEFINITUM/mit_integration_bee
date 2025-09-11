# MIT integration bee - 2013

## Notación y Consideraciones Generales

A lo largo del documento vamos a utilizar la siguiente notación, en algunos problemas más complejos utilizaremos la notación usual:

$$
\{~f(x)~\}_{a}^{b}:= \int_{a}^{b} f(x) ~dx ~~,~~ [~f(x)~]:= \frac{d}{dx}f(x)
$$

Recursos obtenidos de: <https://math.mit.edu/~yyao1/integrationbee.html>

Herramientas que te pueden ser útiles:

- Calculadora gráfica: <https://www.desmos.com/calculator?lang=es>
- Calculadora de integrales: <https://mathdf.com/es/>
- Calculadora de integrales: <https://www.wolframalpha.com/>
- Motor de busqueda para fórmulas en latex <https://approach0.xyz/search/>
- Te ayuda con ideas: <https://chat.deepseek.com>

## Ejercicio 1

$$ \int \log(x^2) - 2\log(2x)  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ -\ln(4) ~\right\} \\
    &=& \displaystyle - \ln(4) x +  C\\
\end{array}
$$

## Ejercicio 2

$$ \int_{-1}^3 e^{|x|}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ e^{|x|} ~\right\}_{-1}^{0} + \left\{~ e^{|x|} ~\right\}_{0}^{3} \\
    &=& \displaystyle \left\{~ e^{-x} ~\right\}_{-1}^{0} + \left\{~ e^{x} ~\right\}_{0}^{3} \\
    &=& \displaystyle -\left(~ e^{-x} ~\right)_{-1}^{0} + \left(~ e^{x} ~\right)_{0}^{3} \\
    &=& \displaystyle e^3 + e^1 - 2 \\
\end{array}
$$

## Ejercicio 3

$$ \int \frac{(\log x)(\cos x) - (\sin x)(1/x)}{(\log x)^2}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{\sin(x)}{\ln(x)} + C & (1)\\
\end{array}
$$

- (1): $\left[ \frac{f(x)}{\ln(x)}\right] = \frac{f'(x)\ln(x)-f(x)\frac{1}{x}}{\ln^2(x)}$

## Ejercicio 4

$$ \int_1^{11} x^3 - 3x^2 + 3x - 1  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ (x-1)^3 ~\right\}_{1}^{11} & (1)\\
    &=& \displaystyle \frac{1}{4}\left(~ (x-1)^4 ~\right)_{1}^{11}\\
    &=& \displaystyle \frac{10^4}{4}\\
\end{array}
$$

- (1): triángulo de pascal

## Ejercicio 5

$$ \int_0^2 \sqrt{12 - 3x^2}  dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

Sea $y = \sqrt{12 - 3x^2}$, entonces $\left(\frac{x}{2}\right)^2 + \left(\frac{y}{2\sqrt{3}}\right)^2 = 1$, esta es la ecuación de una elipse con centro en $(0,0)$, eje mayor paralelo al eje $y$, y radios $r_1 = 2$ $r_2 = 2 \sqrt{3}$.

Sabemos que el area de una elipse en $\pi \cdot r_1 \cdot r_2$ y como la integral nos esta calculando una cuarta parte del área de la elipse tenemos que:

$$
I = \frac{\pi \cdot 2 \cdot 2\sqrt{3}}{4} = \pi \sqrt{3}
$$

## Ejercicio 6

$$ \int_{0}^{6} x + (x - 3)^7 + \sin(x - 3)  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left(~ \frac{x^2}{2} ~\right)_{0}^{6} + \left(~ \frac{(x-3)^8}{8} ~\right)_{0}^{6} - \left(~ \cos(x-3) ~\right)_{0}^{6}\\
    &=& \displaystyle 18
\end{array}
$$

**Nota:**

1. Si $f$ es una función impar entonces $\int_{-a}^{a} f(x) ~dx = 0$

## Ejercicio 7

$$ \int \sin x \sqrt{1 + \tan^2 x}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\sin(x)}{\cos(x)} ~\right\} & (1)\\
    &=& \displaystyle -\ln|\cos(x)| + C & (2)\\
\end{array}
$$

- (1): $1 + \tan^2(x) = \sec^2(x)$

- (2): $[\ln(f(x))] = \frac{f'(x)}{f(x)}$

## Ejercicio 8

$$ \int \frac{x^5 - x^3 + x^2 - 1}{x^4 - x^3 + x - 1}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ x+1 ~\right\}\\
    &=& \displaystyle \frac{x^2}{2} + x + C\\
\end{array}
$$

- (1): $1 + \tan^2(x) = \sec^2(x)$

- (2): $[\ln(f(x))] = \frac{f'(x)}{f(x)}$

## Ejercicio 9

$$ \int_{0}^{1} \log x  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left(~ x \ln(x) - x ~\right)_{0}^{1}& (1)\\
    &=& \displaystyle -1 \\
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \ln(x) & dx \\ \frac{1}{x} & x \end{array}$

## Ejercicio 10

$$ \int \frac{1}{1 - e^{-x}}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{e^x}{e^x-1} ~\right\} \\
    &=& \displaystyle \ln |e^x - 1 | + C & (1)\\
\end{array}
$$

- (1): $[\ln(f(x))] = \frac{f'(x)}{f(x)}$

## Ejercicio 11

$$ \int_{0}^{\pi} \sin^2 x \cos^2 x  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sin^2(\theta) \cos^2(\theta) ~\right\}_{-\pi/2}^{\pi/2} & (1),(2)\\
    &=& \displaystyle 2 \left\{~ \sin^2(\theta) \cos^2(\theta) ~\right\}_{0}^{\pi/2} & (3)\\
    &=& \displaystyle \frac{1}{2} \left\{~ \sin(2\theta)^2 ~\right\}_{0}^{\pi/2} & (4)\\
    &=& \displaystyle \frac{1}{4} \left\{~ 1 - \cos(4x) ~\right\}_{0}^{\pi/2} & (5)\\
    &=& \displaystyle \frac{\pi}{8}
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \pi/2 - \theta \\ dx &=& -d\theta \end{array} \right.$

- (2): $\sin(\pi/2 - x) = \cos(x)$ y $\cos(\pi/2 - x) = \sin(x)$

- (3): función par en un intervalo simétrico

- (4): $\sin(2x) = 2 \sin(x)\cos(x)$

- (5): $\cos(2x) = 1 - 2\sin^2(x)$

## Ejercicio 12

$$ \int_{0}^{441} \frac{\pi \sin(\pi \sqrt{x})}{\sqrt{x}}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2 \pi \left\{~ \sin(u \pi) ~\right\}_{0}^{21} & (1)\\
    &=& \displaystyle -2 \left(~ \cos(u \pi) ~\right)_{0}^{21}\\
    &=& \displaystyle 4\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} t &=& \sqrt{x} \\ dt &=& \frac{1}{2}\frac{1}{\sqrt{x}}~ dx \end{array} \right.$

## Ejercicio 13

$$ \int \tan^2 x  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sec^2(x) - 1 ~\right\} & (1)\\
    &=& \displaystyle \tan(x) - x + C & (2)\\
\end{array}
$$

- (1): $1 + \tan^2(x) = \sec^2(x)$

- (2): $[\tan(x)] = \sec^2(x)$

## Ejercicio 14

$$ \int_0^{256} (x - \lfloor x \rfloor)^2  dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 256 \left\{~ \text{dec}^2(x) ~\right\}_{0}^{1} & (1)\\
    &=& \displaystyle 256\left\{~ x^2 ~\right\}_{0}^{1}& (2)\\
    &=& \displaystyle \frac{256}{3}\\
\end{array}
$$

- (1): la función parte decimal $\text{dec}(x) = x - \lfloor x \rfloor$ es de periodo $1$

- (2): Si $x \in (0,1)$, entonces $\text{dec}(x) = x$

**Nota:**

1. Sea $n \in \mathbb{Z}$ y $x \in \mathbb{R}$, entonces $\lfloor n + x \rfloor = n + \lfloor x \rfloor$

## Ejercicio 15

$$ \int e^{\sqrt[4]{x}}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 4 \left\{~ t^3 e^t ~\right\} & (1)\\
    &=& \displaystyle 4 (t^3e^t - 3t^2e^t + 6te^t - 6e^t) + C & (2)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^4 \\ dx &=& 4 t^3 ~dt \end{array} \right.$

- (2): $\begin{array}{|c|c|} D & I \\ t^3 & e^t \\ 3t^2 & e^t \\ 6 t & e^t \\ 6 & e^t \\ 0 & e^t \end{array}$

## Ejercicio 16

$$ \int \cos x \cot x  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\cos^2(x)}{\sin(x)} ~\right\}\\
    &=& \displaystyle \left\{~ \frac{1 - \sin^2(x)}{\sin(x)} ~\right\} & (1)\\
    &=& \displaystyle \left\{~ \csc(x) \right\} - \left\{~ \sin(x) ~\right\} \\
    &=& \displaystyle - \ln |\csc(x) + \cot(x)| + \cos(x) + C & (2),(3) \\
\end{array}
$$

- (1): $\cos^2(x) + \sin^2(x) = 1$

- (2): $[\csc(x) + \cot(x)] = -\csc(x)(\csc(x) + \cot(x))$

- (3): $[\ln(f(x))] = \frac{f'(x)}{f(x)}$

## Ejercicio 17

$$ \int 2 \log x + (\log x)^2  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ (2t + t^2) e^t ~\right\} & (1)\\
    &=& \displaystyle 2te^t - 2e^t + t^2e^t - 2t e^t + 2e^t & (2)\\
    &=& \displaystyle t^2e^t + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& e^t \\ dx &=& e^t ~dt \end{array} \right.$

- (2): $\begin{array}{|c|c|} D & I \\ t^2 & e^t \\ 2t & e^t \\ 2 & e^t \\ 0 & e^t \end{array}$

## Ejercicio 18

$$ \int \frac{x^3}{1 + x^2}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2} \left\{~ \frac{u-1}{u} ~\right\} & (1)\\
    &=& \displaystyle \frac{1}{2} \left(~ u - \ln|u| ~\right) + C \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& 1 + x^2 \\ du &=& 2x ~dx \end{array} \right.$

## Ejercicio 19

$$ \int \frac{1}{2 - 2x + x^2}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1}{(x-1)^2+1} ~\right\}\\
    &=& \displaystyle \arctan(x-1) + C\\
\end{array}
$$

## Ejercicio 20

$$ \int \sin x \log(\sin x)  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle - \cos(x) \ln(\sin(x)) + \left\{~ \cos(x) \cot(x) ~\right\} & (1) \\
    &=& \displaystyle - \cos(x) \ln(\sin(x)) - \ln |\csc(x) + \cot(x)| + \cos (x) + C & (2) \\
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \ln(\sin(x)) & \sin(x) \\ \frac{\cos(x)}{\sin(x)} & -\cos(x) \end{array}$

- (2): Ver ejercicio $16$

## Ejercicio 21

$$ \int \frac{x}{1-x^4}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2} \left\{~ \frac{1}{1-u^2} ~\right\} & (1) \\
    &=& \displaystyle \frac{1}{4} \left\{~ \frac{1}{1-u} + \frac{1}{1+u}  ~\right\} \\
    &=& \displaystyle \frac{1}{4} \left(~ -\ln|1-u| + \ln|1+u|  ~\right) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} t &=& x^2 \\ dt &=& 2x ~dx \end{array} \right.$

## Ejercicio 22

$$ \int \sqrt{12-3x^2}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \sqrt{3} \left\{~ \sqrt{4-x^2}~\right\}\\
    &=& \displaystyle 4\sqrt{3} \left\{~ \cos^2(\theta)~\right\} & (1)\\
    &=& \displaystyle 2\sqrt{3} \left\{~ \cos(2\theta)+ 1~\right\} & (2)\\
    &=& \displaystyle 2\sqrt{3} \left(~ \frac{\sin(2 \theta)}{2}+ \theta ~\right) + C \\
    &=& \displaystyle 2\sqrt{3} \left(~ \frac{x\sqrt{4-x^2}}{4}+ \arcsin(x/2) ~\right) + C \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& 2\sin(\theta) \\ dx &=& 2\cos(\theta) ~dx \end{array} \right.$

- (2): $\cos(2x) = 2 \cos^2(x)-1$

## Ejercicio 23

$$ \int \sec^5 x \tan^3 x  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sec^4(x)(\sec^2(x)-1)\sec(x)\tan(x) ~\right\}\\
    &=& \displaystyle \left\{~ u^4(u^2-1) ~\right\} & (1)\\
    &=& \displaystyle \frac{u^7}{7} + \frac{u^5}{5} + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& \sec(x) \\ du &=& \sec(x)\tan(x) ~dx \end{array} \right.$

## Ejercicio 24

$$ \int_{-\pi/4}^{\pi/4} \frac{1}{1-\sin x}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\sec(x)}{\sec(x) - \tan(x)} ~\right\}_{-\pi/4}^{\pi/4}\\
    &=& \displaystyle \left\{~ \frac{\sec(x)(\sec(x) - \tan(x))}{(\sec(x) - \tan(x))^2} ~\right\}_{-\pi/4}^{\pi/4}\\
    &=& \displaystyle \left(~ \frac{1}{\sec(x)-\tan(x)}~\right)_{-\pi/4}^{\pi/4} & (2),(3)\\
    &=& \displaystyle 2 \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& \sec(x) \\ du &=& \sec(x)\tan(x) ~dx \end{array} \right.$

- (2): $[\sec(x) - \tan(x)] = \sec(x)(\tan(x) - \sec(x))$

- (3): $[\frac{1}{f(x)}] = -\frac{f`(x)}{f^2(x)}$

## Ejercicio 25

$$ \int \frac{1}{x\sqrt{x^2-2}}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2}\left\{~ \frac{1}{ \frac{x}{\sqrt{2}}\sqrt{ \left(\frac{x}{\sqrt{2}} \right)^2-1}} ~\right\}\\
    &=& \displaystyle \frac{\sqrt{2}}{2} \text{arcsec} \left(\frac{x}{\sqrt{2}} \right) + C\\
\end{array}
$$

**Nota:**

1. Derivadas de las funciones trigonométricas inversas:

    $$
    \left \{
    \begin{array}{ccc}
        [\text{arcsin}(x)] &=& \frac{1}{\sqrt{1-x^2}}\\
        [\text{arccos}(x)] &=& \frac{-1}{\sqrt{1-x^2}}\\
        [\text{arctan}(x)] &=& \frac{1}{x^2+1}\\
        [\text{arccot}(x)] &=& \frac{-1}{x^2+1}\\
        [\text{arcsec}(x)] &=& \frac{1}{|x|\sqrt{x^2-1}}\\
        [\text{arccsc}(x)] &=& \frac{-1}{|x|\sqrt{x^2-1}}\\
    \end{array}
    \right.
    $$
