# MIT integration bee - 2012

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

$$
\int \frac{dx}{\sqrt{x} - 1}
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2 \left\{~ \frac{t}{t-1} ~\right\} & (1)\\
    &=& \displaystyle 2 \left(~ t + \ln(|t-1|) ~\right) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^2 \\ dx &=& 2t dt \end{array} \right.$

## Ejercicio 2

$$
\int x^{1/4} \log(x)  dx
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{4}{5}x^{5/4}\ln(x) - \frac{4}{5}\left\{~ x^{1/4} ~\right\} & (1)\\
    &=& \displaystyle \frac{4}{5}x^{5/4}\ln(x) - \frac{16}{25} x^{5/4} + C\\
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \ln(x) & x^{1/4} \\ \frac{1}{x} & \frac{4}{5} x^{5/4}\end{array}$

## Ejercicio 3

$$
\int \frac{dx}{(1 + \sqrt{x}) \sqrt{x - x^2}}
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1}{\sqrt{x}(1 + \sqrt{x}) \sqrt{1 - x}} ~\right\}\\
    &=& \displaystyle 2 \left\{~ \frac{1}{(1 + t) \sqrt{1 - t^2}} ~\right\} & (1)\\
    &=& \displaystyle 2 \left\{~ \frac{\cos(\theta)}{(~1 + \sin(\theta)~)|\cos(\theta)|} ~\right\} & (2)\\
    &=& \displaystyle \pm 2 \left\{~ \frac{1}{1 + \sin(\theta)} ~\right\}\\
    &=& \displaystyle \pm 2 \left\{~ \frac{\sec(\theta)}{\sec(\theta) + \tan(\theta)} ~\right\}\\
    &=& \displaystyle \pm 2 \left\{~ \frac{\sec(\theta)(~\sec(\theta) + \tan(\theta)~)}{(~\sec(\theta) + \tan(\theta)~)^2} ~\right\}\\
    &=& \displaystyle \mp 2 \frac{1}{\sec(\theta) + \tan(\theta)} + C & (3) ~,~ (4)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^2 \\ dx &=& 2t ~dt \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} t &=& \sin(\theta) \\ dt &=& \cos(\theta) ~d\theta \end{array} \right.$

- (3): $[\sec(\theta) + \tan(\theta)] = \sec(\theta)(\sec(\theta) + \tan(\theta))$

- (4): $\left[ \frac{1}{f(x)} \right] = \frac{-f'(x)}{f^2(x)}$

## Ejercicio 4

$$
\int \frac{dx}{\sqrt{x} (\sqrt[4]{x} + 1)^{10}}
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 4 \left\{~ \frac{t}{(t + 1)^{10}} ~\right\} & (1)\\
    &=& \displaystyle 4 \left\{~ \frac{u-1}{u^{10}} ~\right\} & (2)\\
    &=& \displaystyle 4 \left(~ -\frac{u^{-8}}{8} + \frac{u^{-9}}{9} ~\right) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^4 \\ dx &=& 4t^3 ~dt \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} u &=& t + 1 \\ du &=& dt \end{array} \right.$

## Ejercicio 5

$$
\int_{0}^{1} \sin(\cos^{-1}(x))  dx
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sin^2(\theta) ~\right\}_{0}^{\pi/2} & (1)\\
    &=& \displaystyle \frac{1}{2} \left\{~ 1 - \cos(2\theta) ~\right\}_{0}^{\pi/2} & (2)\\
    &=& \displaystyle \frac{1}{2} \left(~ \theta - \frac{\sin(2\theta)}{2} ~\right)_{0}^{\pi/2}\\
    &=& \displaystyle \frac{\pi}{4} \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \cos(\theta) \\ dx &=& - \sin(\theta)~d\theta \end{array} \right.$

- (2): $\cos(2x) = 1- 2 \sin^2(x)$

## Ejercicio 6

$$
\int \frac{dx}{\sqrt{1 - 4x - x^2}}
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1}{\sqrt{5 -(x+2)^2}} ~\right\}\\
    &=& \displaystyle \frac{1}{\sqrt{5}} \left\{~ \frac{1}{\sqrt{1 -\left( \frac{x+2}{\sqrt{5}} \right)^2}} ~\right\}\\
    &=& \displaystyle \arctan \left( \frac{x+2}{\sqrt{5}} \right) + C
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \cos(\theta) \\ dx &=& - \sin(\theta)~d\theta \end{array} \right.$

- (2): $\cos(2x) = 1- 2 \sin^2(x)$

## Ejercicio 7

$$
\int_{1/4}^{1/2} \left \lfloor \log \left \lfloor \frac{1}{x} \right \rfloor \right \rfloor  dx
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \left \lfloor \log \left \lfloor \frac{1}{x} \right \rfloor \right \rfloor ~\right\}_{1/4}^{1/3} + \left\{~ \left \lfloor \log \left \lfloor \frac{1}{x} \right \rfloor \right \rfloor ~\right\}_{1/3}^{1/2} \\ \\
    I_1 &=& \displaystyle \left\{~ \left \lfloor \log \left \lfloor \frac{1}{x} \right \rfloor \right \rfloor ~\right\}_{1/4}^{1/3}\\
    &=& \displaystyle \left\{~ \left \lfloor \ln(3) \right \rfloor ~\right\}_{1/4}^{1/3} & (1)\\
    &=& \displaystyle \frac{1}{12} & (2)\\ \\
    I_2 &=& \displaystyle \left\{~ \left \lfloor \log \left \lfloor \frac{1}{x} \right \rfloor \right \rfloor ~\right\}_{1/3}^{1/2}\\
    &=& \displaystyle \left\{~ \left \lfloor \ln(2) \right \rfloor ~\right\}_{1/3}^{1/2} & (3)\\
    &=& \displaystyle 0 \\ \\
    I &=& \displaystyle \frac{1}{12}
\end{array}
$$

- (1): Si $1/4 < x < 1/3$, entonces $3 < \frac{1}{x} < 4$

- (2): $e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!}$

- (3): Si $1/3 < x < 1/2$, entonces $2 < \frac{1}{x} < 3$

## Ejercicio 8

$$
\int_0^{\frac{\pi}{2}} \frac{dx}{1 + \sin(x)}
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\sec(x) }{\sec(x) + \tan(x)} ~\right\}_{0}^{\pi/2} \\
    &=& \displaystyle \left\{~ \frac{\sec(x)(\sec(x) + \tan(x)) }{ (\sec(x) + \tan(x))^2 } ~\right\}_{0}^{\pi/2} \\
    &=& \displaystyle -\left(~ \frac{1}{\sec(x) + \tan(x)} ~\right)_{0}^{\pi/2} \\
    &=& \displaystyle 1 \\
\end{array}
$$

- (1): $[\sec(x) + \tan(x)] = \sec(x) (\sec(x) + \tan(x))$

- (2): $\left[ \frac{1}{f(x)} \right] = \frac{-f'(x)}{f^2(x)}$

## Ejercicio 9

$$
\int_1^{2011} \frac{\sqrt{x}}{\sqrt{2012 - x} + \sqrt{x}}  dx
$$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\sqrt{x}}{\sqrt{\alpha - x} + \sqrt{x}} ~\right\}_{1}^{\alpha-1} \\
    &=& \displaystyle \left\{~ \frac{\sqrt{\alpha - t}}{\sqrt{t} + \sqrt{\alpha - t}} ~\right\}_{1}^{\alpha-1} & (1)\\ \\
    2I &=& \displaystyle \left\{~ \frac{\sqrt{x}}{\sqrt{\alpha - x} + \sqrt{x}} + \frac{\sqrt{\alpha - x}}{\sqrt{x} + \sqrt{\alpha - x}} ~\right\}_{1}^{\alpha-1}\\
    &=& \displaystyle \alpha\\ \\
    I &=& \displaystyle \frac{\alpha}{2}
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \alpha - t \\ dx &=& -dt \end{array} \right.$

## Ejercicio 10

$$
\int \frac{x - 1}{(x + 1) \sqrt{x^3 + x^2 + x}}  dx
$$

$$\textcolor{red}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2 \left\{~ \frac{t^2 - 1}{(t^2 + 1) \sqrt{t^4 + t^2 + 1}} ~\right\} & (1) \\
    &=& \displaystyle 2 \left\{~ \frac{t^2-1}{t^2} ~ \frac{t^2}{t^2+1} ~ \frac{1}{t\sqrt{t^2 + \frac{1}{t^2} + 1}} ~\right\}\\
    &=& \displaystyle 2 \left\{~ \left(1 -\frac{1}{t^2} \right)~ \frac{1}{t+\frac{1}{t}} ~ \frac{1}{\sqrt{(t+\frac{1}{t})^2-1}} ~\right\} \\
    &=& \displaystyle 2 \left\{~ \frac{1}{u\sqrt{u^2-1}} ~\right\} & (2)\\
    &=& \displaystyle 2 ~\text{arcsec}(u) + C & (3)\\
    &=& \displaystyle 2 ~\text{arcsec} \left(~ \frac{x+1}{\sqrt{x}} ~\right) + C \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^2 \\ dx &=& 2t~dt \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} u &=& t + \frac{1}{t} \\ du &=& (1 - \frac{1}{t^2})~dt \end{array} \right.$

**Nota:**

1. ¿Cuándo podemos utilizar la sustitución $u = t + \frac{1}{t}$?.

    - $\left\{\begin{array}{rcl} u &=& \frac{t^2+1}{t} \\ du &=& \frac{t^2-1}{t^2}~dt \end{array} \right.$

    - $\frac{u}{u'} = t ~ \frac{t^2+1}{t^2-1} ~~,~~ \frac{u'}{u} =  \frac{t^2-1}{t(t^2+1)}$

    - $(t+ \frac{1}{t})^2 = t^2+\frac{1}{t^2} + 2$

## Ejercicio 11

$$
\int_{-1}^0 \frac{x^4 + 4x^3 + 6x^2 + 4x + 1}{x^3 - 3x^2 + 3x - 1}  dx
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{(x+1)^4}{(x-1)^3} ~\right\}_{-1}^{0} & (1) \\
    &=& \displaystyle \left\{~ \frac{(t+2)^4}{t^3} ~\right\}_{-2}^{-1} & (2) \\
    &=& \displaystyle \left\{~ t + 8 + 24t^{-1} +32t^{-2} + 16t^{-3} ~\right\}_{-2}^{-1} \\
    &=& \displaystyle \left(~ \frac{t^2}{2} + 8t + 24\ln |t| -32t^{-1} - 8 t^{-2} ~\right)_{-2}^{-1} \\
    &=& \displaystyle \frac{33}{2} - 24 \ln(2) \\
\end{array}
$$

- (1): Triángulo de pascal

- (2): $\left\{\begin{array}{rcl} t &=& x-1 \\ dt &=& dx \end{array} \right.$

## Ejercicio 12

$$
\int \left( \cos(x) \log(x) + \frac{\sin(x)}{x} \right)  dx
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \sin(x)\ln(x) + C & (1) \\
\end{array}
$$

- (1): $[f(x)\ln(x)] = f'(x)\ln(x) + \frac{f(x)}{x}$

## Ejercicio 13

$$
\int \frac{dx}{x^3 - x}
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1}{x(x^2 - 1)}  ~\right\}\\
    &=& \displaystyle - \left\{~ \frac{1}{\sin(\theta)\cos(\theta)}  ~\right\} & (1)\\
    &=& \displaystyle -2 \left\{~ \frac{1}{\sin(2\theta)}  ~\right\} & (2)\\
    &=& \displaystyle -2 \left\{~ \csc(2\theta) ~\right\}\\
    &=& \displaystyle \ln | \csc(2\theta) + \cot(2\theta)| + C & (3)\\
    &=& \displaystyle \frac{1}{2} \ln \left| 1 - \frac{1}{x^2} \right| + C \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \sin(\theta) \\ dx &=& \cos(\theta)~d\theta \end{array} \right.$

- (2): $[\sin(2\theta)] = 2 \sin(\theta)\cos(\theta)$

- (3): $[\csc(\theta) + \cot(\theta)] = -\csc(\theta)(\csc(\theta) + \cot(\theta))$

## Ejercicio 14

$$
\int_0^{1/2} \frac{x \sin^{-1}(x)}{\sqrt{1-x^2}}  dx
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sin(u) ~ u ~\right\}_{0}^{\pi/6} & (1)\\
    &=& \displaystyle \left(~ -u \cos(u) + \sin(u) ~\right)_{0}^{\pi/6} & (2)\\
    &=& \displaystyle \frac{1}{2} - \pi \frac{\sqrt{3}}{12}\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& \arcsin(x) \\ du &=& \frac{1}{\sqrt{1-x^2}}~dx \end{array} \right.$

- (2): $\begin{array}{|c|c|} D & I \\ u & \sin(u) \\ 1 & -\cos(u) \\ 0 & - \sin(u) \end{array}$

## Ejercicio 15

$$
\int_0^1 x(1-x)^{99}  dx
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ u^{99}(1-u) ~\right\}_{0}^{1} & (1)\\
    &=& \displaystyle \left(~ \frac{u^{100}}{100} - \frac{u^{101}}{101} \frac{}{} ~\right)_{0}^{1}\\
    &=& \displaystyle \frac{1}{10100}\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& 1-x \\ du &=& -dx \end{array} \right.$

## Ejercicio 16

$$
\int_{0}^{\pi/2} \frac{\sin(4x)}{\sin(x)}  dx
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2 \left\{~ \frac{2\sin(2x)\cos(2x)}{\sin(x)} ~\right\}_{0}^{\pi/2} & (1)\\
    &=& \displaystyle 4 \left\{~ \frac{\sin(x)\cos(x)\cos(2x)}{\sin(x)} ~\right\}_{0}^{\pi/2} & (1)\\
    &=& \displaystyle 4 \left\{~ \cos(x)\cos(2x) ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle 2 \left\{~ \cos(x) + \cos(3x) ~\right\}_{0}^{\pi/2} & (2)\\
    &=& \displaystyle 2 \left(~ \sin(x) + \frac{\sin(3x)}{3} ~\right)_{0}^{\pi/2}\\
    &=& \displaystyle \frac{4}{3}
\end{array}
$$

- (1): $\sin(2\theta) = 2 \sin(\theta)\cos(\theta)$

- (2): $2\cos(\alpha)\cos(\beta) = \cos(\alpha - \beta) + \cos(\alpha + \beta)$

## Ejercicio 17

$$
\int \frac{x^{-\frac{1}{2}}}{1 + x^{\frac{1}{3}}}  dx
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 6 \left\{~ \frac{t^2}{1+t^2} ~\right\} & (1)\\
    &=& \displaystyle 6 \left(~ t - \arctan(t) ~\right) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^6 \\ dx &=& 6t^5 ~dt \end{array} \right.$

## Ejercicio 18

$$
\int \frac{dx}{\sqrt{2x^2 - 1}}
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1}{\sqrt{(\sqrt{2}x)^2 - 1}} ~\right\} \\
    &=& \displaystyle \frac{1}{\sqrt{2}} \left\{~ \frac{\sec(\theta)\tan(\theta)}{|\tan(\theta)|} ~\right\} & (1)\\
    &=& \displaystyle \frac{1}{\sqrt{2}} \left\{~ \sec(\theta) ~\right\} & (2)\\
    &=& \displaystyle \frac{1}{\sqrt{2}} \ln|\sec(\theta) + \tan(\theta)| + C\\
    &=& \displaystyle \frac{1}{\sqrt{2}} \ln \left| \sqrt{2}x + \sqrt{2x^2-1} \right| + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} \sqrt{2}x &=& \sec(\theta) \\ \sqrt{2}dx &=& \sec(\theta)\tan(\theta) ~dt \end{array} \right.$

- (2): Dado que $2x^2 -1 >0$, entonces podemos concluir que $|\sec(\theta)| > 1$, en la sustitución $(1)$ se puede tomar a $\theta  \in (0,\pi/2) \cup (\pi/2, 3\pi/2)$. Así si $\tan(\theta) < 0$, entonces $\sec(\theta) < 0$ y $\frac{\sec(\theta)\tan(\theta)}{|\tan(\theta)|} = |\sec(\theta)|$. Si $\tan(\theta) > 0$, entonces $\sec(\theta) > 0$ y $\frac{\sec(\theta)\tan(\theta)}{|\tan(\theta)|} = |\sec(\theta)|$.

## Ejercicio 19

$$
\int \frac{dx}{\sqrt{e^x - 1}}
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle -2 \left\{~ \frac{e^t}{\sqrt{1 - e^{2t}}} ~\right\} & (1)\\
    &=& \displaystyle -2 \left\{~ \frac{1}{\sqrt{1 - u^2}} ~\right\} & (2)\\
    &=& -2 \arcsin(u) + C
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& -2t \\ dx &=& -2~dt \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} u &=& e^t \\ du &=& e^t~dt \end{array} \right.$

## Ejercicio 20

$$
\int \frac{x}{x^4 + 4}  dx
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2} \left\{~ \frac{1}{u^2+4} ~\right\} & (1)\\
    &=& \displaystyle \frac{1}{8} \left\{~ \frac{1}{(u/2)^2+1} ~\right\}\\
    &=& \displaystyle \frac{1}{4} \arctan(u/2) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& x^2 \\ du &=& 2x~dx \end{array} \right.$

## Ejercicio 21

$$
\int \frac{2  dx}{(\cos(x) - \sin(x))^2}
$$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2 \left\{~ \frac{(\cos(x)+\sin(x))^2 - 2\sin(x) \cos(x)}{(\cos(x)-\sin(x))^2} ~\right\} & (1)\\
    &=& \displaystyle 2 \left\{~ \left( \frac{\cos(x)+\sin(x)}{\cos(x)-\sin(x)} \right)^2  - \frac{2\sin(x)\cos(x)}{1 - 2 \sin(x)\cos(x)}~\right\} & (1)\\
    &=& \displaystyle 2 \left\{~ \left(~ \tan(\pi/4 + x) ~\right)^2  - \frac{2\sin(x)\cos(x)}{1 - 2 \sin(x)\cos(x)}~\right\} & (2)\\
    &=& \displaystyle 2 \left\{~ \sec^2(\pi/4 + x) - 1  - \frac{2\sin(x)\cos(x)}{1 - 2 \sin(x)\cos(x)}~\right\} & (3)\\
    &=& \displaystyle 2 \left\{~ \sec^2(\pi/4 + x) - \frac{1}{1 - 2 \sin(x)\cos(x)}~\right\}\\
    &=& \displaystyle 2 \left\{~ \sec^2(\pi/4 + x) ~\right\} - I & (2)\\ \\
    I &=& \tan(\pi/4+x) + C
\end{array}
$$

- (1): $(\cos(x) \pm \sin(x))^2 = 1 \pm 2\sin(x)\cos(x)$

- (2): $\tan(\pi/4 + x) = \frac{\cos(x)+\sin(x)}{\cos(x)-\sin(x)} = \frac{1+\tan(x)}{1-\tan(x)}$

- (3): $\tan^2(x) + 1 = \sec^2(x)$

## Ejercicio 22

$$
\int \frac{x \cosh(x)}{\sinh(x)^2}   dx
$$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle -x\text{csch}(x) + \left\{~ \text{csch}(x) ~\right\} & (1)\\
    &=& \displaystyle -x\text{csch}(x) + \left\{~ \frac{\text{csch}(x) (~ \text{csch}(x) + \text{coth}(x)~) }{\text{csch}(x) + \text{coth}(x)} ~\right\}\\
    &=& \displaystyle -x\text{csch}(x) - \ln |\text{csch(x) + \text{coth(x)}}| + C & (2)\\
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ x & \frac{\cosh(x)}{\sinh^2(x)} \\ 1 & -\text{csch}(x) \end{array}$ ver nota $(2)$

- (2): $[\text{csch(x) + \text{coth(x)}}] = - \text{csch}(x)\text{coth}(x) - \text{csch}^2(x) = -\text{csch}(x) (~ \text{csch}(x) + \text{coth}(x)~)$

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

## Ejercicio 23

$$
\int_0^2 x^5 \sqrt{1 + x^3}  dx
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{3}\left\{~(t-1) t^{1/2}~\right\}_{1}^{9} & (1)\\
    &=& \displaystyle \frac{1}{3}\left\{~ t^{3/2} - t^{1/2}~\right\}_{1}^{9}\\
    &=& \displaystyle \frac{1}{3}\left(~ t^{5/2}\frac{2}{5} - t^{3/2}\frac{2}{3}~\right)_{1}^{9}\\
    &=& \displaystyle \frac{1192}{45}
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} t &=& x^3 + 1 \\ dt &=& 3x^2~dx \end{array} \right.$

## Ejercicio 24

$$
\int_0^1 \frac{x^7 - 1}{\log(x)}  dx
$$

$$\textcolor{red}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I(a) &=& \displaystyle \int_{0}^{1} \frac{x^{a}-1}{\ln(x)} ~ dx\\
    \displaystyle \frac{d}{da}I(a) &=& \displaystyle \int_{0}^{1} \frac{\partial}{\partial a} \left(\frac{x^{a}-1}{\ln(x)} \right) ~ dx & (1)\\
    &=& \displaystyle \int_{0}^{1} x^a ~ dx\\
    &=& \displaystyle  \frac{1}{a+1}\\ \\
    I(a) &=& \displaystyle  \int \frac{1}{a+1} ~da + C\\ \\
    &=& \displaystyle  \ln(a+1) + C\\ \\
    I(0) &=& 0\\
    &=& 0 + C\\
    C &=& 0\\ \\
    I(a) &=& \ln(a+1)
\end{array}
$$

- (1): Demostración Regla de Leibniz para derivadas parciales <https://math.stackexchange.com/questions/3778739/can-i-replace-the-fracddt-with-frac-partial-partial-t-in-the-leibn?rq=1>

$$\textcolor{red}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I(a) &=& \displaystyle \int_{0}^{1} \frac{x^{a}-1}{\ln(x)} ~ dx\\
    &=& \displaystyle \int_{0}^{1} \int_{0}^{a} x^y ~dy ~ dx & (1)\\
    &=& \displaystyle \int_{0}^{a} \int_{0}^{1} x^y ~dx ~ dy & (2)\\
    &=& \displaystyle \int_{0}^{a} \left( \frac{x^{y+1}}{y+1} \right)_{0}^{1} ~ dy\\
    &=& \displaystyle \int_{0}^{a} \frac{1}{y+1} ~ dy\\
    &=& \displaystyle \left( \ln |y+1| \right)_{0}^{a}\\
    &=& \displaystyle \ln |a+1|\\
\end{array}
$$

- (1): $\frac{\partial}{\partial y} \left( \frac{x^{y}-1}{\ln(x)} \right) = x^y$

- (2): Teorema de Fubini

## Ejercicio 25

$$
\int \sqrt{\csc(x) - \sin(x)}  dx
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\cos(x)}{\sqrt{\sin(x)}} ~\right\} \\
    &=& \displaystyle 2\sqrt{\sin(x)} + C \\
\end{array}
$$

- (1): $[\sqrt{f(x)}] = \frac{1}{2} \frac{f'(x)}{\sqrt{f(x)}}$
