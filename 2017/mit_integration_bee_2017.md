# MIT integration bee - 2017

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

$$ \int \frac{x^2}{\sqrt{x^3 + 2}}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{3} \left\{~ \frac{1}{u^{1/2}} ~\right\} & (1)\\
    &=& \displaystyle \frac{2}{3} \sqrt{u} + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& x^3 + 2 \\ du &=& 3x^2 ~dx \end{array} \right.$

## Ejercicio 2

$$ \int_1^\infty \frac{\log x}{x^2}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle - \left(~ \frac{\ln(x)}{x} ~\right)_{1}^{\infty} + \left\{~ \frac{1}{x^2} ~\right\}_{1}^{\infty} & (1)\\
    &=& \displaystyle - \left(~ \frac{\ln(x)}{x} ~\right)_{1}^{\infty} - \left(~ \frac{1}{x} ~\right)_{1}^{\infty}\\
    &=& \displaystyle 1
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \ln(x) & \frac{1}{x^2} \\ \frac{1}{x} & \frac{-1}{x}\end{array}$

## Ejercicio 3

$$ \int \text{sech}(x)  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{2e^x}{e^{2x} + 1} ~\right\}\\
    &=& \displaystyle 2\left\{~ \frac{1}{u^2 + 1} ~\right\} & (1)\\
    &=& \displaystyle 2\arctan(u) + C \\
    &=& \displaystyle 2\arctan(e^x) + C \\
    &=& \displaystyle \arctan(-\text{csch}(x)) + C \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& e^x \\ du &=& e^x ~dx \end{array} \right.$

- (2): Sea $y = 2 \arctan(e^x)$, entonces $\left\{\begin{array}{rcl} \sin(y/2) &=& \text{sech}(x) \\ \cos(y/2) &=& - \tanh(x)\end{array} \right.$, por lo tanto $\tan(y) = -\text{csch}(x)$

**Nota:**

1. Propiedades básicas de las funciones trigonometricas hiperbólicas:

    $$
    \left \{
    \begin{array}{ccc}
        \cosh^2(x) - \sinh^2(x) &=& 1 \\
        2\sinh^2(x) &=& \cosh(2x)-1 \\
        2\cosh^2(x) &=& \cosh(2x)+1 \\
        \sinh^2(x) + \cosh^2(x) &=& \cosh(2x) \\
        2\sinh(x) \cosh(x) &=& \sinh(2x)\\
        (\sinh(x) + \cosh(x))^2 &=&  \cosh(2x) + \sinh(2x)\\
    \end{array}
    \right.
    $$

2. Derivadas de las funciones trigonométricas hiperbólicas:

    $$
    \left \{
    \begin{array}{ccc}
        [\sinh(x)] &=& \cosh(x)\\
        [\cosh(x)] &=& \sinh(x)\\
        [\tanh(x)] &=& \text{sech}^2(x)\\
        [\coth(x)] &=& -\text{csch}^2(x)\\
        [\text{sech}(x)] &=& -\text{sech}(x)\text{tanh}(x)\\
        [\text{csch}(x)] &=& -\text{csch}(x)\text{coth}(x)\\
    \end{array}
    \right.
    $$

## Ejercicio 4

$$ \int x^3 e^{x^2}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ x x^2 e^{x^2} ~\right\}\\
    &=& \displaystyle \frac{1}{2} \left\{~ u e^{u} ~\right\} & (1)\\
    &=& \displaystyle \frac{1}{2} \left(~ u e^{u} - e^u ~\right) + C & (2)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& x^2 \\ du &=& 2x ~dx \end{array} \right.$

- (2): $\begin{array}{|c|c|} D & I \\ u & e^u \\ 1 & e^u \\ 0 & e^u \end{array}$

## Ejercicio 5

$$ \int_1^2 \frac{1}{x\sqrt{x^2 - 1}}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left(~ \text{arcsec}(x) ~\right)_{1}^{2} & (1)\\
    &=& \displaystyle \frac{\pi}{3}\\
\end{array}
$$

- (1): $[ \text{arcsec}(x)] = \frac{1}{|x| \sqrt{x^2-1}}$

## Ejercicio 6

$$ \int_1^\infty \frac{dx}{x(x^2 + 1)} $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{x}{x^2+1} ~\right\}_{0}^{1} & (1)\\
    &=& \displaystyle \frac{1}{2} \left(~ \ln|x^2+1| ~\right)_{0}^{1} & (2)\\
    &=& \displaystyle \frac{\ln(2)}{2} \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \frac{1}{t} \\ dx &=& -\frac{1}{t^2} ~dt \end{array} \right.$

- (2): $[\ln(f(x))] = \frac{f'(x)}{f(x)}$

## Ejercicio 7

$$ \int \text{arccosh}(x)  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ u \sinh(u) ~\right\} & (1)\\
    &=& \displaystyle u \cosh(u) - \sinh(u) + C & (2)\\
    &=& \displaystyle x ~ \text{arccosh}(x) - \sqrt{x^2 - 1} + C & (3)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \cosh(u) \\ dx &=& \sinh(u) ~du \end{array} \right.$

- (2): $\begin{array}{|c|c|} D & I \\ u & \sinh(u) \\ 1 & \cosh(u) \\ 0 & \sinh(u) \end{array}$

- (3): $\cosh^2(x) - \sinh^2(x) = 1$

## Ejercicio 8

$$ \int_{-\infty}^\infty e^{-2x^2 - 5x - 3}  dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~  e^{-\left(~ (\sqrt{2}x + \frac{5}{2 \sqrt{2}})^2 - \frac{1}{8}~\right)} ~\right\}_{-\infty}^{+\infty}\\
    &=& \displaystyle e^{\frac{1}{8}} \left\{~  e^{-(\sqrt{2}x + \frac{5}{2 \sqrt{2}})^2}  ~\right\} _{-\infty}^{+\infty}\\
    &=& \displaystyle e^{\frac{1}{8}} \sqrt{\pi/2} & (1)\\
\end{array}
$$

- (1): Integral Gaussiana $\{e^{-x^2}\}_{-\infty}^{+\infty} = \sqrt{\pi}$

## Ejercicio 9

$$ \int \sin \sqrt{x}  dx $$

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

$$ \int_0^\infty \frac{dx}{(x + 1/x)^2} $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{x^2}{(x^2 + 1)^2} ~\right\}_{0}^{\infty}\\
    &=& \displaystyle \left\{~ \frac{1}{x^2} ~ \frac{1}{(1+1/x^2)^2} ~\right\}_{0}^{\infty}\\
    &=& \displaystyle \left\{~ \frac{1}{(1+u^2)^2} ~\right\}_{0}^{\infty} & (1)\\ \\
    2 I &=& \displaystyle \left\{~ \frac{1 + x^2}{(1+x^2)^2} ~\right\}_{0}^{\infty}\\
    &=& \displaystyle \left\{~ \frac{1}{1+x^2} ~\right\}_{0}^{\infty}\\
    &=& \displaystyle \left(~ \arctan(x) ~\right)_{0}^{\infty}\\
    &=& \displaystyle \pi/2\\ \\
    I &=& \displaystyle \frac{\pi}{4}
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& \frac{1}{x} \\ du &=& -\frac{1}{x^2} ~dx \end{array} \right.$

## Ejercicio 11

$$ \int \frac{(2+x)e^{-x}}{x^3}  dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \left(\frac{2}{x^3} + \frac{1}{x^2} \right) e^{-x} ~\right\}\\
    &=& \displaystyle \left\{~ \frac{2}{x^3}e^{-x} + \frac{1}{x^2} e^{-x} ~\right\}\\
    &=& \displaystyle I_1 + \left\{~ \frac{1}{x^2} e^{-x} ~\right\} & (1)\\
    &=& \displaystyle I_1 + - \frac{e^{-x}}{x^2} - I_1 & (2)\\
    &=& \displaystyle - \frac{e^{-x}}{x^2} + C\\
\end{array}
$$

- (1): $I_1 = \left\{~ \frac{2}{x^3}e^{-x} ~\right\}$

- (2): $\begin{array}{|c|c|} D & I \\ \frac{1}{x^2} & e^{-x} \\ \frac{-2}{x^3} & -e^{-x} \end{array}$

## Ejercicio 12

$$ \int_0^1 \frac{dx}{\sqrt{x(1-x)}} $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2\left\{~ \frac{1}{\sqrt{1-t^2}} ~\right\}_{0}^{1} & (1)\\
    &=& \displaystyle 2 \left(~ \arcsin(t) ~\right)_{0}^{1} & (2)\\
    &=& \displaystyle \pi\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^2 \\ dx &=& 2t~dt \end{array} \right.$

- (2): $[\arcsin(x)] = \frac{1}{\sqrt{1-x^2}}$

## Ejercicio 13

$$ \int_0^\infty \frac{\tanh(x)}{\exp(x)}  dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \tanh(x)(\cosh(x) - \sinh(x)) ~\right\} & (1)\\
    &=& \displaystyle \left\{~ \sinh(x) - \frac{\sinh^2(x)}{\cosh(x)} ~\right\} \\
    &=& \displaystyle \cosh(x) - \left\{~ \frac{\sinh^2(x)}{\cosh(x)} ~\right\} \\
    &=& \displaystyle \cosh(x) - \left\{~ \cosh(x) - \text{sech}(x) ~\right\} \\
    &=& \displaystyle \cosh(x) - \sinh(x)  + \left\{~ \text{sech}(x) ~\right\}\\
    &=& \displaystyle \cosh(x) - \sinh(x)  + \arctan(-\text{csch}(x)) + C & (3)\\
    &=& \displaystyle e^{-x}  + \arctan(-\text{csch}(x)) + C & (1)\\ \\
    I &=& \left( e^{-x}  + \arctan(-\text{csch}(x)) \right)_{0}^{\infty}\\
    &=& \pi/2 -1
\end{array}
$$

- (1): $\cos(x) - \sinh(x) = e^{-x}$

- (2): $\cosh^2(x) - \sinh^2(x) = 1$

- (3): Ver ejercicio 3

**Nota:**

1. Propiedades básicas de las funciones trigonometricas hiperbólicas:

    $$
    \left \{
    \begin{array}{ccc}
        \cosh^2(x) - \sinh^2(x) &=& 1 \\
        2\sinh^2(x) &=& \cosh(2x)-1 \\
        2\cosh^2(x) &=& \cosh(2x)+1 \\
        \sinh^2(x) + \cosh^2(x) &=& \cosh(2x) \\
        2\sinh(x) \cosh(x) &=& \sinh(2x)\\
        (\sinh(x) + \cosh(x))^2 &=&  \cosh(2x) + \sinh(2x)\\
    \end{array}
    \right.
    $$

2. Derivadas de las funciones trigonométricas hiperbólicas:

    $$
    \left \{
    \begin{array}{ccc}
        [\sinh(x)] &=& \cosh(x)\\
        [\cosh(x)] &=& \sinh(x)\\
        [\tanh(x)] &=& \text{sech}^2(x)\\
        [\coth(x)] &=& -\text{csch}^2(x)\\
        [\text{sech}(x)] &=& -\text{sech}(x)\text{tanh}(x)\\
        [\text{csch}(x)] &=& -\text{csch}(x)\text{coth}(x)\\
    \end{array}
    \right.
    $$

## Ejercicio 14

$$ \int_0^{\frac{\pi}{2}} \sqrt{\sin(x)+1}  dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sqrt{\cos(\theta) + 1} ~\right\}_{0}^{\pi/2} & (1),(2)\\
    &=& \displaystyle 2 \left\{~ \sqrt{\cos(2t) + 1} ~\right\}_{0}^{\pi/4} & (3)\\
    &=& \displaystyle 2 \left\{~ \sqrt{2\cos^2(t)} ~\right\}_{0}^{\pi/4} & (4)\\
    &=& \displaystyle 2^{3/2} \left\{~ \cos(t) ~\right\}_{0}^{\pi/4}\\
    &=& \displaystyle 2^{3/2} \left(~ \sin(t) ~\right)_{0}^{\pi/4}\\
    &=& \displaystyle 2
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \pi/2 - \theta \\ dx &=& -d\theta \end{array} \right.$

- (2): $\sin(\pi/2 -x) = \cos(x)$

- (3): $\left\{\begin{array}{rcl} \theta &=& 2 t \\ d\theta &=& 2 dt \end{array} \right.$

- (4): $\cos(2x) = 2\cos^2(x) - 1$

## Ejercicio 15

$$ \lim_{n\to\infty} I_n, \text{ donde } I_1 = \int_0^1 \frac{dx}{1+\sqrt{x}}, \quad I_2 = \int_0^1 \frac{dx}{1+\frac{1}{1+\sqrt{x}}}, \quad I_3 = \int_0^1 \frac{dx}{1+\frac{1}{1+\frac{1}{1+\sqrt{x}}}}, \quad \cdots $$

$$\textcolor{red}{---\text{ Demostración } ---}$$

Considere la siguiente sucesión de funciones:  

$$a_1(x) = \frac{1}{1+\sqrt{x}} \quad a_{n+1}(x) =\frac{1}{1+a_n}$$

Así pues, nuestro objetivo es determinar la convergencia de la siguiente sucesión:

$$
I_n = \{a_n\}_{0}^{1}
$$

Necesitamos que la sucesión $\{a_n(x)\}_{n \geq 1}$ converga uniformemente a una función $f(x)$ para todo $x \in (0,1)$, para poder aplicar el siguiente teorema: <https://en.wikipedia.org/wiki/Uniform_convergence> (nos permite conmutar la integral por el límite).

Suponiendo esto (todavia no tengo la teoría suficiente para afrontar el problema formalmente), tenemos el siguiente desarrollo:

$$
\begin{array}{rclr}
    a &=& \displaystyle \lim_{n \to \infty} a_n\\
    &=& \displaystyle \lim_{n \to \infty} \frac{1}{1+a_{n-1}}\\
    &=& \displaystyle \frac{1}{1+a}\\
\end{array}
$$

Así pues, tenemos que $a = \frac{-1+\sqrt{5}}{2}$.

$$
\begin{array}{rclr}
    \displaystyle \lim_{n \to \infty} I_n &=& \displaystyle \left\{~ \lim_{n \to \infty} a_n ~\right\}_{0}^{1}\\
    &=& \displaystyle \left\{~ \frac{-1+\sqrt{5}}{2} ~\right\}_{0}^{1}\\
    &=& \displaystyle \frac{-1+\sqrt{5}}{2}\\
\end{array}
$$

**Nota:**

1. Convergencia uniforme:

    - <https://en.wikipedia.org/wiki/Uniform_convergence>
    - <https://alephsub0.org/material-nuevo/jonathan-ortiz/intercambiar-la-integral-y-el-limite/>
    - (video que demuestra el teorema para convergencia uniforme) <https://www.youtube.com/watch?v=SPq6-kEs9CU> 

2. Demostrar que para todo $x \in (0,1)$ se tiene que $\lim_{n \to \infty} a_n  = \frac{-1+\sqrt{5}}{2}$, note que la sucesión $\{a_n\}_{n \geq 1}$ no es monótona para ningún valor de $x \in (0,1)$ lo cual complica las cosas.

    **Proposición:** Sea $\{b_n\}_{n \geq 0}$ una sucesión tal que $\lim_{n \to \infty} b_{2n} = b$ y $\lim_{n \to \infty} b_{2n+1} = b$, entonces $\lim_{n \to \infty} b_{n} = b$

## Ejercicio 16

$$ \int_{-\infty}^{\infty} \frac{\sin^2(x+\pi/4)}{e^{x^2}}  dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sin^2(x+\pi/4) e^{-x^2} ~\right\}_{-\infty}^{\infty}\\
    &=& \displaystyle \frac{1}{2} \left\{~ (\sin(x) + \cos(x))^2 e^{-x^2} ~\right\}_{-\infty}^{\infty} & (1)\\
    &=& \displaystyle \frac{1}{2} \left\{~ (1 + 2 \sin(x) \cos(x)) e^{-x^2} ~\right\}_{-\infty}^{\infty} & (2)\\
    &=& \displaystyle \frac{1}{2} \left\{~ (1 + \sin(2x)) e^{-x^2} ~\right\}_{-\infty}^{\infty} & (3)\\
    &=& \displaystyle \frac{1}{2}( \sqrt{\pi} +  \left\{~ \sin(2x) e^{-x^2} ~\right\}_{-\infty}^{\infty}) & (4)\\
    &=& \displaystyle \frac{\sqrt{\pi}}{2} & (5)\\
\end{array}
$$

- (1): $\sqrt{2} ~ \sin(x + \pi/4) = \sin(x) + \cos(x)$

- (2): $\cos^2(x) + \sin^2(x) = 1$

- (3): $\sin(2x) = 2 \sin(x)\cos(x)$

- (4): Integral Gaussiana $\{e^{-x^2}\}_{-\infty}^{\infty} = \sqrt{\pi}$

- (5): Función impar en intervalo simétrico

## Ejercicio 17

$$ \int_{-\infty}^\infty 3x^2(x^3+1)^2 e^{-x^6-2x^3}  dx $$

$$\textcolor{red}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ (u+1)^2 e^{-(u^2+2u)} ~\right\}_{-\infty}^{\infty}  & (1)\\
    &=& \displaystyle \left\{~ (u+1)^2 e^{-((u+1)^2 - 1)} ~\right\}_{-\infty}^{\infty}\\
    &=& \displaystyle e \left\{~ (u+1)^2 e^{-(u+1)^2} ~\right\}_{-\infty}^{\infty}\\
    &=& \displaystyle e \left\{~ t^2 e^{-t^2} ~\right\}_{-\infty}^{\infty} & (2)\\
    &=& \displaystyle 2e \left\{~ t^2 e^{-t^2} ~\right\}_{0}^{\infty} & (3)\\ \\
    I_1 &=& \displaystyle \left\{~ t^2 e^{-t^2} ~\right\}_{0}^{\infty}\\
    &=& \displaystyle \frac{1}{2} \left\{~ s^{1/2} e^{-s} ~\right\}_{0}^{\infty} & (4)\\
    &=& \displaystyle \frac{1}{2} \Gamma(3/2) & (5)\\
    &=& \displaystyle \frac{1}{4} \Gamma(1/2) & (6)\\
    &=& \displaystyle \frac{1}{4} \sqrt{\pi} & (7)\\ \\
    I &=& \displaystyle \frac{e}{2} \sqrt{\pi}
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& x^3 \\ du &=& 3x^2 ~dx \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} t &=& u+1 \\ dt &=& du \end{array} \right.$

- (3): Función par en intervalo simétrico

- (4): $\left\{\begin{array}{rcl} s &=& t^2 \\ ds &=& 2t ~dt \end{array} \right.$

- (5): $\Gamma(n) = \{t^{n-1}e^{-t}\}_{0}^{+\infty}$

- (6) Para todo $z \in \mathbb{R}$ se tiene que $\Gamma(z+1) = z \Gamma(z)$

- (7): $\Gamma(1/2) = \sqrt{\pi}$ se deduce de la integral gaussiana $\{~ e^{-x^2} ~\}_{-\infty}^{\infty} = \sqrt{\pi}$

## Ejercicio 18

$$ \int_0^{\pi/2} \frac{dx}{1+\tan^{2017}x} $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1}{1+\tan^{\alpha}x} ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle \left\{~ \frac{1}{1+\cot^{\alpha}x} ~\right\}_{0}^{\pi/2} & (1),(2)\\ \\
    2I &=& \displaystyle \left\{~ \frac{1}{1+\tan^{\alpha}x} + \frac{1}{1+\cot^{\alpha}x} ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle \left\{~ \frac{\cos^{\alpha}(x)}{\sin^{\alpha}(x)+\cos^{\alpha}x} + \frac{\sin^{\alpha}(x)}{\sin^{\alpha}(x)+\cos^{\alpha}x} ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle \left\{~ 1 ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle \pi/2\\ \\
    I &=& \displaystyle \frac{\pi}{4}
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \pi/2 - \theta \\ dx &=& -d\theta \end{array} \right.$

- (2): $\tan(\pi/2 - x) =  \cot(x)$

## Ejercicio 19

$$ \int e^{2x} \cos(3x)  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{\cos(3x)}{2}e^{2x} + \frac{3\sin(3x)}{4}e^{2x} - \frac{9}{4} I& (1)\\ \\
    I &=& \displaystyle \frac{4}{13} \left( \frac{\cos(3x)}{2}e^{2x} + \frac{3\sin(3x)}{4}e^{2x} \right) + C\\
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \cos(3x) & e^{2x} \\ -3\sin(3x) & \frac{e^{2x}}{2} \\ -9 \cos(3x) & \frac{e^{2x}}{4}\end{array}$

## Ejercicio 20

$$ \int (\cos(x))^{\cos(x)+1} \tan(x)(1+\log(\cos(x)))  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ (\cos(x))^{\cos(x)} \sin(x) (1+\log(\cos(x))) ~\right\}\\
    &=& \displaystyle -(\cos(x))^{\cos(x)} + C\\
\end{array}
$$

- (1): $[(\cos(x))^{\cos(x)}] = [e^{\cos(x) \ln(\cos(x))}] = -\cos(x)^{\cos(x)}(\sin(x)\ln(\cos(x)) + \sin(x))$