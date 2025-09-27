# MIT integration bee - 2014

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

$$ \int_{1}^{e} \log(x^n)  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \left(x\ln(x^n) - nx \right)_{1}^{e} & (1)\\
    &=& n
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \ln(x^n) & dx \\ \frac{n}{x} & x \end{array}$

## Ejercicio 2

$$ \int_{-9}^{9} \sin(\sqrt[3]{x})  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 0 & (1)
\end{array}
$$

- (1): función impar en intervalo de integración simétrico.

## Ejercicio 3

$$ \int_{0}^{\infty} \frac{d}{dx} \left[ e^{1+x-x^2} \right]  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left( e^{1+x-x^2} \right)_{0}^{\infty} & (1)\\
    &=& \displaystyle -e
\end{array}
$$

- (1): Teorema fundamental del cálculo

## Ejercicio 4

$$ \int_{0}^{2} \sqrt{x + \sqrt{x + \sqrt{x + \cdots}}}  dx $$

$$\textcolor{red}{---\text{ Demostración } ---}$$

Considere la siguiente sucesión:

$$
a_1 = \sqrt{x} ~~,~~ a_{n+1} = \sqrt{x + a_n} ~~~~\text{para } x \in [0,2]
$$

Veamos que $\{a_n\}_{n \geq 1}$ converge para todo $x \in [0,2]$.

**(Monótona Creciente)** Usando induccion matemática tenemos que:

$$
\begin{array}{rclr}
    0 &\leq& \sqrt{x}\\
    x &\leq& x + \sqrt{x}\\
    \sqrt{x} &\leq& \sqrt{x + \sqrt{x}}\\
    a_1 &\leq& a_2\\
\end{array}
$$

Suponiendo que para $n \in \mathbb{N}$ se tiene que $a_{n} \geq a_{n-1}$, entonces:

$$
\begin{array}{rclr}
    a_{n-1} &\leq& a_{n}\\
    x + a_{n-1} &\leq& x + a_{n}\\
    \sqrt{x + a_{n-1}} &\leq& \sqrt{x + a_{n}}\\
    a_{n} &\leq& a_{n+1}\\
\end{array}
$$

Así pues, la sucesión $\{a_n\}_{n \geq 1}$ es monótona creciente.

**(Acotada Superiormente)** Veamos que la sucesión $\{a_n\}_{n \geq 1}$ es acotada superiormente por $2$. Razonemos por inducción matemática.

Claramente tenemos que $a_1 \leq \sqrt{2} \leq 2$ pues $x \in [0,2]$, ahora suponiendo que para $n \in \mathbb{N}$ se tiene que $a_n \leq 2$, entonces:

$$
\begin{array}{rclr}
    a_n &\leq& 2 \\
    x + a_n &\leq& x + 2 \\
    \sqrt{x + a_n} &\leq& \sqrt{x + 2} \\
    a_{n+1} &\leq& \sqrt{x + 2} \\
    &\leq& \sqrt{2 + 2} \\
    &=& 2 \\
\end{array}
$$

Así pues, la sucesión $\{a_n\}_{n \geq 1}$ es acotada superiormente por $2$.

Considere la función $f(x) = \lim_{n \to \infty} a_n(x)$ definida para todo $x \in [0,2]$, esta función esta bien definida pues ya vimos que la sucesión $\{a_n\}_{n \geq 1}$ converge para todo $x \in [0,2]$.

$$
\begin{array}{rclr}
    a^2 &=& \displaystyle \lim_{n \to \infty} a^2_n\\
    &=& \displaystyle \lim_{n \to \infty} x + a_{n-1}\\
    &=& \displaystyle x + a\\
    a &=& \displaystyle \frac{1 + \sqrt{1+4x}}{2}\\
\end{array}
$$

Así pues, tenemos que:

$$
f(x) = \lim_{n \to \infty} a_n(x) = \displaystyle \frac{1 + \sqrt{1+4x}}{2}
$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2}\left\{~ 1 + \sqrt{1+4x} ~\right\}_{0}^{2}\\
    &=& \displaystyle \frac{1}{2}\left(~ x + \frac{(1+4x)^{3/2}}{6} ~\right)_{0}^{2}\\
    &=& \displaystyle \frac{19}{6}
\end{array}
$$

## Ejercicio 5

$$ \int \sqrt{x}  e^{\sqrt{x}}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2 \left\{~ t^2 e^t ~\right\} & (1)\\
    &=& \displaystyle 2 \left(~ t^2e^t - 2te^t + 2e^t ~\right) + C & (2)
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^2 \\ dx &=& 2t ~ dt \end{array} \right.$

- (2): $\begin{array}{|c|c|} D & I \\ t^2 & e^t \\ 2 t & e^t \\ 2 & e^t \\ 0 & e^t \end{array}$

## Ejercicio 6

$$ \int \sin(2x) \cos(3x)  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2} \left\{~ \sin(5x) - \sin(x)  ~\right\} & (1),(2)\\
    &=& \displaystyle \frac{1}{2} \left(~ -\frac{\cos(5x)}{5} + \cos(x)  ~\right) + C\\
\end{array}
$$

- (1): $2\sin(a)\cos(b) = \sin(a+b) + \sin(a-b)$

- (2): $\sin(-x) = - \sin(x)$

## Ejercicio 7

$$ \int_0^{2\pi} |1 + 2 \sin x|  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ 1 + 2 \sin x ~\right\}_{0}^{7\pi/6} - \left\{~ 1 + 2 \sin x ~\right\}_{7\pi/6}^{11\pi/6} + \left\{~ 1 + 2 \sin x ~\right\}_{11\pi/6}^{2\pi}& (1)\\
    &=& \displaystyle \left(~ x - 2 \cos x ~\right)_{0}^{7\pi/6} - \left(~ x - 2 \cos x ~\right)_{7\pi/6}^{11\pi/6} + \left(~ x - 2 \cos x ~\right)_{11\pi/6}^{2\pi}\\
    &=& \displaystyle \frac{2\pi}{3} + 4 \sqrt{3}\\
\end{array}
$$

- (1): Si $1 + 2\sin(x) \leq 0$, entonces $\sin(x) \leq -\frac{1}{2}$, dado que $x \in [0,2\pi]$ tenemos que esto ocurre cuando $x \in [\frac{7\pi}{6},\frac{11\pi}{6}]$.

- (2): $\sin(-x) = - \sin(x)$

## Ejercicio 8

$$ \int x (1 - x)^{2014}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ x (1-x)^{\alpha}~\right\}\\
    &=& \displaystyle -\left\{~ (1-u) u^{\alpha}~\right\}& (1)\\
    &=& \displaystyle -\left(~ \frac{u^{\alpha+1}}{\alpha + 1} - \frac{u^{\alpha+2}}{\alpha+2} ~\right) + C \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& 1-x \\ du &=& - dx \end{array} \right.$

## Ejercicio 9

$$ \int \text{arcsinh}(x) dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ t \cosh(t) ~\right\} & (1)\\
    &=& \displaystyle t \sinh(t) - \cosh(t) + C & (2)\\
    &=& \displaystyle x ~\text{arcsinh}(x) - \sqrt{x^2 + 1} + C & (3)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \sinh(t) \\ dx &=& \cosh(t) ~dt \end{array} \right.$

- (2): $\begin{array}{|c|c|} D & I \\ t & \cosh(t) \\ 1 & \sinh(t) \\ 0 & \cosh(t) \end{array}$

- (3): $\cosh^2(t) - \sinh^2(t) = 1$

## Ejercicio 10

$$ \int_{-1}^0 \frac{x^2}{x - 1}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ x + 1 + \frac{1}{x-1}~\right\}_{-1}^{0} \\
    &=& \displaystyle \left( \frac{x^2}{2} + x + \ln|x-1| \right)_{-1}^{0}\\
    &=& \displaystyle \frac{1}{2} - \ln(2)
\end{array}
$$

## Ejercicio 11

$$ \int x \arctan x  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ x + 1 + \frac{1}{x-1}~\right\}_{-1}^{0} \\
    &=& \displaystyle \left( \frac{x^2}{2} + x + \ln|x-1| \right)_{-1}^{0}\\
    &=& \displaystyle \frac{1}{2} - \ln(2)
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ t & \cosh(t) \\ 1 & \sinh(t) \\ 0 & \cosh(t) \end{array}$

## Ejercicio 12

$$ \int \frac{dx}{x^2 - 15x - 2014} $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{91}\left\{~ \frac{1}{x-53} - \frac{1}{x+38}~\right\}\\
    &=& \displaystyle \frac{1}{91}(\ln|x-53| - \ln|x+38|) + C\\
\end{array}
$$

- (1): Utilizar fórmula cuadrática para aplicar fracciones parciales $x_{1,2} = \frac{15 \pm 91}{2}$

## Ejercicio 13

$$ \int e^x \left( \log(1 + x^2) - 2(1 + x) \arctan x \right)  dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle e^x\left( \log(1 + x^2) - 2(1 + x) \arctan x \right) + 2 \left\{~ e^x \left(\arctan(x) + \frac{1}{x^2+1}\right) ~\right\} & (1)\\
    &=& \displaystyle e^x\left( \log(1 + x^2) - 2(1 + x) \arctan x \right) + 2 (e^x\arctan(x)) + C& (2)\\
    &=& \displaystyle e^x\left( \log(1 + x^2) - 2 x \arctan x \right) + C \\
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \log(1 + x^2) - 2(1 + x) \arctan x & e^x \\ -2 (\arctan(x) + \frac{1}{x^2+1}) & e^x \end{array}$

- (2): $[e^x f(x)] = e^x(f(x) + f'(x))$

## Ejercicio 14

$$ \int (\arcsin x)^2  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \theta^2 \cos(\theta) ~\right\} & (1)\\
    &=& \displaystyle \theta^2 \sin(\theta) + 2\theta \cos(\theta) - 2 \sin(\theta) + C & (2)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \sin(\theta) \\ dx &=& \cos(\theta) ~d\theta \end{array} \right.$

- (2): $\begin{array}{|c|c|} D & I \\ \theta^2 & \cos(\theta) \\ 2 \theta & \sin(\theta) \\ 2 & - \cos(\theta) \\ 0 & -\sin(\theta)\end{array}$

## Ejercicio 15

$$ \int \frac{\sqrt{x^2 - 1}}{x}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \tan^2(\theta) ~\right\} & (1)\\
    &=& \displaystyle \left\{~ \sec^2(\theta) - 1 ~\right\} & (2)\\
    &=& \displaystyle \tan(\theta) - \theta + C \\
    &=& \displaystyle \sqrt{x^2-1} - \text{arcsec}(x) + C \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \sec(\theta) \\ dx &=& \sec(\theta)\tan(\theta) ~d\theta \end{array} \right.$, suponiendo que $x \geq 1$

- (2): $\tan^2(\theta) + 1 = \sec^2(\theta)$

## Ejercicio 16

$$ \int x \sec^2 (4x)  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{x}{4} \tan(4x) + \frac{1}{16}\ln|\cos(4x)| + C & (1)\\
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ x & \sec^2(4x) \\ 1 & \frac{\tan(4x)}{4} \\ 0 & -\frac{1}{16}\ln|\cos(4x)| \end{array}$

## Ejercicio 17

$$ \int \frac{2}{6 - 11x + 6x^2 - x^3}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle -\left\{~ \frac{1}{(x-1)(x-2)(x-3)} ~\right\}& (1)\\
    &=& \displaystyle \left\{~ \left( \frac{1}{x-1} - \frac{1}{x-2} \right)\frac{1}{x-3} ~\right\} \\
    &=& \displaystyle \left\{~ \frac{1}{(x-1)(x-3)} - \frac{1}{(x-2)(x-3)} ~\right\} \\
    &=& \displaystyle \left\{~ -\frac{1}{2}\left( \frac{1}{x-1} - \frac{1}{x-3} \right) + \left( \frac{1}{x-2} - \frac{1}{x-3} \right) ~\right\} \\
    &=& \displaystyle \left\{~ -\frac{1}{2} ~ \frac{1}{x-1} + \frac{1}{x-2} -\frac{1}{2} \frac{1}{x-3}  ~\right\} \\
    &=& \displaystyle -\frac{1}{2}\ln|x-1| + \ln|x-2| - \frac{1}{2}\ln|x-3| + C \\
\end{array}
$$

- (1): Teorema de las posibles raices racionales

## Ejercicio 18

$$ \int_0^1 \frac{1}{\lfloor 1 - \log_2 (1 - x) \rfloor}  dx $$

$$\textcolor{red}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \ln(2) \left\{~ \frac{2^t}{\lfloor 1 - t \rfloor} ~\right\}_{-\infty}^{0} & (1)\\
    &=& \displaystyle \ln(2) \sum_{n=0}^{\infty} \left\{~ \frac{2^t}{\lfloor 1 - t \rfloor} ~\right\}_{-(n+1)}^{-n}\\
    &=& \displaystyle \ln(2) \sum_{n=0}^{\infty} \left\{~ \frac{2^t}{1 + \lfloor - t \rfloor} ~\right\}_{-(n+1)}^{-n} & (2)\\
    &=& \displaystyle \ln(2) \sum_{n=0}^{\infty} \left\{~ \frac{2^t}{ n + 1} ~\right\}_{-(n+1)}^{-n} & (3)\\
    &=& \displaystyle \sum_{n=0}^{\infty} \frac{2^{-n} - 2^{-(n+1)}}{n+1} \\
    &=& \displaystyle \sum_{n=0}^{\infty} \frac{2^{-n}}{n+1} - \sum_{n=0}^{\infty} \frac{2^{-(n+1)}}{n+1} \\
    &=& \displaystyle -2\ln(1-1/2) + \ln(1 - 1/2) & (4)\\
    &=& \displaystyle \ln(2)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} 1- x &=& 2^t \\ -dx &=& 2^t \ln(2) ~dt \end{array} \right.$

- (2): Para todo $n \in \mathbb{Z}$ y $x \in \mathbb{R}$ se tiene que $\lfloor n + x \rfloor = n + \lfloor x \rfloor$

- (3): Como $-(n+1) < t < -n$, entonces $n < -t < n+1$ y, por lo tanto, $\lfloor - t \rfloor = n$

- (4): Desarrollo de Taylor:

    $$
    \ln(1+x) = \sum_{n \geq 1} \frac{(-1)^{n+1}}{n} ~~ x^n
    $$

**Nota:**

1. <https://math.stackexchange.com/questions/1846249/evaluate-int-01-frac1-lfloor1-log-21-x-rfloordx?noredirect=1>

## Ejercicio 19

$$ \int_0^{1/\sqrt{3}} \sqrt{x + \sqrt{x^2 + 1}}  dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sqrt{\tan(u) + \sec(u)} ~ \sec^{2}(u) ~\right\}_{0}^{\pi/6} & (1)\\
    &=& \displaystyle \left(\sqrt{ \tan(u) + \sec(u)} \tan(u) \right)_{0}^{\pi/6} - \frac{1}{2}\left\{~ \sqrt{\tan(u) + \sec(u)} ~ \sec(u) \tan(u) ~\right\}_{0}^{\pi/6} & (2)\\
    &=& \displaystyle 3^{-1/4} - \frac{1}{2}\left\{~ \sqrt{\tan(u) + \sec(u)} ~ \sec(u) \tan(u) ~\right\}_{0}^{\pi/6}\\
    &=& \displaystyle 3^{-1/4} - \frac{1}{2} \left( \sqrt{\tan(u) + \sec(u)} \sec(u) \right)_{0}^{\pi/6} + \frac{1}{4} I & (3)\\
    &=& \displaystyle \frac{1}{2} + \frac{1}{4} I\\ \\
    I &=& \displaystyle \frac{2}{3}
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \tan(u)\\ dx &=& \sec^2(u)~dt \end{array} \right.$

- (2): $\begin{array}{|c|c|} D & I \\ \sqrt{\tan(u) + \sec(u)} & \sec^2(u) \\ \frac{1}{2} \sqrt{\tan(u) + \sec(u)}\sec(u) & \tan(u) \end{array}$

- (3): $\begin{array}{|c|c|} D & I \\ \sqrt{\tan(u) + \sec(u)} & \sec(u)\tan(u) \\ \frac{1}{2} \sqrt{\tan(u) + \sec(u)}\sec(u) & \sec(u) \end{array}$

## Ejercicio 20

$$ \int_0^{5\pi/2} \frac{dx}{2 + \cos x} $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle  2 \left\{ \frac{1}{a + \cos x} \right\}_{0}^{\pi} + \left\{ \frac{1}{a + \cos x} \right\}_{2\pi}^{5\pi/2} & \text{ver nota 1}\\ \\
    I_1 &=& \displaystyle  2 \left\{ \frac{1}{a + \cos x} \right\}_{0}^{\pi}\\
    &=& \displaystyle 4 \left\{~ \frac{1}{(a+1) + (a-1)u^2} ~\right\}_{0}^{+\infty} & (1)\\
    &=& \displaystyle \frac{4}{a+1} \left\{~ \frac{1}{1 + \left(u\sqrt{\frac{a-1}{a+1}}\right)^2} ~\right\}_{0}^{+\infty}\\
    &=& \displaystyle \frac{4}{a+1} \left( \sqrt{\frac{a+1}{a-1}}\arctan \left(u \sqrt{\frac{a-1}{a+1}} \right) ~\right)_{0}^{+\infty}\\
    &=& \displaystyle \frac{2}{a+1} \pi\\ \\
    I_2 &=& \displaystyle \left\{ \frac{1}{a + \cos x} \right\}_{2\pi}^{5\pi/2} \\
    &=& \displaystyle \frac{4}{a+1} \left( \sqrt{\frac{a+1}{a-1}}\arctan \left(u \sqrt{\frac{a-1}{a+1}} \right) ~\right)_{0}^{1}\\
    &=& \displaystyle \frac{2}{a+1} \left( \sqrt{\frac{a+1}{a-1}}\arctan \left(\sqrt{\frac{a-1}{a+1}} \right) ~\right)\\ \\
    I &=& \displaystyle \frac{2}{a+1} \pi + \frac{2}{a+1} \left( \sqrt{\frac{a+1}{a-1}}\arctan \left(\sqrt{\frac{a-1}{a+1}} \right) \right)
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& \tan(x/2)\\ du &=& \frac{\sec^2(x/2)}{2}~dx \end{array} \right.$

- (2): $\begin{array}{|c|c|} D & I \\ \sqrt{\tan(u) + \sec(u)} & \sec^2(u) \\ \frac{1}{2} \sqrt{\tan(u) + \sec(u)}\sec(u) & \tan(u) \end{array}$

**Nota:**

1. Tener presente que las sustituciones tienen que ser biyectivas y diferenciables en el intervalo de integración.
