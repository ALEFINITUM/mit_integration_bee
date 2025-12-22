# MIT integration bee - 2019

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

$$ \int_{0}^{2\pi} \tan(\cos(x)) \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \tan(\cos(x)) ~\right\}_{0}^{\pi} + \left\{~ \tan(\cos(x)) ~\right\}_{\pi}^{2\pi}\\
    &=& \displaystyle \left\{~ \tan(\cos(x)) ~\right\}_{0}^{\pi} + \left\{~ \tan(-\cos(x)) ~\right\}_{0}^{\pi} & (1)\\
    &=& \displaystyle \left\{~ \tan(\cos(x)) ~\right\}_{0}^{\pi} - \left\{~ \tan(\cos(x)) ~\right\}_{0}^{\pi} & (2)\\
    &=& \displaystyle 0\\
\end{array}
$$

- (1): $\cos(x + \pi) = \cos(x)\cos(\pi) - \sin(x) \sin(\pi) = - \cos(x)$

- (2): $\tan(x)$ es una función impar

## Ejercicio 2

$$ \int \frac{x+1}{x(x+\log x)} \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1+1/x}{x+\ln x} ~\right\}\\
    &=& \displaystyle \ln|x + \ln(x)| + C & (1)\\
\end{array}
$$

- (1): $[\ln(f(x))] = \frac{f'(x)}{f(x)}$

## Ejercicio 3

$$ \int e^{x+e^x} + e^{x-e^x} \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ e^{u} + e^{-u} ~\right\} & (1)\\
    &=& \displaystyle 2 \left\{~ \cosh(u) ~\right\} & (2)\\
    &=& \displaystyle 2 \sinh(u) + C & (3)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& e^x \\ du &=& e^x ~dx \end{array} \right.$

- (2): $\cosh(x) = \frac{e^{x} + e^{-x}}{2}$

- (3): $[\sinh(x)] = \cosh(x)$ y $[\cosh(x)] = \sinh(x)$

## Ejercicio 4

$$ \int_{-1/2}^{1/2} \frac{dx}{1-x^2} $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2}\left\{~ \frac{1}{1-x} + \frac{1}{1+x}  ~\right\}_{-1/2}^{1/2}\\
    &=& \displaystyle \frac{1}{2}\left(~ -\ln|1-x| + \ln|1+x|  ~\right)_{-1/2}^{1/2}\\
    &=& \displaystyle \ln(3)\\
\end{array}
$$

## Ejercicio 5

$$ \int_{0}^{2} 2^{\log x} \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ 2^{\frac{\log_2(x)}{\log_2(e)}} ~\right\}_{0}^{2} & (1)\\
    &=& \displaystyle \left\{~ 2^{\frac{\log_2(x)}{\log_2(e)}} ~\right\}_{0}^{2}\\
    &=& \displaystyle \left\{~ x^{\frac{1}{\log_2(e)}} ~\right\}_{0}^{2}\\
    &=& \displaystyle \left\{~ x^{\ln(2)} ~\right\}_{0}^{2} & (1)\\
    &=& \displaystyle \left(~ \frac{x^{\ln(2)+1}}{\ln(2)+1} ~\right)_{0}^{2}\\
    &=& \displaystyle \frac{2^{\ln(2)+1}}{\ln(2)+1}\\
\end{array}
$$

- (1): $\log_a(x) = \frac{\log_b(x)}{\log_b(a)}$

## Ejercicio 6

$$ \int_{-2\pi}^{2\pi} (\cos 3x + \sin 2x)(-\sin 2019x + \cos 3x) \, dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ -\cos(3x)\sin(2019x) + \cos^2(3x) -\sin(2x)\sin(2019x) + \sin(2x)\cos(3x) ~\right\}_{-2\pi}^{2\pi}\\
    &=& \displaystyle -\left\{~ \cos(3x)\sin(2019x) ~\right\}_{-2\pi}^{2\pi} + \left\{~ \sin(2x)\cos(3x) ~\right\}_{-2\pi}^{2\pi} + \left\{~ \cos^2(3x) -\sin(2x)\sin(2019x) ~\right\}_{-2\pi}^{2\pi}\\
    &=& \displaystyle \left\{~ \cos^2(3x) -\sin(2x)\sin(2019x) ~\right\}_{-2\pi}^{2\pi} & (1)\\
    &=& \displaystyle 2 \left\{~ \cos^2(3x) -\sin(2x)\sin(2019x) ~\right\}_{0}^{2\pi} & (2)\\ \\
    I_1 &=& \displaystyle \left\{~ \cos^2(3x) ~\right\}_{0}^{2\pi}\\
    &=& \displaystyle \frac{1}{2}\left\{~ \cos(6x) + 1 ~\right\}_{0}^{2\pi} & (3)\\
    &=& \displaystyle \frac{1}{2}\left(~ \frac{\sin(6x)}{6} + x ~\right)_{0}^{2\pi}\\
    &=& \displaystyle \pi\\ \\
    I_2 &=& \displaystyle \left\{~ \sin(2x)\sin(2019x) ~\right\}_{0}^{2\pi}\\
    &=& \displaystyle \left\{~ \sin(2x)\sin(2019x) ~\right\}_{0}^{2\pi}\\
    &=& \displaystyle \frac{1}{2} \left\{~ \cos(2017) - \cos(2021) ~\right\}_{0}^{2\pi} & (4)\\
    &=& \displaystyle \frac{1}{2} \left(~ \frac{\sin(2017x)}{2017} - \frac{\sin(2021x)}{2021} ~\right)_{0}^{2\pi}\\
    &=& \displaystyle 0\\ \\
    I &=& 2 \pi
\end{array}
$$

- (1): Funciones impares en intervalos simétricos

- (2): Funciones pares en intervalos simétricos

- (3): $\cos(2x) = 2 \cos^2(x) - 1$

- (4): $\cos(a-b) -\cos(a+b) = 2 \sin(a)\sin(b)$

## Ejercicio 7

$$ \int \cos (x) \cdot \cos (\sin x) \cdot \cos (\sin (\sin x)) \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \cos (u)\cos (\sin (u)) ~\right\} & (1)\\
    &=& \displaystyle \left\{~ \cos (t) ~\right\} & (2)\\
    &=& \displaystyle \sin (t) + C \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& \sin(x) \\ du &=& \cos(x) ~dx \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} t &=& \sin(u) \\ dt &=& \cos(u) ~du \end{array} \right.$

## Ejercicio 8

$$ \int_{0}^{\infty} \frac{e^{-\frac{2019}{4t^2}}}{t^2} \, dt $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{e^{-\frac{\alpha}{t^2}}}{t^2} ~\right\}_{0}^{\infty}\\
    &=& \displaystyle \left\{~ e^{-\alpha x^2} ~\right\}_{0}^{\infty} & (1)\\
    &=& \displaystyle \left\{~ e^{-(\sqrt{\alpha} x)^2} ~\right\}_{0}^{\infty}\\
    &=& \displaystyle \frac{1}{\sqrt{\alpha}} \left\{~ e^{-u^2} ~\right\}_{0}^{\infty} & (2)\\
    &=& \displaystyle \frac{1}{2} \sqrt{\frac{\pi}{\alpha}} & (3)\\
    &=& \displaystyle \sqrt{\frac{\pi}{2019}}\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \frac{1}{t} \\ dx &=& -\frac{1}{t^2} ~dt \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} u &=& \sqrt{\alpha}x \\ du &=& \sqrt{\alpha} ~dx \end{array} \right.$

- (3): Integral Gaussiana $\{e^{-x^2}\}_{-\infty}^{\infty} = \sqrt{\pi}$

## Ejercicio 9

$$ \int \sin(\sqrt{x}) \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2 \left\{~ t\sin(t) ~\right\} & (1)\\
    &=& \displaystyle 2 \left(~ -t\cos(t) + \sin(t) ~\right) + C & (2)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^2 \\ dx &=& 2t ~dt \end{array} \right.$

- (2): $\begin{array}{|c|c|} D & I \\ t & \sin(t) \\ 1 & -\cos(t) \\ 0 & -\sin(t) \end{array}$

## Ejercicio 10

$$ \int_{0}^{1} \frac{\sqrt{x}}{1+x} \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2 \left\{~ \frac{t^2}{1+t^2} ~\right\}_{0}^{1} & (1)\\
    &=& \displaystyle 2 \left\{~ 1 - \frac{1}{1+t^2} ~\right\}_{0}^{1}\\
    &=& \displaystyle 2 \left(~ t - \arctan(t) ~\right)_{0}^{1}\\
    &=& \displaystyle 2 \left(~ 1 - \pi/4~\right)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^2 \\ dx &=& 2t ~dt \end{array} \right.$

## Ejercicio 11

$$ \int_{0}^{2\pi} \cos(x) \cos(2x) \cos(3x) \, dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2} \left\{~ \cos(x) ( \cos(5x) + \cos(x))~\right\}_{0}^{2\pi} & (1)\\
    &=& \displaystyle \frac{1}{2} \left\{~ \cos(x)\cos(5x) + \cos^2(x) ~\right\}_{0}^{2\pi}\\
    &=& \displaystyle \frac{1}{2} \left\{~ \frac{\cos(6x) + \cos(4x)}{2} + \cos^2(x) ~\right\}_{0}^{2\pi} & (1)\\
    &=& \displaystyle \frac{1}{4} \left\{~ \cos(6x) + \cos(4x) ~\right\}_{0}^{2\pi} + \frac{1}{2}\left\{~ \cos^2(x) ~\right\}_{0}^{2\pi} \\
    &=& \displaystyle \frac{1}{2}\left\{~ \cos^2(x) ~\right\}_{0}^{2\pi} & (2)\\
    &=& \displaystyle \frac{1}{4}\left\{~ \cos(2x) + 1 ~\right\}_{0}^{2\pi} & (3)\\
    &=& \displaystyle \frac{1}{4}\left\{~ \cos(2x) ~\right\}_{0}^{2\pi} + \frac{1}{4}\left\{~ 1 ~\right\}_{0}^{2\pi}\\
    &=& \displaystyle \frac{1}{4}\left\{~ 1 ~\right\}_{0}^{2\pi} & (2)\\
    &=& \displaystyle \frac{\pi}{2}\\
\end{array}
$$

- (1): $\cos(a+b) + \cos(a-b) = 2\cos(a)\cos(b)$

- (2): $\cos(x + \pi) = -\cos(x)$

- (3): $\cos(2x) = 2 \cos^2(x) -1$

## Ejercicio 12

$$ \lim_{n \to \infty} \int_{-\infty}^{\infty} e^{-x^{2n}} \, dx $$

$$\textcolor{red}{---\text{ Demostración } ---}$$

Considere la siguiente sucesion de funciones $f_n(x) = e^{-x^{2n}}$ donde $x \in \mathbb{R}$.

Necesitamos que la sucesión $\{f_n(x)\}_{n \geq 1}$ converga uniformemente a una función $f(x)$ para todo $x \in \mathbb{R}$, para poder aplicar el siguiente teorema: <https://en.wikipedia.org/wiki/Uniform_convergence> (nos permite conmutar la integral por el límite).

Suponiendo que tenemos esta convergencia uniforme, entonces:

$$
\begin{array}{rclr}
    \displaystyle \lim_{n \to \infty} I_n &=& \displaystyle \lim_{n \to \infty} \left\{~ f_{n}(x) ~\right\}_{-\infty}^{\infty}\\
    &=& \displaystyle \lim_{n \to \infty}  2 \left\{~ f_{n}(x) ~\right\}_{0}^{\infty} & (1)\\
    &=& \displaystyle 2 \lim_{n \to \infty} (~~ \left\{~ f_{n}(x) ~\right\}_{0}^{1} + \left\{~ f_{n}(x) ~\right\}_{1}^{\infty} ~~) \\
    &=& \displaystyle 2 (~ \left\{~ \lim_{n \to \infty} f_{n}(x) ~\right\}_{0}^{1} + \left\{~ \lim_{n \to \infty}f_{n}(x) ~\right\}_{1}^{\infty} ~) \\
    &=& \displaystyle 2 (~ \left\{~ 1 ~\right\}_{0}^{1} + \left\{~ \lim_{n \to \infty}f_{n}(x) ~\right\}_{1}^{\infty} ~) & (2)\\
    &=& \displaystyle 2 (~ \left\{~ 1 ~\right\}_{0}^{1} + \left\{~ 0 ~\right\}_{1}^{\infty} ~) & (3)\\
    &=& \displaystyle 2 \\
\end{array}
$$

- (1): Función par en intervalo simétrico

- (2): Si $x \in (0,1)$, entonces $x^n < x < 1$ y por lo tanto $\lim_{n \to \infty} f_n(x) = \lim_{n \to \infty} e^{-x^{2n}} = e^{0} = 1$

- (3): Si $x \in (1, \infty)$, entonces $1 < x < x^n$ y por lo tanto $\lim_{n \to \infty} f_n(x) = \lim_{n \to \infty} e^{-x^{2n}} = 0$

**Nota:**

1. Convergencia uniforme:

    - <https://en.wikipedia.org/wiki/Uniform_convergence>
    - <https://alephsub0.org/material-nuevo/jonathan-ortiz/intercambiar-la-integral-y-el-limite/>
    - (video que demuestra el teorema para convergencia uniforme) <https://www.youtube.com/watch?v=SPq6-kEs9CU>

## Ejercicio 13

$$ \int_{0}^{e} x^{\frac{1}{\log x}} \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ e ~\right\}_{0}^{e} & (1)\\
    &=& \displaystyle e (x)_{0}^{e}\\
    &=& \displaystyle e^2\\
\end{array}
$$

- (1): $x^{\frac{1}{\ln(x)}} = e^{\ln(x^{\frac{1}{\ln(x)}})} = e$

## Ejercicio 14

$$ \int_{0}^{\pi/100} \frac{\sin(20x) + \sin(19x)}{\cos(20x) + \cos(19x)} \, dx $$

$$\textcolor{red}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{2 \sin \left(~ \frac{39}{2} x ~\right) \cos \left(~ \frac{x}{2} ~\right)}{\cos(20x) + \cos(19x)}~\right\}_{0}^{\pi/100} & (1)\\
    &=& \displaystyle \left\{~ \frac{2 \sin \left(~ \frac{39}{2} x ~\right) \cos \left(~ \frac{x}{2} ~\right)}{2 \cos \left(~ \frac{39}{2}x ~\right) \cos \left(~ \frac{x}{2} ~\right)} ~\right\}_{0}^{\pi/100}  & (2)\\
    &=& \displaystyle \left\{~ \tan \left(\frac{39}{2}x \right) ~\right\}_{0}^{\pi/100}\\
    &=& \displaystyle -\frac{2}{39}  \left( \ln \left|\cos \left( \frac{39}{2}x \right)  \right| \right)_{0}^{\pi/100}\\
    &=& \displaystyle -\frac{2}{39} \ln \left|\cos \left( \frac{39\pi}{200} \right)  \right|
\end{array}
$$

- (1): Considere el siguinete desarrollo:

    $$
    \begin{array}{rclr}
        \displaystyle 2 \sin \left(~ \frac{a+b}{2} ~\right) \cos \left(~ \frac{a-b}{2} ~\right) &=& \displaystyle 2 \left(~ \sin(a/2) \cos(b/2) + \cos(a/2) \sin(b/2) ~\right) \left(~ \cos(a/2) \cos(b/2) + \sin(a/2) \sin(b/2) ~\right)\\
        &=& \displaystyle 2 \left(~ \sin(a/2) \cos(b/2) + \cos(a/2) \sin(b/2) ~\right) \left(~ \cos(a/2) \cos(b/2) + \sin(a/2) \sin(b/2) ~\right)\\
        &=& \displaystyle 2 \left(~ \sin(a/2)\cos(a/2) + \sin(b/2)\cos(b/2) ~\right)\\
        &=& \displaystyle  \sin(a) + \sin(b) \\
    \end{array}
    $$

- (2): Considere el siguiente desarrollo:

    $$
    \begin{array}{rclr}
        \displaystyle 2 \cos \left(~ \frac{a+b}{2} ~\right) \cos \left(~ \frac{a-b}{2} ~\right) &=& \displaystyle 2 \left(~ \cos(a/2) \cos(b/2) - \sin(a/2) \sin(b/2) ~\right) \left(~ \cos(a/2) \cos(b/2) + \sin(a/2) \sin(b/2) ~\right)\\
        &=& \displaystyle 2 \left(~ \cos^2(a/2) \cos^2(b/2) - \sin^2(a/2) \sin^2(b/2) ~\right)\\
        &=& \displaystyle 2 \left(~ \cos^2(a/2) \cos^2(b/2) -(1 - \cos^2(a/2))(1 - \cos^2(b/2)) ~\right)\\
        &=& \displaystyle 2 \left(~ \cos^2(a/2) + \cos^2(b/2)) - 1 ~\right)\\
        &=& \displaystyle \cos(a) + \cos(b)\\
    \end{array}
    $$

## Ejercicio 15

$$ \int (e^x \cos^2(x) + e^x \cos(x) \sin(x) - e^x \sin^2(x)) \, dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ e^x(~ \cos^2(x) + \cos(x) \sin(x) - \sin^2(x) ~) ~\right\}\\
    &=& \displaystyle \left\{~ e^x(~ \cos(2x) + \cos(x) \sin(x) ~) ~\right\} & (1)\\
    &=& \displaystyle \left\{~ e^x \left(~ \cos(2x) + \frac{\sin(2x)}{2} ~\right) ~\right\} & (2)\\
    &=& \displaystyle \frac{\sin(2x)}{2}e^x + C & (3)\\
\end{array}
$$

- (1): $\cos(2x) = \cos^2(x) - \sin^2(x)$

- (2): $\sin(2x) = 2 \sin(x)\cos(x)$

- (3): $[e^xf(x)] = e^x(f(x) + f'(x))$

## Ejercicio 16

$$ \int_{0}^{\pi/2} \frac{\sin x}{\sin(x + \pi/4)} \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \sqrt{2} \left\{~ \frac{\sin(x)}{\sin(x) + \cos(x)}~\right\}_{0}^{\pi/2} & (1)\\
    &=& \displaystyle \sqrt{2} \left\{~ \frac{\cos(\theta)}{\sin(x) + \cos(x)} ~\right\}_{0}^{\pi/2} & (2)\\ \\
    2I &=& \displaystyle \sqrt{2} \left\{~ \frac{\sin(\theta)}{\sin(x) + \cos(x)} + \frac{\cos(\theta)}{\sin(x) + \cos(x)}~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle \sqrt{2} \left\{~ 1 ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle \frac{\pi}{\sqrt{2}}\\ \\
    I &=& \displaystyle \frac{\pi}{2\sqrt{2}}
\end{array}
$$

- (1): $\sin(x + \pi/4) = \frac{1}{\sqrt{2}}(\sin(x) + \cos(x))$

- (2): $\left\{\begin{array}{rcl} x &=& \pi/2 - \theta \\ dx &=& - d\theta \end{array} \right.$


## Ejercicio 17

$$ \int \frac{dx}{x + \sqrt[3]{x}} $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 3 \left\{~ \frac{t}{t^2 + 1} ~\right\} & (1)\\
    &=& \displaystyle \frac{3}{2} \ln |t^2+1| + C & (2)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^3 \\ dx &=& 3t^2 dt \end{array} \right.$

- (2): $[\ln(f(x))]= \frac{f'(x)}{f(x)}$

## Ejercicio 18

$$ \int_{0}^{2} x^{x^2+1}(2\log(x) + 1) \, dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ x^{x^2}(2x\ln(x) + x) ~\right\}_{0}^{2}\\
    &=& \displaystyle \left( x^{x^2} \right)_{0}^{2} & (1) \\
    &=& \displaystyle 2^{2^2} - 1  & (2) \\
    &=& \displaystyle 15 & (2) \\
\end{array}
$$

- (1): $[x^{x^2}]= [e^{x^2\ln(x)}]= e^{x^2\ln(x)}(2x\ln(x) + x) = x^{x^2}(2x\ln(x) + x)$

- (2): $\lim_{x \to 0} x^{x^{2}} = \lim_{x \to 0} e^{x^2\ln(x)} = e^{\lim_{x \to 0} x^2\ln(x)} = e^{0} = 0$ (aplicando L'hopital)

## Ejercicio 19

$$ \int \frac{2x^3 - 1}{x(x^3 + 1)} \, dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{2(x^3+1) - 3}{x(x^3 + 1)} ~\right\} \\
    &=& \displaystyle \left\{~ \frac{2}{x} - \frac{3}{x(x^3 + 1)} ~\right\} \\
    &=& \displaystyle 2 \ln|x| - 3 \left\{~ \frac{1}{x(x^3 + 1)} ~\right\} \\
    &=& \displaystyle 2 \ln|x| - 3 \left\{~ \frac{1}{x(x^3 + 1)} ~\right\} \\ \\
    I_1 &=& \displaystyle \left\{~ \frac{1}{x(x^3 + 1)} ~\right\}\\
    &=& \displaystyle -\left\{~ \frac{u^2}{u^3 + 1} ~\right\} & (1)\\
    &=& \displaystyle - \frac{1}{3} \left\{~ \frac{3u^2}{u^3 + 1} ~\right\} \\
    &=& \displaystyle - \frac{1}{3} \ln|u^3 + 1| +  C & (2)\\
    &=& \displaystyle - \frac{1}{3} \ln \left| \left(\frac{1}{x} \right)^3 + 1 \right| +  C \\ \\
    I &=&  \displaystyle 2 \ln|x| + \ln \left| \left(\frac{1}{x} \right)^3 + 1 \right| +  C \\
    &=&  \displaystyle \ln \left| x^3 + 1 \right| - \ln|x| +  C \\
\end{array}
$$

- (1): $\left\{ \begin{array}{rcl} x &=& \frac{1}{u} \\ dx &=& - \frac{1}{u^2} ~ du \end{array} \right.$

- (2): $[\ln(f(x))] = \frac{f'(x)}{f(x)}$

## Ejercicio 20

$$ \int \cos(\arctan(x)) \, dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \cos(u) \sec^2(u) ~\right\} & (1),(2) \\
    &=& \displaystyle \left\{~ \sec(u) ~\right\} \\
    &=& \displaystyle \ln|\sec(u) + \tan(u)| + C & (3),(4)\\
    &=& \displaystyle \ln|\sqrt{x^2+1} + x| + C \\
\end{array}
$$

- (1): $\left\{ \begin{array}{rcl} u &=& \arctan(x) \\ du &=& \frac{1}{1+x^2} ~ dx \end{array} \right.$

- (2): $1 + \tan^2(x) = \sec^2(x)$

- (3): $\sec(x) = \frac{\sec(x)(\sec(x) + \tan(x))}{\sec(x) + \tan(x)}$

- (4): $[\sec(x) + \tan(x)] = \sec(x)(\sec(x) + \tan(x))$
