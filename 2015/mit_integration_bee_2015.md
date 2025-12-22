# MIT integration bee - 2015

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

$$ \int ( \cos^4 x - \sin^4 x )  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle -\left\{~ (\cos^2(x) - \sin^2(x))(\cos^2(x) + \sin^2(x))~\right\} \\
    &=& \displaystyle -\left\{~ \cos(2x) ~\right\} & (1)\\
    &=& \displaystyle \frac{\sin(2x)}{2} + C\\
\end{array}
$$

- (1): $\cos(2x) = \cos^2(x) - \sin^2(x)$

## Ejercicio 2

$$ \int \frac{x}{\sqrt{2 + 4x}}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{16}\left\{~ \frac{u-2}{u^{1/2}}~\right\} \\
    &=& \displaystyle \frac{1}{16}\left(~ \frac{2}{3}u^{3/2} - 4 u^{1/2} ~\right) + C \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} 2+4x &=& u \\ 4dx &=& du \end{array} \right.$

## Ejercicio 3

$$ \int_0^8 \frac{\cos \sqrt{x}}{\sqrt{x}}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2 \left\{~ \cos(t) ~\right\}_{0}^{2\sqrt{2}} & (1)\\
    &=& \displaystyle 2 \left(~ \sin(t) ~\right)_{0}^{2\sqrt{2}}\\
    &=& \displaystyle 2 \sin(2\sqrt{2})\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} t &=& \sqrt{x} \\ dt &=& \frac{1}{2\sqrt{x}} ~ dx \end{array} \right.$

## Ejercicio 4

$$ \int \sec x  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \ln |\sec(x) + \tan(x)| + C
\end{array}
$$

- (1): $\sec(x) = \frac{\sec(x)(\sec(x) + \tan(x))}{\sec(x) + \tan(x)}$

- (2): $[\sec(x) + \tan(x)] = \sec(x) (\sec(x) + \tan(x))$

## Ejercicio 5

$$ \int_0^{\pi/2} \frac{e^{\sin x}}{\tan x \csc x}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ e^{\sin(x)}\cos(x) ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle \left(~ e^{\sin(x)} ~\right)_{0}^{\pi/2} & (1)\\
    &=& \displaystyle e-1
\end{array}
$$

- (1): $[e^{f(x)}] = e^{f(x)}f'(x)$

## Ejercicio 6

$$ \int_1^e x (\log x)^2  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2}\left(~ (\ln(x)x)^2 ~\right)_{1}^{e} - \left\{~ x \ln(x) ~\right\}_{1}^{e} & (1)\\
    &=& \displaystyle \frac{e^2}{2} - \left\{~ x \ln(x) ~\right\}_{1}^{e}\\
    &=& \displaystyle \frac{e^2}{2} - \left(~ \frac{\ln(x)x^2}{2} - \frac{x^2}{4}~\right)_{1}^{e} & (2)\\
    &=& \displaystyle \frac{e^2}{4} - \frac{1}{4} \\
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \ln^2(x) & x \\ \frac{2\ln(x)}{x} & \frac{x^2}{2}\end{array}$

- (2): $\begin{array}{|c|c|} D & I \\ \ln(x) & x \\ \frac{1}{x} & \frac{x^2}{2} \end{array}$

## Ejercicio 7

$$ \int \frac{1}{5 + 4\sqrt{x} + x}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{2t}{5 + 4t + t^2} ~\right\} & (1)\\
    &=& \displaystyle \left\{~ \frac{2t + 4 }{5 + 4t + t^2}  - \frac{4}{5 + 4t + t^2} ~\right\} \\
    &=& \displaystyle \left\{~ \frac{2t + 4 }{5 + 4t + t^2}  - \frac{4}{(t+2)^2 + 1} ~\right\}\\
    &=& \displaystyle  \ln|5 + 4t + t^2|  - 4 \arctan(t+2) +  C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^2 \\ dx &=& 2t ~dt \end{array} \right.$

## Ejercicio 8

$$ \int (2015)^x  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{2015^x}{\ln(2015)} + C  & (1)\\
\end{array}
$$

- (1): $[a^x] = a^x \ln(a)$

## Ejercicio 9

$$ \int_0^2 \frac{x}{(x-3)(x+5)^2}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{5}{8}\left\{~ \left( \frac{3/5}{x-3} + \frac{1}{x+5} \right)\frac{1}{x+5} ~\right\}_{0}^{2}\\
    &=& \displaystyle \frac{5}{8}\left\{~ \frac{3}{40}\left( \frac{1}{x-3} - \frac{1}{x+5} \right) + \frac{1}{(x+5)^2} ~\right\}_{0}^{2}\\
    &=& \displaystyle \frac{5}{8} \left(~ \frac{3}{40}\left( \ln|x-3| - \ln|x+5| \right) - \frac{1}{x+5} ~\right)_{0}^{2}\\
    &=& \displaystyle \frac{3}{64}\ln(5/21) + \frac{1}{28}
\end{array}
$$

**Nota:**

1. Hacer fracciones parciales para el producto de dos factores es más sencillo que determinar los coeficientes de toda la fracción parcial.

## Ejercicio 10

$$ \int \frac{\log(1+\log x)}{x}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \log(1+t) ~\right\} & (1)\\
    &=& \displaystyle (1+t)\log(1+t) - (1+t) + C\\
    &=& \displaystyle (1+t)\log(1+t) - (1+t) + C\\
    &=& \displaystyle \log(1+\ln(x)) + \ln(x)(\ln(1+\ln(x))-1) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} t &=& \ln(x)\\ dt &=& \frac{1}{x} ~dx \end{array} \right.$

## Ejercicio 11

$$ \int \sqrt{\csc x - \sin x}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sqrt{\frac{1-\sin^2(x)}{\sin(x)}} ~\right\}\\
    &=& \displaystyle \pm \left\{~ \frac{\cos(x)}{\sqrt{\sin(x)}} ~\right\}\\
    &=& \displaystyle \pm 2\sqrt{\sin(x)} +  C & (1)\\
\end{array}
$$

- (1): $[\sqrt{f(x)}] =\frac{f'(x)}{2\sqrt{f(x)}}$

## Ejercicio 12

$$ \int \frac{1}{\sqrt{x^2 + 25}}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{5} \left\{~ \sec(\theta)~\right\}\\
    &=& \displaystyle \frac{1}{5} \ln|\sec(\theta) + \tan(\theta)| + C\\
    &=& \displaystyle \frac{1}{5} \ln \left| \frac{\sqrt{x^2 + 25}}{5} + \frac{x}{5} \right| + C
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& 5 \tan(\theta)\\ dx &=& 5\sec^2(\theta) ~d\theta \end{array} \right.$

## Ejercicio 13

$$ \int_2^e \frac{\log^2 x - 1}{x \log^2 x}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{t^2 - 1}{t^2} ~\right\}_{\ln(2)}^{1} & (1)\\
    &=& \displaystyle \left(~ t + \frac{1}{t} ~\right)_{\ln(2)}^{1}\\
    &=& \displaystyle -\frac{(\ln(2)-1)^2}{\ln(2)}\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} t &=& \ln(x)\\ dd &=& \frac{1}{x} ~dx \end{array} \right.$

## Ejercicio 14

$$ \int e^{3x} \arctan e^x  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle  \frac{\arctan(e^x)e^{3x}}{3} - \frac{1}{3} \left\{~  \frac{e^{4x}}{1 + e^{2x}}~\right\} & (1)\\
    &=& \displaystyle  \frac{\arctan(e^x)e^{3x}}{3} - \frac{1}{6} \left\{~  \frac{t}{1 + t}~\right\} & (2)\\
    &=& \displaystyle  \frac{\arctan(e^x)e^{3x}}{3} - \frac{1}{6} \left(~ t - \ln|1+t| ~\right) \\
    &=& \displaystyle  \frac{\arctan(e^x)e^{3x}}{3} - \frac{1}{6} \left(~ e^{2x} - \ln|1+e^{2x}| ~\right) + C \\
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \arctan(e^x) & e^{3x} \\ \frac{e^x}{1+e^{2x}} & \frac{e^{3x}}{3}\end{array}$

- (2): $\left\{\begin{array}{rcl} t &=& e^{2x} \\ dt &=& 2e^{2x} ~dx \end{array} \right.$

## Ejercicio 15

$$ \int_0^4 \frac{|x-1|}{|x-2| + |x-3|} $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle  \left\{~  \frac{x-1}{2x-5} ~\right\}_{0}^{1} - \left\{~  \frac{x-1}{2x-5} ~\right\}_{1}^{2} + \left\{~  x-1 ~\right\}_{2}^{3} +  \left\{~  \frac{x-1}{2x-5} ~\right\}_{3}^{4}\\
    &=& \displaystyle \frac{1}{2}\left\{~ \frac{2x-2}{2x-5} ~\right\}_{0}^{1} - \frac{1}{2}\left\{~  \frac{2x-2}{2x-5} ~\right\}_{1}^{2} + \left\{~  x-1 ~\right\}_{2}^{3} +  \frac{1}{2}\left\{~  \frac{2x-2}{2x-5} ~\right\}_{3}^{4}\\
    &=& \displaystyle \frac{1}{2}\left\{~ 1 + \frac{3}{2x-5} ~\right\}_{0}^{1} - \frac{1}{2}\left\{~ 1 + \frac{3}{2x-5} ~\right\}_{1}^{2} + \left\{~  x-1 ~\right\}_{2}^{3} +  \frac{1}{2}\left\{~ 1 + \frac{3}{2x-5} ~\right\}_{3}^{4}\\
    &=& \displaystyle \frac{1}{2}\left(~ x + 3 ~\frac{\ln|2x-5|}{2} ~\right)_{0}^{1} - \frac{1}{2}\left(~ x + 3 \frac{\ln|2x-5|}{2} ~\right)_{1}^{2} + \left(~  \frac{x^2}{2} - x ~\right)_{2}^{3} +  \frac{1}{2}\left(~ x + 3 \frac{\ln|2x-5|}{2} ~\right)_{3}^{4}\\
    &=& \displaystyle \frac{9}{4}\ln(3) - \frac{3}{4}\ln(5) + 2
\end{array}
$$

## Ejercicio 16

$$ \int_0^{2\pi} \frac{1}{\sin^4 x + \cos^4 x}  dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~  \frac{1}{(\sin^2(x) + \cos^2(x)) - 2 \sin^2(x)\cos^2(x)} ~\right\}_{0}^{2\pi}\\
    &=& \displaystyle \left\{~  \frac{1}{1 - 2 \sin^2(x)\cos^2(x)} ~\right\}_{0}^{2\pi}\\
    &=& \displaystyle 2 \left\{~ \frac{1}{2 - \sin^2(2x)} ~\right\}_{0}^{2\pi} & (1)\\
    &=& \displaystyle 2 \left\{~ \frac{1}{2(\cos^2(2x) + \sin^2(2x)) - \sin^2(2x)} ~\right\}_{0}^{2\pi}\\
    &=& \displaystyle 2 \left\{~ \frac{1}{ \sin^2(2x) + 2 \cos^2(2x) } ~\right\}_{0}^{2\pi}\\
    &=& \displaystyle \left\{~ \frac{\sec^2(2x)}{ (\tan(2x)/\sqrt{2})^2 + 1 } ~\right\}_{0}^{2\pi}\\
    &=& \displaystyle \sum_{n=0}^{7} \left\{~ \frac{\sec^2(2x)}{ (\tan(2x)/\sqrt{2})^2 + 1 } ~\right\}_{n\pi/4}^{(n+1)\pi/4} \\
    &=& \displaystyle \frac{1}{\sqrt{2}} \left( \left\{~ \frac{1}{ t^2 + 1 } ~\right\}_{0}^{+\infty} + \left\{~ \frac{1}{ t^2 + 1 } ~\right\}_{-\infty}^{+\infty} + \left\{~ \frac{1}{ t^2 + 1 } ~\right\}_{-\infty}^{+\infty} + \left\{~ \frac{1}{ t^2 + 1 } ~\right\}_{-\infty}^{+\infty} + \left\{~ \frac{1}{ t^2 + 1 } ~\right\}_{-\infty}^{0} \right)& (2)\\
    &=& \displaystyle \frac{1}{\sqrt{2}} \left( \left(~ \arctan(t) ~\right)_{0}^{+\infty} + 3 \left(~ \arctan(t) ~\right)_{-\infty}^{+\infty} + \left(~ \arctan(t) ~\right)_{-\infty}^{0}\right) \\
    &=& \displaystyle 2\sqrt{2}\pi
\end{array}
$$

- (1): $\sin(2x) = 2\sin(x)\cos(x)$

- (2): $\left\{\begin{array}{rcl} t &=& \frac{\tan(2x)}{\sqrt{2}} \\ dt &=& \sqrt{2} \sec^2(2x) ~dx \end{array} \right.$

## Ejercicio 17

$$ \int \frac{1 + e^x}{1 - e^x}  dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2 \left\{~ \frac{1+e^{2t}}{1-e^{2t}} ~\right\} & (1)\\
    &=& \displaystyle -2 \left\{~ \frac{\cosh(t)}{\sinh(t)} ~\right\}\\
    &=& \displaystyle -2 \ln|\sinh(t)| + C\\
    &=& \displaystyle -2 \ln|\sinh(x/2)| + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& 2t \\ dx &=& 2 ~dt \end{array} \right.$

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

## Ejercicio 18

$$ \int \tan^4 x  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \tan^2(x)\sec^2(x) -\sec^2(x) + 1 ~\right\} & (1)\\
    &=& \displaystyle \frac{\tan^3(x)}{3} - \tan(x) + x + C
\end{array}
$$

- (1): $\tan^2(x) + 1 = \sec^2(x)$

## Ejercicio 19

$$ \int \sin x \tan^2 x  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\sin(x) (1 - \cos^2(x))}{\cos^2(x)}~\right\}\\
    &=& \displaystyle \left\{~ \frac{u^2 - 1}{u^2} ~\right\} & (1)\\
    &=& \displaystyle u + \frac{1}{u} + C\\
    &=& \displaystyle \cos(x) + \sec(x) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& \cos(x) \\ du &=& -\sin(x) ~dx \end{array} \right.$

## Ejercicio 20

$$ \int \frac{x + 1}{x^2 + 2x + 3}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2}\left\{~ \frac{2x+2}{x^2+2x+3}~\right\}\\
    &=& \displaystyle \frac{1}{2} \ln |x^2+2x+3| + C
\end{array}
$$

- (1): $[\ln(f(x))] = \frac{f'(x)}{f(x)}$