# MIT integration bee - 2016

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

$$ \int \tanh x  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \ln|\cosh(x)| + C\\
\end{array}
$$

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

## Ejercicio 2

$$ \int_{-4}^{4} |x^3 - x|  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2\left\{~ |x||x^2 - 1| ~\right\}_{0}^{4} & (1)\\
    &=& \displaystyle 2 \left( \left\{~ |x||x^2 - 1| ~\right\}_{0}^{1} + \left\{~ |x||x^2 - 1| ~\right\}_{1}^{4} \right)\\
    &=& \displaystyle 2 \left( -\left\{~ x(x^2 - 1) ~\right\}_{0}^{1} + \left\{~ x(x^2 - 1) ~\right\}_{1}^{4} \right)\\
    &=& \displaystyle 2 \left( -\left(~ \frac{x^4}{4} - \frac{x^2}{2} ~\right)_{0}^{1} + \left\{~ \frac{x^4}{4} - \frac{x^2}{2} ~\right\}_{1}^{4} \right)\\
    &=& \displaystyle 2 \left( -\left(~ \frac{x^4}{4} - \frac{x^2}{2} ~\right)_{0}^{1} + \left(~ \frac{x^4}{4} - \frac{x^2}{2} ~\right)_{1}^{4} \right)\\
    &=& 113
\end{array}
$$

- (1): Función par en intervalo simétrico

## Ejercicio 3

$$ \int_1^e \log(\sqrt{x})  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2} \left\{~ \ln(x) ~\right\}_{1}^{e}\\
    &=& \displaystyle \frac{1}{2} \left(~ x\ln(x) - x ~\right)_{1}^{e}\\
    &=& \displaystyle \frac{1}{2}\\
\end{array}
$$

## Ejercicio 4

$$ \int \left( e^{e^x + e^{-x} + x} - e^{e^x + e^{-x} - x} \right)  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ e^{e^x+e^{-x}}(e^{x} - e^{-x}) ~\right\}\\
    &=& \displaystyle \left\{~ e^{2\cosh(x)}(2\sinh(x)) ~\right\}\\
    &=& \displaystyle e^{2\cosh(x)} + C & (1)\\
\end{array}
$$

- (1): $[e^{f(x)}] = e^{f(x)}f'(x)$

## Ejercicio 5

$$ \int \frac{\log(\log(x))}{x \log(x)}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\log(u)}{u} ~\right\} & (1)\\
    &=& \displaystyle \left\{~ s ~\right\} & (2)\\
    &=& \displaystyle \frac{s^2}{2} + C\\
    &=& \displaystyle \frac{(~\ln(\ln(x))~)^2}{2} + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& \ln(x) \\ du &=& \frac{1}{x} ~dx \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} s &=& \ln(u) \\ ds &=& \frac{1}{u} ~du \end{array} \right.$

## Ejercicio 6

$$ \int_0^{\pi/3} \frac{dx}{1 + \tan^2(x)} $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1}{\sec^2(x)} ~\right\}_{0}^{\pi/3} & (1)\\
    &=& \displaystyle \left\{~ \cos^2(x) ~\right\}_{0}^{\pi/3}\\
    &=& \displaystyle \frac{1}{2} \left\{~ \cos(2x) + 1 ~\right\}_{0}^{\pi/3} & (2)\\
    &=& \displaystyle \frac{1}{2} \left(~ \frac{\sin(2x)}{2} + x ~\right)_{0}^{\pi/3}\\
    &=& \displaystyle \frac{\sqrt{3}}{8} + \frac{\pi}{6}
\end{array}
$$

- (1): $\tan^2(x) + 1 = \sec^2(x)$

- (2): $\cos(2x) = 2 \cos^2(x) - 1$

## Ejercicio 7

$$ \int_{-27}^{27} \arcsin \left( \frac{x^{1/3}}{3} \right)  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 0 & (1)\\
\end{array}
$$

- (1): Función impar en intervalo simétrico

## Ejercicio 8

$$ \int_{50}^{100} \lfloor \log_2 x \rfloor dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \lfloor \log_2 x \rfloor ~\right\}_{50}^{64} + \left\{~ \lfloor \log_2 x \rfloor ~\right\}_{64}^{100}\\
    &=& \displaystyle \left\{~ 5 ~\right\}_{50}^{64} + \left\{~ 6 ~\right\}_{64}^{100}\\
    &=& \displaystyle 286
\end{array}
$$

## Ejercicio 9

$$ \int (e^x \cos x - e^x \sin x)  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ e^x(\cos x - \sin x)  ~\right\} \\
    &=& \displaystyle e^x\cos(x) + C & (1)\\
\end{array}
$$

- (1): $[e^xf(x)] = e^x(f(x) + f'(x))$

## Ejercicio 10

$$ \int_0^\infty x^3 e^{-x^2}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ x x^2e^{-x^2}  ~\right\}_{0}^{\infty} \\
    &=& \displaystyle \frac{1}{2}\left\{~ ue^{u}  ~\right\}_{0}^{-\infty}\\
    &=& \displaystyle \frac{1}{2} \left(~ ue^{u}-e^u  ~\right)_{0}^{-\infty} & (2)\\
    &=& \displaystyle \frac{1}{2}
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& -x^2 \\ du &=& -2x ~dx \end{array} \right.$

- (2): $\begin{array}{|c|c|} D & I \\ u & e^{u} \\ 1 & e^u \\ 0 & e^u \end{array}$

## Ejercicio 11

$$ \int ((2e^{x^2}x + 1) \cos x - (e^{x^2} + x) \sin x) \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle (e^{x^2}+x)\cos(x) + C & (1) \\
\end{array}
$$

- (1): $[(e^{x^2} + x)f(x)] = (2e^{x^2}x + 1)f(x) + (e^{x^2} + x)f'(x)$

## Ejercicio 12

$$ \int (1 + x^{1/2} + x^{1/3})(1 + x^{-1/2} + x^{-1/3}) \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 6\left\{~ (1 + t^{3} + t^2)(t^5 + t^2 + t^3) ~\right\} & (1) \\
    &=& \displaystyle 6\left\{~ t^8 + t^7 + t^6 + 3t^5 + t^4 + t^3 + t^2 ~\right\} \\
    &=& \displaystyle 6\left(~ \frac{t^9}{9} + \frac{t^8}{8}  + \frac{t^7}{7} + 3\frac{t^6}{6} + \frac{t^5}{5} + \frac{t^4}{4} + \frac{t^3}{3} ~\right) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^6 \\ dx &=& 6t^5 ~dt \end{array} \right.$

## Ejercicio 13

$$ \int \sin(\sin(x)) \cos(\sin(x)) \cos(x) \ dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sin(u) \cos(u) ~\right\} & (1) \\
    &=& \displaystyle \frac{1}{2} \left\{~ \sin(2u) ~\right\} & (2) \\
    &=& \displaystyle -\frac{\cos(2u)}{4} + C \\
    &=& \displaystyle -\frac{\cos(2\sin(x))}{4} + C \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& \sin(x) \\ du &=& \cos(x) ~dx \end{array} \right.$

- (2): $\sin(2x) = 2 \sin(x)\cos(x)$

## Ejercicio 14

$$ \int \left( \frac{\cos(x) + \sin(x)}{x^2} + \frac{\sin(x) - \cos(x)}{x} \right) \ dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\cos(x) + \sin(x)}{x^2} - \frac{\cos(x) - \sin(x)}{x}  ~\right\} \\
    &=& \displaystyle -\frac{\cos(x) + \sin(x)}{x} + C & (1),(2)\\
\end{array}
$$

- (1): $[\sin(x) + \cos(x)] = \cos(x) - \sin(x)$

- (2): $[\frac{f(x)}{x}] = \frac{-f(x)}{x^2} + \frac{f'(x)}{x}$

## Ejercicio 15

$$ \int x^3 \sqrt{x^2 + 1} \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2}\left\{~ (u-1) u^{1/2} ~\right\} & (1) \\
    &=& \displaystyle \frac{1}{2}\left(~ \frac{2}{5}u^{5/2} - u^{3/2}\frac{2}{3} ~\right) + C \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& x^2 + 1 \\ du &=& 2x ~dx \end{array} \right.$

## Ejercicio 16

$$ \int \frac{x}{x^4 + x^2 + 1} \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2} \left\{~ \frac{1}{u^2 + u + 1} ~\right\} & (1) \\
    &=& \displaystyle \frac{1}{2} \left\{~ \frac{1}{(u+\frac{1}{2})^2  + \frac{3}{4}} ~\right\} \\
    &=& \displaystyle \frac{2}{3} \left\{~ \frac{1}{((u+\frac{1}{2})\frac{2}{\sqrt{3}})^2 + 1} ~\right\} \\
    &=& \displaystyle \frac{1}{\sqrt{3}}  \arctan \left( \left( u+\frac{1}{2} \right) \frac{2}{\sqrt{3}} \right) +  C \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& x^2 \\ du &=& 2x ~dx \end{array} \right.$

## Ejercicio 17

$$ \int e^{e^{2016x} + 6048x} \, dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ e^{e^{\alpha x} + 3\alpha x} ~\right\}\\
    &=& \displaystyle \left\{~ e^{e^{\alpha x}} e^{\alpha x} e^{2\alpha x} ~\right\} \\
    &=& \displaystyle \frac{1}{\alpha} \left\{~ e^{u} u^2 ~\right\} & (1) \\
    &=& \displaystyle \frac{1}{\alpha} \left(~ u^2e^u - 2ue^u + 2e^u ~\right) + C & (2) \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& e^{\alpha x} \\ du &=& \alpha e^{\alpha x} ~dx \end{array} \right.$

- (2): $\begin{array}{|c|c|} D & I \\ u^2 & e^{u} \\ 2u & e^u \\ 2 & e^u \\ 0 & e^u \end{array}$

## Ejercicio 18

$$ \int \frac{dx}{1 - x + x^2 - x^3} $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle -\left\{~ \frac{x+1}{x^4-1} ~\right\} & (1)\\
    &=& \displaystyle -\left\{~ \frac{x+1}{(x-1)(x+1)(x^2+1)} ~\right\}\\
    &=& \displaystyle -\left\{~ \frac{1}{(x-1)(x^2+1)} ~\right\}\\
    &=& \displaystyle -\frac{1}{2}\left\{~ \frac{1}{x-1} - \frac{x+1}{x^2+1} ~\right\}\\
    &=& \displaystyle -\frac{1}{2}\left\{~ \frac{1}{x-1} - \frac{x}{x^2+1} - \frac{1}{x^2+1} ~\right\}\\
    &=& \displaystyle -\frac{1}{2}\left(~ \ln|x-1| - \frac{\ln|x^2+1|}{2} - \arctan(x) ~\right) + C\\
\end{array}
$$

- (1): $a^n - b^n = (a-b)(a^{n-1} + a^{n-2}b + \ldots + ab^{n-2} + b^{n-1})$

## Ejercicio 19

$$ \int_{\pi/3}^{\pi/2} \frac{1 - \cos x}{\sin x}  dx $$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \csc(x) - \cot(x) ~\right\}_{\pi/3}^{\pi/2}\\
    &=& \displaystyle \left(~ -\ln|\csc(x) + \cot(x)| - \ln|\sin(x)| ~\right)_{\pi/3}^{\pi/2}\\
    &=& \displaystyle \ln(\sqrt{3}) + \ln(\sqrt{3}/2)\\
\end{array}
$$

## Ejercicio 20

$$ \int_{0}^{\infty} \frac{dx}{2 + \cosh x} $$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1}{1 + 2\cosh^2(x/2)} ~\right\}_{0}^{\infty} & (1)\\
    &=& \displaystyle \left\{~ \frac{1}{\cosh^2(x/2) - \sinh^2(x/2) + 2\cosh^2(x/2)} ~\right\}_{0}^{\infty} & (2)\\
    &=& \displaystyle \left\{~ \frac{1}{3\cosh^2(x/2) - \sinh^2(x/2)} ~\right\}_{0}^{\infty}\\
    &=& \displaystyle \left\{~ \frac{\text{sech}^2(x/2)}{3 - \tanh^2(x/2)} ~\right\}_{0}^{\infty}\\
    &=& \displaystyle 2\left\{~ \frac{1}{3 - u^2} ~\right\}_{0}^{1} & (3)\\
    &=& \displaystyle 2\left\{~ \frac{1}{(\sqrt{3} - u)(\sqrt{3} + u)}  ~\right\}_{0}^{1}\\
    &=& \displaystyle \frac{1}{\sqrt{3}}\left\{~ \frac{1}{\sqrt{3} - u} + \frac{1}{\sqrt{3} + u}  ~\right\}_{0}^{1}\\
    &=& \displaystyle \frac{1}{\sqrt{3}}\left(~ -\ln|\sqrt{3} - u| + \ln|\sqrt{3} + u|  ~\right)_{0}^{1}\\
    &=& \displaystyle \frac{1}{\sqrt{3}}\ln \left| \frac{\sqrt{3}+1}{\sqrt{3}-1}\right|\\
\end{array}
$$

- (1): $2\cosh^2(x) = 1 + \cosh(2x)$

- (2): $\cosh^2(x) - \sinh^2(x) = 1$

- (3): $\left\{\begin{array}{rcl} u &=& \tanh(x/2) \\ du &=& \frac{\text{sech}^2(x/2)}{2} ~dx \end{array} \right.$

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