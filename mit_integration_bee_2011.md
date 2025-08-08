# MIT integration bee - 2011

## Notación y Consideraciones Generales

A lo largo del docuemnto vamos a utilizar la siguiente notación:

$$
\{~f(x)~\}_{a}^{b}:= \int_{a}^{b} f(x) ~dx ~~,~~ [~f(x)~]:= \frac{d}{dx}f(x)
$$

Recursos obtenidos de: <https://math.mit.edu/~yyao1/integrationbee.html>

Herramientas que te pueden ser útiles:

- Calculadora gráfica: <https://www.desmos.com/calculator?lang=es>
- Calculadora de integrales: <https://mathdf.com/es/>
- Calculadore de integrales: <https://www.wolframalpha.com/>
- Te ayuda con ideas: <https://chat.deepseek.com>

## Ejercicio 1

$$  
\int \frac{x^6 - 1}{x^4 + x^3 - x - 1}  dx  
$$  

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \{~ x^2 - x + 1 ~\}\\
    &=& \displaystyle \frac{x^3}{3} - \frac{x^2}{2} + x +C\\
\end{array}
$$

**Nota:**

1. Si tenemos una funcion racional $\frac{p(x)}{q(x)}$ donde $\deg p(x) \geq \deg q(x)$, entonces por el algoritmo de la división para polinomios tenemos que  $p(x) = s(t)q(x) + r(x)$ donde $\deg r(x) < \deg q(x)$.

## Ejercicio 2

$$  
\int \left( 2 \ln x + (\ln x)^2 \right)  dx  
$$  

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \{~ 2t e^t + t^2 e^t ~\} & (1)\\
    &=& \displaystyle \{~ 2t e^t + t^2 e^t ~\} & (1)\\
    &=& t^2 e^t + C & (2)
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& e^t \\ dx &=& e^t dt \end{array} \right.$

- (2): $[e^tf(t)] = e^t(f(t) + f'(t))$

## Ejercicio 3

$$  
\int \frac{2x}{\sqrt{1 - x^4}}  dx  
$$  

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1}{\sqrt{1-t^2}} ~\right\} & (1)\\
    &=& \arcsin(t) + C
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} t &=& x^2 \\ dt &=& 2x dx \end{array} \right.$

## Ejercicio 4

$$  
\int \frac{x^2 + 1}{x + 1}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ x -1 + \frac{2}{x+1} ~\right\}\\
    &=& \displaystyle \frac{x^2}{2} - x + 2 \ln|x+1| + C\\
\end{array}
$$

## Ejercicio 5

$$  
\int \frac{\sin(x)^3 + \sin(x)^2 - 2\sin(x) - 2}{\sin(x)^2 + 2\sin(x) + 1}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sin(x) - 1 - \frac{\sin(x)+1}{\sin^2(x) + 2\sin(x) + 1} ~\right\} & (1)\\
    &=& \displaystyle \left\{~ \sin(x) - 1 - \frac{1}{\sin(x)+1} ~\right\}\\ \\

    I_1 &=& \displaystyle \left\{~ \sin(x) - 1 ~\right\}\\
    &=& \displaystyle -\cos(x) - x\\ \\

    I_2 &=& \displaystyle \left\{~ \frac{1}{\sin(x)+1} ~\right\}\\
    &=& \displaystyle \left\{~ \frac{\sec(x)(~\tan(x) + \sec(x)~) }{(~\tan(x) + \sec(x)~)^2} ~\right\}\\
    &=& \displaystyle \left\{~ \frac{1}{t^2} ~\right\} & (2)\\
    &=& \displaystyle -\frac{1}{t}\\ \\

    I &=& \displaystyle \frac{1}{\tan(x) + \sec(x)} -\cos(x) - x  + C
\end{array}
$$

- (1): Hacer una división de polinomios con la variable $t = \sin(x)$

- (2): $\left\{\begin{array}{rcl} t &=& \tan(x) + \sec(x) \\ dt &=&  \sec(x)(~\tan(x) + \sec(x)~) dx \end{array} \right.$

## Ejercicio 6

$$  
\int \sinh(x)^{-2}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle  \left\{~ \text{csch}^2(x) ~\right\}\\
    &=& \displaystyle  -\text{coth}(x) + C \\
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
        [\text{sech}(x)] &=& \text{csch}(x)\\
        [\text{csch}(x)] &=& \text{sech}(x)\\
    \end{array}
    \right.
    $$

## Ejercicio 7

$$  
\int \sec^4 x \tan^2 x  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle  \left\{~ \tan^2(x)(1+ \tan^2(x))\sec^2(x) ~\right\}\\
    &=& \displaystyle  \left\{~ u^2(1+ u^2)~\right\} & (1)\\
    &=& \displaystyle  \frac{u^3}{3} + \frac{u^5}{5} + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& \tan^2(x)\\ du &=&  \sec^2(x)dx \end{array} \right.$

## Ejercicio 8

$$  
\int \sqrt{\csc x - \sin x}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle  \left\{~ \frac{|\cos(x)|}{\sqrt{\sin(x)}} ~\right\}\\
    &=& \displaystyle  \pm \left\{~ \frac{\cos(x)}{\sqrt{\sin(x)}} ~\right\}\\
    &=& \pm 2\sqrt{\sin(x)} + C & (2)
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& \tan^2(x)\\ du &=&  \sec^2(x)dx \end{array} \right.$

- (2): $\displaystyle [\sqrt{f(x)}] = \frac{1}{2} \frac{f'(x)}{\sqrt{f(x)}}$

## Ejercicio 9

$$  
\int \cos^6 x  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle  \frac{1}{8} \left\{~ (\cos(2x) +  1)^3 ~\right\} & (1)\\
    &=& \displaystyle  \frac{1}{8} \left\{~ \cos^3(2x) + 3\cos^2(2x) +  3 \cos(2x) + 1 ~\right\}\\
    &=& \displaystyle  \frac{1}{8} \left\{~ -\cos(2x)\sin^2(2x) + 3\cos^2(2x) +  4 \cos(2x) + 1 ~\right\} & (2)\\
    &=& \displaystyle  \frac{1}{8} \left(~ -\frac{\sin^3(2x)}{6} + \frac{3}{2} \left( \frac{\sin(4x)}{4} + x \right) +  2 \sin(2x) + x ~\right) + C & (1) ~\text{y}~ (3)\\
\end{array}
$$

- (1): $\cos(2x) =  2\cos^2(x) - 1$

- (2): $\sin^2(x) + \cos^2(x) = 1$

- (3): $[f^n(x)] = n f^{n-1}(x)f'(x)$

## Ejercicio 10

$$  
\int \frac{1}{1 + 2x^2 + x^4}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1}{(x^2+1)^2} ~\right\}\\
    &=& \displaystyle \left\{~ \cos^2(\theta) ~\right\} &(1)\\
    &=& \displaystyle \frac{1}{2} \left\{~ \cos(2\theta) +  1 ~\right\} & (2)\\
    &=& \displaystyle \frac{1}{2} \left(~ \frac{\sin(2\theta)}{2} +  \theta ~\right)\\
    &=& \displaystyle \frac{1}{2} \left(~ \frac{x}{x^2+1} +  \arctan(x) ~\right) +  C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \tan(\theta)\\ dx &=&  \sec^2(\theta) d\theta \end{array} \right.$

- (2): $\cos(2x) = 2 \cos^2(x) - 1$

## Ejercicio 11

$$  
\int \cos(\log x)  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle x \cos(\ln x) + \left\{~ \sin(\ln x )~\right\} & (1)\\
    &=& \displaystyle x \cos(\ln x) + x\sin(\ln x) - I & (2)\\ \\

    I &=& \displaystyle \frac{x}{2} ~ (\cos(\ln x) + \sin(\ln x)) + C
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \cos(\ln x) & dx \\ -\frac{\sin(\ln x)}{x} & x \end{array}$

- (2): $\begin{array}{|c|c|} D & I \\ \sin(\ln x) & dx \\ \frac{\cos(\ln x)}{x} & x \end{array}$

## Ejercicio 12

$$
\int \frac{1}{\cos x}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sec(x)~\right\}\\
    &=& \displaystyle \ln |\tan(x)+ \sec(x)| +  C & (1)\\
\end{array}
$$

- (1): $[\tan(x) + \sec(x)] = \sec(x) (\tan(x)+\sec(x))$

## Ejercicio 13

$$  
\int \frac{1}{9 \cos^2 x + 4 \sin^2 x}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\sec^2(x)}{9 + 4 \tan^2(x)} ~\right\}\\
    &=& \displaystyle \left\{~ \frac{1}{9 + 4 u^2} ~\right\} & (1)\\
    &=& \displaystyle \frac{1}{9}\left\{~ \frac{1}{1 + \frac{4}{9} u^2} ~\right\}\\
    &=& \displaystyle \frac{1}{6} \arctan \left(\frac{2}{3}u \right) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& \tan(x)\\ du &=&  \sec^2(x) dx \end{array} \right.$

## Ejercicio 14

$$  
\int \frac{1}{x^2 (x^4 + 1)^{3/4}}  dx  
$$ 

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle - \left\{~ \frac{t^3}{(t^4+1)^{3/4}} ~\right\} & (1)\\
    &=& \displaystyle - \frac{1}{4} \left\{~ \frac{1}{u^{3/4}} ~\right\} & (2)\\
    &=& \displaystyle - u^{1/4} + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \frac{1}{t} \\ dx &=& -\frac{1}{t^2} dt \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} u &=& t^4 + 1 \\ du &=& 4t^3  dt \end{array} \right.$

## Ejercicio 15

$$  
\int_0^\pi \cos x \cos 3x \cos 5x  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2} \left\{~ \cos(x)(\cos(8x) + \cos(2x)) ~\right\}_{0}^{\pi} & (1)\\
    &=& \displaystyle \frac{1}{4} \left\{~ \cos(9x) + \cos(7x) + \cos(3x) + \cos(x) ~\right\}_{0}^{\pi} & (1)\\
    &=& \displaystyle \frac{1}{4} \left(~ \frac{\sin(9x)}{9} + \frac{\sin(7x)}{7} + \frac{\sin(3x)}{3} + \sin(x)  ~\right)_{0}^{\pi}\\
    &=& \displaystyle 0 \\
\end{array}
$$

- (1): $2 \cos(a)\cos(b) = \cos(a+b) + \cos(a-b)$

**Nota:**

1. Una forma mas facil de resolver la integral es ver que si $f$ es una función impar, entonces:

    $$
    \left\{ f(x) \right\}_{-a}^{a} = 0
    $$

2. Resolver el límite-integral:

    $$
    \lim_{n \to \infty} \left\{\prod_{i=1}^{n} \cos(nx) \right\}_{0}^{\pi}
    $$

## Ejercicio 16

$$  
\int \left( \frac{1}{\log x} + \log(\log x) \right)  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle x \left( \frac{1}{\ln x} + \ln(\ln x) \right) - \left\{~ \frac{\ln(x) - 1}{\ln^2(x)} ~\right\} & (1)\\
    &=& \displaystyle x \left( \frac{1}{\ln x} + \ln(\ln x) \right) - \frac{x}{\ln(x)} + C & (2)\\
    &=& \displaystyle x \ln(\ln x) + C \\
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \frac{1}{\log x} + \log(\log x) & dx \\ \frac{1}{x}\left(\frac{\ln(x) - 1}{\ln^2(x)} \right) & x \end{array}$

- (2): $\left[\frac{f(x)}{\ln(x)} \right] = \frac{f'(x)\ln(x) - f(x)\frac{1}{x}}{\ln^2(x)}$

## Ejercicio 17

$$  
\int \frac{1}{2 + e^x}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle -\left\{~ \frac{e^t}{2e^t + 1} ~\right\} & (1)\\
    &=& \displaystyle -\left\{~ \frac{1}{2u + 1} ~\right\} & (2)\\
    &=& \displaystyle - \frac{\ln (2u+1)}{2} + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& -t \\ dx &=& -dt \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} u &=& e^t \\ du &=& e^t dt \end{array} \right.$

## Ejercicio 18

$$  
\int \sqrt{\frac{x}{1 - x^3}}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2 \left\{~ \frac{t^2}{\sqrt{1 - t^6}} ~\right\} & (1)\\
    &=& \displaystyle \frac{2}{3} \left\{~ \frac{1}{\sqrt{1 - u^2}} ~\right\} & (2)\\
    &=& \displaystyle \frac{2}{3} \arcsin(u) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^2 \\ dx &=& 2t dt \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} u &=& t^3 \\ du &=& 3t^2 dt \end{array} \right.$

## Ejercicio 19

$$  
\int \frac{4x}{1 - x^4}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle  2 \left\{~ \frac{1}{1 - t^2} ~\right\} & (1)\\
    &=& \displaystyle \left\{~ \frac{1}{1 - t} + \frac{1}{1 + t} ~\right\}\\
    &=& \displaystyle \ln(1+t) - \ln(1-t) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} t &=& x^2 \\ dt &=& 2x dx \end{array} \right.$

## Ejercicio 20

$$  
\int x^x (1 + \log x)  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle  x^x + C & (1)\\
\end{array}
$$

- (1): $[x^x] = [e^{x \ln(x)}] = x^x(1+ \ln(x))$

## Ejercicio 21

$$  
\int_0^6 \sqrt{6x - x^2}  dx  
$$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

Sea $y = \sqrt{6x-x^2}$, entonces:

$$
(x-3)^2 + y^2 = 9 ~~,~~ \text{ para $y \geq 0$}
$$

Así pues, la integral esta calculando el área de media circunferencia de radio $3$ centrada en el punto $(3,0)$.

$$
I = \frac{9}{2} \pi
$$

## Ejercicio 22

$$  
\int \sin(101x) \sin^{99}(x)  dx  
$$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sin((\alpha+1)x) ~ \sin^{\alpha-1}(x) ~\right\}\\
    &=& \displaystyle \frac{\sin^{\alpha}\sin(\alpha x)}{\alpha} + C
\end{array}
$$

- (1):

    $$
    \begin{array}{rclr}
        [\sin^{\alpha}(x) \sin(\alpha x)] &=& \alpha \sin^{\alpha-1}(x)\cos(x)\sin(\alpha x) + \alpha \cos(\alpha)\sin^{\alpha}(x)\\
        &=& \alpha \sin^{\alpha-1}(x) (~ \cos(x)\sin(\alpha x) + \cos(\alpha)\sin(x) ~)\\
        &=& \alpha \sin^{\alpha-1}(x) \sin((\alpha +1)x)\\
    \end{array}
    $$

## Ejercicio 23

$$  
\int x e^{e^{x^2} + x^2}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ x e^{e^{x^2}} e^{x^2} ~\right\}\\
    &=& \displaystyle \left\{~ x e^{e^{x^2}} e^{x^2} ~\right\}\\
    &=& \displaystyle \frac{e^{e^{x^2}}}{2} + C\\
\end{array}
$$

- (1): $\left[e^{e^{x^2}}\right] = 2xe^{e^{x^2}}e^{x^2}$

## Ejercicio 24

$$
\int_0^1 \frac{x^3 - 3x^2 + 3x - 1}{x^4 + 4x^3 + 6x^2 + 4x + 1}  dx
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{(x-1)^3}{(x+1)^4} ~\right\}_{0}^{1} & (1)\\
    &=& \displaystyle \left\{~ \frac{(t-2)^3}{t^4} ~\right\}_{1}^{2} & (2)\\
    &=& \displaystyle \left\{~ t^{-1} - 6t^{-2} + 12t^{-3} - 8t^{-4} ~\right\} _{1}^{2}\\
    &=& \displaystyle \left(~ \ln |t| + \frac{6}{t} - \frac{6}{t^{2}} + \frac{8}{3}\frac{1}{t^3} ~\right)_{1}^{2}\\
    &=& \displaystyle \ln(2) - \frac{5}{6}
\end{array}
$$

- (1): Triángulo de Pascal

- (2): $\left\{\begin{array}{rcl} t &=& x+1 \\ dt &=& dx \end{array} \right.$

## Ejercicio 25

$$
\int \sqrt{\frac{1-x}{1+x}}  dx 
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1-x}{\sqrt{1-x^2}} ~\right\}\\
    &=& \displaystyle \left\{~ \frac{1}{\sqrt{1-x^2}} - \frac{x}{\sqrt{1-x^2}} ~\right\}\\ \\

    I_1 &=& \displaystyle \left\{~ \frac{1}{\sqrt{1-x^2}} ~\right\}\\
    &=& \displaystyle \arcsin(x)\\ \\

    I_2 &=& \displaystyle \left\{~ \frac{x}{\sqrt{1-x^2}} ~\right\}\\
    &=& \displaystyle \frac{1}{2}\left\{~ \frac{1}{\sqrt{1-t}} ~\right\}\\
    &=& \displaystyle -\sqrt{1-t}\\
    &=& \displaystyle -\sqrt{1-x^2}\\ \\

    I &=& \displaystyle \arcsin(x) + \sqrt{1-x^2} + C
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} t &=& x^2 \\ dt &=& 2x ~dx \end{array} \right.$