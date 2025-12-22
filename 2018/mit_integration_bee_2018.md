# MIT integration bee - 2018

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

$$ \int \frac{e^x}{e^x + 2} \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \ln|e^x+2| + C & (1)\\
\end{array}
$$

- (1): $[\ln(f(x))] = \frac{f'(x)}{f(x)}$

## Ejercicio 2

$$ \int \sqrt{x \cdot \sqrt[3]{x \cdot \sqrt[4]{x \cdot \sqrt[5]{x \cdots}}}} ~dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ x^{\frac{1}{2}} \cdot x^{\frac{1}{2 \cdot 3}} \cdot x^{\frac{1}{2 \cdot 3 \cdot 4}} \cdots ~\right\}\\
    &=& \displaystyle \left\{~ x^{\frac{1}{2!}} \cdot x^{\frac{1}{3!}} \cdot x^{\frac{1}{4!}} \cdots ~\right\}\\
    &=& \displaystyle \left\{~ x^{\sum_{n \geq 2} \frac{1}{n!}}~\right\}\\
    &=& \displaystyle \left\{~ x^{\sum_{n \geq 0} \frac{1}{n!} - 2}~\right\}\\
    &=& \displaystyle \left\{~ x^{e - 2}~\right\} & (1)\\
    &=& \displaystyle \frac{x^{e-1}}{e-1} + C\\
\end{array}
$$

- (1): $e^x = \sum_{n \geq 0} \frac{x^n}{n!}$

## Ejercicio 3

$$ \int_0^{2018\pi} |\sin(2018x)| \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ |\sin(\alpha x)| ~\right\}_{0}^{\alpha \pi}\\
    &=& \displaystyle \frac{1}{\alpha} \left\{~ |\sin(u)| ~\right\}_{0}^{\alpha^2 \pi} & (1)\\
    &=& \displaystyle \frac{2 \alpha^2}{\alpha} \left\{~ |\sin(u)| ~\right\}_{0}^{\pi/2} & (2)\\
    &=& \displaystyle 2 \alpha \left\{~ \sin(u) ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle 2 \alpha \left(~ -\cos(u) ~\right)_{0}^{\pi/2}\\
    &=& \displaystyle 2 \alpha \left(~ -\cos(u) ~\right)_{0}^{\pi/2}\\
    &=& \displaystyle 2 \alpha 
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& \alpha x\\ du &=& \alpha ~dx \end{array} \right.$

- (2) función de periodo $\pi$

## Ejercicio 4

$$ \int \frac{dx}{\tan x + \cot x} $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\sin(x) \cos(x)}{\sin^2(x) + \cos^2(x)} ~\right\}\\
    &=& \displaystyle \left\{~ \sin(x) \cos(x) ~\right\} & (1)\\
    &=& \displaystyle \frac{\sin^2(x)}{2} + C\\
\end{array}
$$

- (1): $\cos^2(x) + \sin^2(x) = 1$

## Ejercicio 5

$$ \int \frac{x^5}{2 + x^{12}} \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{x^5}{2 + (x^6)^2} ~\right\}\\
    &=& \displaystyle \frac{1}{6}\left\{~ \frac{1}{2 + u^2} ~\right\} & (1)\\
    &=& \displaystyle \frac{1}{12}\left\{~ \frac{1}{1 + (\frac{u}{\sqrt{2}})^2} ~\right\} \\
    &=& \displaystyle \frac{\sqrt{2}}{12} \arctan \left(\frac{u}{\sqrt{2}} \right) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& x^6 \\ du &=& 6x^5 ~dx \end{array} \right.$

## Ejercicio 6

$$ \int (\cos x \cosh x + \sin x \sinh x) \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \sin(x) \cosh(x) + C & (1)\\
\end{array}
$$

- (1): $[\sin(x) \cosh(x)] = \cos(x) \cosh(x) + \sin(x)\sinh(x)$

## Ejercicio 7

$$ \int \frac{e^x + \cos x}{e^x + \sin x} ~ dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \ln|e^x+\sin(x)| + C & (1)\\
\end{array}
$$

- (1): $[\ln(f(x))] = \frac{f'(x)}{f(x)}$

## Ejercicio 8

$$ \int \sin(\cos(\sin x)) \sin(\sin x) \cos x \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sin(\cos(u)) \sin(u) ~\right\} & (1)\\
    &=& \displaystyle -\left\{~ \sin(t) ~\right\} & (2)\\
    &=& \displaystyle \cos(t) + C\\
    &=& \displaystyle \cos(\cos(\sin(x))) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& \sin(x) \\ du &=& \cos(x) ~dx \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} t &=& \cos(u) \\ dt &=& -\sin(u) ~du \end{array} \right.$

## Ejercicio 9

$$ \int \frac{dx}{1 + \sin(x)} $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\sec(x)}{\sec(x) + \tan(x)} ~\right\}\\
    &=& \displaystyle \left\{~ \frac{\sec(x)(~\sec(x) + \tan(x)~)}{(\sec(x) + \tan(x))^2} ~\right\}\\
    &=& \displaystyle \left\{~ \frac{1}{u^2} ~\right\} & (1)\\
    &=& \displaystyle - \frac{1}{u} + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& \sec(x) + \tan(x) \\ du &=& \sec(x)(~\sec(x) + \tan(x)~) ~dx \end{array} \right.$

## Ejercicio 10

$$ \int \frac{\cos x}{1 - \cos(2x)} \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2} \left\{~ \frac{\cos x}{\sin^2(x)} ~\right\} & (1)\\
    &=& \displaystyle -\frac{1}{2} \frac{1}{\sin(x)} + C & (2)\\
    &=& \displaystyle -\frac{\csc(x)}{2} + C\\
\end{array}
$$

- (1): $\cos(2x) = 1 - 2 \sin^2(x)$

- (2): $[\frac{1}{f(x)}] = -\frac{f`(x)}{f^2(x)}$

## Ejercicio 11

$$ \int e^x (1/x + \log x) \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle e^x\ln(x) + C & (1)\\
\end{array}
$$

- (1): $[e^xf(x)] = e^x(f(x) + f'(x))$

## Ejercicio 12

$$ \int \tanh^2(x) \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ 1 - \text{sech}^2(x) ~\right\} & (1)\\
    I &=& \displaystyle x - \tanh(x) + C & (2)\\
\end{array}
$$

- (1): $1 - \tanh^2(x) = \text{sech}^2(x)$

- (2): $[\tanh(x)] = \text{sech}^2(x)$

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

## Ejercicio 13

$$ \int \frac{2017x^{2016} + 2018x^{2017}}{1 + x^{4034} + 2x^{4035} + x^{4036}} \, dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\alpha x^{\alpha-1} + (\alpha+1)x^{\alpha}}{1 + x^{2\alpha} + 2x^{2 \alpha + 1} + x^{2\alpha + 2}} ~\right\}\\
    &=& \displaystyle \left\{~ \frac{\alpha x^{\alpha-1} + (\alpha+1)x^{\alpha}}{1 + (x^{\alpha+1} + x^{\alpha})^2} ~\right\} & (1)\\
    &=& \displaystyle \left\{~ \frac{1}{1 + u^2} ~\right\} & (2)\\
    &=& \displaystyle \arctan(u) + C\\
\end{array}
$$

- (1): Triángulo de Pascal

- (2): $\left\{\begin{array}{rcl} u &=& x^{\alpha +1} + x^{\alpha}\\ du &=& (~ (\alpha + 1) x^{\alpha} + \alpha x^{\alpha - 1} ~) ~dx \end{array} \right.$

## Ejercicio 14

$$ \int \frac{\sin(2x) - \sin^2 x}{\cos(2x) - \cos^2 x} \, dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\sin(2x) - \sin^2 x}{ \cos^2 x - 1} ~\right\} & (1)\\
    &=& \displaystyle -\left\{~ \frac{\sin(2x) - \sin^2 x}{\sin^2(x)} ~\right\} & (2)\\
    &=& \displaystyle -\left\{~ \frac{\sin(2x)}{\sin^2(x)} - 1 ~\right\}\\
    &=& \displaystyle -\left\{~ \frac{2\sin(x)\cos(x)}{\sin^2(x)} - 1 ~\right\} & (3)\\
    &=& \displaystyle -\left\{~ 2\cot(x) - 1 ~\right\}\\
    &=& \displaystyle -\left(~ 2\ln|\sin(x)| - x ~\right) + C\\
    &=& \displaystyle x - 2\ln|\sin(x)| + C\\
\end{array}
$$

- (1): $\cos(2x) = 2 \cos^2(x) - 1$

- (2): $\cos^2(x) + \sin^2(x) = 1$

- (3): $\sin(2x) = 2 \sin(x)\cos(x)$

## Ejercicio 15

$$ \int \frac{dx}{x^{\frac{25}{25}} \cdot x^{\frac{16}{25}} + x^{\frac{9}{25}}} $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 25 \left\{~ \frac{t^{16}}{t^{32} + 1}  ~\right\} & (1)\\
    &=& \displaystyle 25 \left\{~ \frac{t^{15}}{(t^{16})^2 + 1}  ~\right\}\\
    &=& \displaystyle \frac{25}{16} \left\{~ \frac{1}{u^2 + 1}  ~\right\} & (2)\\
    &=& \displaystyle \frac{25}{16}\arctan(u) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^{25} \\ dx &=& 25t^{24} ~dt \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} u &=& t^{16} \\ du &=& 16t^{15} ~dt \end{array} \right.$

## Ejercicio 16

$$ \int_0^{\pi/2} \frac{\cos(x)}{2 - \cos^2(x)} \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\cos(x)}{1 + \sin^2(x)} ~\right\}_{0}^{\pi/2} & (1)\\
    &=& \displaystyle \left\{~ \frac{1}{1 + u^2} ~\right\}_{0}^{1} & (2)\\
    &=& \displaystyle \left(~ \arctan(u) ~\right)_{0}^{1}\\
    &=& \displaystyle \frac{\pi}{4}\\
\end{array}
$$

- (1): $\cos^2(x) + \sin^2(x) = 1$

- (2): $\left\{\begin{array}{rcl} u &=& \sin(x) \\ du &=& \cos(x) ~dx \end{array} \right.$

## Ejercicio 17

$$ \int \frac{dx}{(1 + x^2)^{3/2}} $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\sec^2(\theta)}{\sec^3(\theta)} ~\right\} & (1)\\
    &=& \displaystyle \left\{~ \cos(\theta) ~\right\}\\
    &=& \displaystyle \sin(\theta) + C\\
    &=& \displaystyle \frac{x}{\sqrt{x^2+1}} + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \tan(\theta) \\ dx &=& \sec^2(\theta) ~d\theta \end{array} \right.$

## Ejercicio 18

$$ \int \frac{dx}{\sqrt{x\sqrt{x} - x^2}} $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2\left\{~ \frac{t}{\sqrt{t^3 - t^4}} ~\right\} & (1)\\
    &=& \displaystyle 2\left\{~ \frac{1}{\sqrt{t - t^2}} ~\right\}\\
    &=& \displaystyle 4\left\{~ \frac{u}{\sqrt{u^2 - u^4}} ~\right\} & (2)\\
    &=& \displaystyle 4\left\{~ \frac{1}{\sqrt{1 - u^2}} ~\right\}\\
    &=& \displaystyle 4\arcsin(u) + C\\
    &=& \displaystyle 4\arcsin(x^{1/4}) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^2 \\ dx &=& 2t ~dt \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} t &=& u^2 \\ dt &=& 2u ~dt \end{array} \right.$

## Ejercicio 19

$$ \int \frac{x - 1}{x + x^2 \log x} \, dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{u-1}{u^2 - u \ln u} ~\right\} & (1)\\
    &=& \displaystyle \left\{~ \frac{1-\frac{1}{u}}{u - \ln u} ~\right\}\\
    &=& \displaystyle \ln |u - \ln(u)| + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \frac{1}{u} \\ dx &=& -\frac{1}{u^2} ~du \end{array} \right.$

- (2): $[\ln(f(x))] = \frac{f'(x)}{f(x)}$

## Ejercicio 20

$$ \int \csc(x) \sec(x) \, dx $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\sin^2(x) + \cos^2(x)}{\sin(x)\cos(x)} ~\right\} & (1)\\
    &=& \displaystyle \left\{~ \tan(x) + \cot(x) ~\right\} \\
    &=& \displaystyle -\ln|\cos(x)| + \ln|\sin(x)| + C \\
\end{array}
$$

- (1): $\cos^2(x) + \sin^2(x) = 1$