# MIT integration bee - 2020

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

$$ \int \frac{\log(2x)}{x \log x}  dx $$

$$\textcolor{green}{--- \text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{ \ln(2) + \ln(x)}{x \ln x} ~\right\}\\
    &=& \displaystyle \left\{~ \frac{ \ln(2) + t}{t} ~\right\} & (1)\\
    &=& \displaystyle \ln(2) \ln|t| + t + C\\
    &=& \displaystyle \ln(2) \ln|\ln(x)| + \ln(x) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} t &=& \ln(x) \\ dt &=& \frac{1}{x} dx \end{array} \right.$

## Ejercicio 2

$$\int_0^\infty \frac{1}{e^x + 1}  dx$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{e^{u}}{e^u + 1} ~\right\}_{-\infty}^{0} & (1)\\
    &=& \displaystyle \left( \ln|e^u + 1| \right)_{-\infty}^{0}\\
    &=& \displaystyle \ln(2)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& -u \\ dx &=& -du \end{array} \right.$

## Ejercicio 3

$$\int_e^{e^e} \frac{\log x \cdot \log (\log x)}{x}  dx$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ t \ln(t) ~\right\}_{1}^{e} & (1)\\
    &=& \displaystyle  \frac{1}{2}\left(~ t^2\ln(t) ~\right)_{1}^{e} - \frac{1}{2} \left\{~ t ~\right\}_{1}^{e} & (2)\\
    &=& \displaystyle  \frac{e^2}{2} - \frac{1}{2} \left(~ \frac{t^2}{2} ~\right)_{1}^{e} &\\
    &=& \displaystyle  \frac{e^2}{4} + \frac{1}{4} &\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} t &=& \ln(x) \\ dt &=& \frac{1}{x} dx \end{array} \right.$

- (2): $\begin{array}{|c|c|} D & I \\ \ln(t) & t \\ \frac{1}{t} & \frac{t^2}{2} \end{array}$

## Ejercicio 4

$$\int_0^1 \log \left( \frac{1 + x}{1 - x} \right)  dx$$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I_1 &=& \displaystyle x \ln \left( \frac{1 + x}{1 - x} \right)  - 2\left\{~ \frac{x}{1-x^2} ~\right\} & (1)\\
    &=& \displaystyle x \ln \left( \frac{1 + x}{1 - x} \right)  + \ln|1-x^2| + C & (2)\\ \\
    I &=& \left( x \ln \left( \frac{1 + x}{1 - x} \right)  + \ln|1-x^2| \right)_{0}^{1}\\
    &=& \left(~~ x \ln \left(~ (1+x)^2 ~\right) ~~\right)_{0}^{1}\\
    &=& \ln(4)
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \ln(\frac{1+x}{1-x}) & dx \\ \frac{2}{1-x^2} & x \end{array}$

- (2): $[\ln(f(x))]= \frac{f'(x)}{f(x)}$

**Nota:**

1. Al aplicar integración por partes debemos de tener cuidado con las integrales impropias:

    $$
    I =  \textcolor{red}{\left( x \ln \left( \frac{1 + x}{1 - x} \right) \right)_{0}^{1}} - 2\left\{~ \frac{x}{1-x^2} ~\right\}_{0}^{1}
    $$

## Ejercicio 5

$$\int \frac{1}{x^2 + (x - 1)^2}  dx$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle - \left\{~ \frac{1}{1 + ( 1 - t)^2} ~\right\} & (1)\\
    &=& \displaystyle \arctan(1-t) + C\\
    &=& \displaystyle \arctan\left( 1-\frac{1}{x} \right) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \frac{1}{t} \\ dx &=& -\frac{1}{t^2} dt \end{array} \right.$

## Ejercicio 6

$$\int \sqrt{x \sqrt{x \cdots x}}  dx$$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ x^{1/2} x^{1/4} x^{1/8} \cdots ~\right\}\\
    &=& \displaystyle \left\{~ x^{\sum_{n \geq 1} (1/2)^n} ~\right\}\\
    &=& \displaystyle \left\{~ x^{\sum_{n \geq 0} (1/2)^n - 1} ~\right\}\\
    &=& \displaystyle \left\{~ x^{2 - 1} ~\right\} & (1)\\
    &=& \displaystyle \frac{x^2}{2} + C & \\
\end{array}
$$

- (1): Serie geométrica $\sum_{n \geq 0} r^n = \frac{1}{1-r}$ con $|r|<1$

## Ejercicio 7

$$\int \sin^4 x \cos^4 x (\cos x + \sin x)(\cos x - \sin x)  dx$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sin^4 x \cos^4 x (\cos^2 x - \sin^2 x) ~\right\}\\
    &=& \displaystyle \left\{~ \sin^4 x \cos^4 x \cos(2x) ~\right\} & (1)\\
    &=& \displaystyle \frac{1}{2^4}\left\{~ (2 \sin x \cos x)^4 \cos(2x) ~\right\}\\
    &=& \displaystyle \frac{1}{2^4}\left\{~ \sin^4(2x) \cos(2x) ~\right\} & (2)\\
    &=& \displaystyle \frac{1}{2^5} \frac{\sin^5(2x)}{5} + C\\
    &=& \displaystyle \frac{\sin^5(x) \cos^5(x)}{5} + C\\
\end{array}
$$

- (1): $\cos(2x) = \cos^2(x) - \sin^2(x)$

- (2): $\sin(2x) = 2 \sin(x)\cos(x)$

## Ejercicio 8

$$\int \log(x^2 + 1)  dx$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle x \ln(1+x^2) - 2 \left\{~ \frac{x^2}{1+x^2} ~\right\} & (1)\\
    &=& \displaystyle x \ln(1+x^2) - 2 \left\{~ 1 - \frac{1}{1+x^2} ~\right\}\\
    &=& \displaystyle x \ln(1+x^2) - 2 \left(~ x - \arctan(x) ~\right) + C\\
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \ln(1 + x^2) & dx \\ \frac{2x}{1+x^2} & x \end{array}$

## Ejercicio 9

$$\int_0^{2\pi} \cos^{2020}(x)  dx$$

$$\textcolor{red}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{2\pi}{2^{2020}} \binom{2020}{1010} & (1)\\
\end{array}
$$

- (1): Usando variable compleja tenemos el siguiente resultado: <https://math.stackexchange.com/questions/1366304/integration-of-int-02-pi-cos2ntdt?noredirect=1>

    $$
    \int_{0}^{2\pi} \cos^{2n}(x) ~dx = \frac{2\pi}{2^{2n}} \binom{2n}{n}
    $$

## Ejercicio 10

$$\int \frac{2x + 1}{2x^2 + 2x + 1}  dx$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2} \left\{~ \frac{4x + 2}{2x^2 + 2x + 1} ~\right\}\\
    &=& \displaystyle \frac{1}{2} \ln|2x^2+2x+1| + C & (1)\\
\end{array}
$$

- (1): $[\ln(f(x))] = \frac{f'(x)}{f(x)}$

## Ejercicio 11

$$\int_{1/\sqrt{2}}^{1} \frac{\arcsin(x)}{x^3}  dx$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle -\frac{1}{2} \left(~ \frac{\arcsin(x)}{x^2} ~\right)_{1/\sqrt{2}}^{1} + \frac{1}{2} \left\{~ \frac{1}{x^2\sqrt{1-x^2}} ~\right\}_{1/\sqrt{2}}^{1} & (1)\\
    &=& \displaystyle \frac{1}{2} \left\{~ \frac{1}{x^2\sqrt{1-x^2}} ~\right\}_{1/\sqrt{2}}^{1}\\
    &=& \displaystyle \frac{1}{2} \left\{~ \csc^2(\theta) ~\right\}_{\pi/4}^{\pi/2} & (2)\\
    &=& \displaystyle - \frac{1}{2} \left(~ \cot(\theta) ~\right)_{\pi/4}^{\pi/2}\\
    &=& \displaystyle \frac{1}{2} \\
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \arcsin(x) & \frac{1}{x^3} \\ \frac{1}{\sqrt{1-x^2}} & - \frac{1}{2x^2}\end{array}$

- (2): $\left\{\begin{array}{rcl} x &=& \sin(\theta) \\ dx &=& \cos(\theta) d\theta \end{array} \right.$

## Ejercicio 12

$$\int_{0}^{\pi/2} \sin(2x) \cos(\cos(x))  dx$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2 \left\{~ \sin(x)\cos(x) \cos(\cos(x)) ~\right\}_{0}^{\pi/2} & (1)\\
    &=& \displaystyle 2 \left\{~ u\cos(u) ~\right\}_{0}^{1} & (2)\\
    &=& \displaystyle 2 \left(~ u\sin(u) + \cos(u) ~\right)_{0}^{1} & (3)\\
    &=& \displaystyle 2 \left(~ \sin(1) + \cos(1) - 1  ~\right)\\
\end{array}
$$

- (1): $\sin(2x) = 2 \sin(x)\cos(x)$

- (2): $\left\{\begin{array}{rcl} u &=& \cos(x) \\ du &=& -\sin(x) dx \end{array} \right.$

- (3): $\begin{array}{|c|c|} D & I \\ u & \cos(u) \\ 1 & \sin(u) \\ 0 & -\cos(u) \end{array}$

## Ejercicio 13

$$\int_{0}^{2\pi} \sin(\sin(x) - x)  dx$$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sin(\sin(x) - x) ~\right\}_{0}^{\pi} + \left\{~ \sin(\sin(x) - x) ~\right\}_{\pi}^{2\pi}\\ \\ 
    I_1 &=& \displaystyle \left\{~ \sin(~\sin(x + \pi) - (x+\pi)~) ~\right\}_{0}^{\pi}\\
    &=& \displaystyle \left\{~ \sin(~ - (\sin(x) +x + \pi)~) ~\right\}_{0}^{\pi} & (1)\\
    &=& \displaystyle \left\{~ \sin(~ \sin(x) + x + \pi ~) ~\right\}_{0}^{\pi} & (2)\\
    &=& \displaystyle \left\{~ \sin(~ \sin(x) + x ~) ~\right\}_{0}^{\pi} & (1)\\
    &=& \displaystyle \left\{~ \sin(\sin(x)) \cos(x)  + \cos(\sin(x)) \sin(x) ~\right\}_{0}^{\pi} & (3)\\ \\
    I_2 &=& \displaystyle \left\{~ \sin(\sin(x) - x) ~\right\}_{0}^{\pi}\\
    &=& \displaystyle \left\{~ \sin(\sin(x)) \cos(x) - \cos(\sin(x))\sin(x) ~\right\}_{0}^{\pi}\\ \\
    I &=& \displaystyle 2 \left\{~ \sin(\sin(x)) \cos(x)  ~\right\}_{0}^{\pi}\\
    &=& \displaystyle -2 \left(~ \cos(\sin(x)) ~\right)_{0}^{\pi} & (4)\\
    &=& \displaystyle 0
\end{array}
$$

- (1): $\sin(x + \pi) = - \sin(x)$

- (2): Función impar

- (3): $\sin(a \pm b) = \sin(a)\cos(b) \pm \cos(a)\sin(b)$

- (4): $[f(g(x))] = f'(g(x))g'(x)$

## Ejercicio 14

$$\int \frac{1}{x-1} + \frac{\sum_{k=0}^{2018}(k+1)x^k}{\sum_{k=0}^{2019}x^k}  dx$$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1}{x-1} + \frac{\sum_{k=0}^{\alpha-1}(k+1)x^k}{\sum_{k=0}^{\alpha}x^k} ~\right\}\\
    &=& \displaystyle \ln|x-1| + \left\{~ \frac{\sum_{k=0}^{\alpha-1}(k+1)x^k}{\sum_{k=0}^{\alpha}x^k} ~\right\}\\
    &=& \displaystyle \ln|x-1| + \ln \left| \sum_{k=0}^{\alpha}x^k \right| +  C & (1)\\
    &=& \displaystyle \ln|x-1| + \ln \left| \frac{x^{\alpha+1} - 1}{x-1} \right| +  C & (2)\\
    &=& \displaystyle \ln \left| x^{\alpha+1} - 1 \right| +  C & (2)\\
\end{array}
$$

- (1): $[\sum_{k=0}^{\alpha}x^k] = [1 + \sum_{k=1}^{\alpha}x^k] = \sum_{k=1}^{\alpha}kx^{k-1} = \sum_{k=0}^{\alpha-1}(k+1)x^{k}$

- (2): $a^n - b^n = (a-b) (a^{n-1}+a^{n-2}b + \cdots + b^{n-2}a + b^{n-1})$

## Ejercicio 15

$$\int_{0}^{\frac{\pi}{2}} \frac{1}{\tan^{\sqrt{2020}}(x)+1}  dx$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1}{\tan^{\alpha}(x)+1} ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle \left\{~ \frac{1}{\cot^{\alpha}(\theta)+1} ~\right\}_{0}^{\pi/2} & (1),(2)\\ \\
    2I &=& \displaystyle \left\{~ \frac{1}{\tan^{\alpha}(x)+1} + \frac{1}{\cot^{\alpha}(x)+1} ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle \left\{~ \frac{\cos^{\alpha}(x)}{\sin^{\alpha}(x) + \cos^{\alpha}(x)} + \frac{\sin^{\alpha}(x)}{\sin^{\alpha}(x) + \cos^{\alpha}(x)} ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle \left\{~ 1 ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle \pi/2 \\ \\
    I &=& \pi/4
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \pi/2 - \theta \\ dx &=& -d\theta \end{array} \right.$

- (2): $\tan(\pi/2 - x) = \cot(x)$

## Ejercicio 16

$$\int x(1-x)^{2020}  dx$$  

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle - \left\{~ (1-u)u^{\alpha} ~\right\} & (1)\\
    &=& \displaystyle - \frac{u^{\alpha+1}}{\alpha+1} + \frac{u^{\alpha+2}}{\alpha+2} + C \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& 1 -x \\ du &=& -dx \end{array} \right.$

## Ejercicio 17

$$\int \frac{\sec^{4}(x) \tan(x)}{\sec^{4}(x)+4}  dx$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{4} \left\{~ \frac{4\sec^{3}(x) \sec(x)\tan(x)}{\sec^{4}(x)+4} ~\right\}\\
    &=& \displaystyle \frac{1}{4} \ln |\sec^4(x) + 4| + C & (1),(2)\\
\end{array}
$$

- (1) $[\sec^4(x)] = 4 \sec^4(x)\tan(x)$

- (2) $[\ln(f(x))] = \frac{f'(x)}{f(x)}$

## Ejercicio 18

$$\int x^{2x}(2\log(x)+2)  dx$$  

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle x^{2x} + C & (1)\\
\end{array}
$$

- (1): $[x^{2x}] = [e^{2x\ln(x)}] = e^{2x\ln(x)}(2\ln(x) + 2) = x^{2x}(2\log(x)+2)$

## Ejercicio 19

$$\int_{0}^{1} \sqrt{1-x^2}  dx$$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

Sea $y = \sqrt{1-x^2}$, entonces $y^2 + x^2 = 1$ que representa la ecuación de una circunferencia de radio $r=1$ y centro en $(0,0)$. Así pues, la integral está calculando una cuarta parte del área de esta circunferencia.

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{\pi r^2}{4}\\
    &=& \displaystyle \frac{\pi}{4}\\
\end{array}
$$

## Ejercicio 20

$$ \int_{0}^{\infty} x^5 e^{-x^4}  dx$$  

$$\textcolor{red}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ x^3 x^2 e^{-x^4}  ~\right\}_{0}^{\infty}\\
    &=& \displaystyle \frac{1}{4} \left\{~ u^{1/2} e^{-u}  ~\right\}_{0}^{\infty} & (1)\\
    &=& \displaystyle \frac{1}{4} \Gamma(3/2)\\
    &=& \displaystyle \frac{1}{8} \Gamma(1/2) & (3)\\
    &=& \displaystyle \frac{\sqrt{\pi}}{8} & (4)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& x^4 \\ du &=& 4x^3 ~dx \end{array} \right.$

- (2): Funcion Gamma $\Gamma(n) = \{ t^{n-1} e^{-t}\}_{0}^{\infty}$

- (3): $\Gamma(x+1) = x \Gamma(x)$

- (4): $\Gamma(1/2) = \sqrt{\pi}$ que se puede deducir de la integral Gaussiana $\{e^{-x^2}\}_{-\infty}^{\infty} = \sqrt{\pi}$
