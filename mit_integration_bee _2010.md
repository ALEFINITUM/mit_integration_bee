# MIT integration bee - 2010

## Notación y Consideraciones Generales

A lo largo del docuemnto vamos a utilizar la siguiente notación:

$$
\{~f(x)~\}_{a}^{b}:= \int_{a}^{b} f(x) ~dx ~~,~~ [~f(x)~]:= \frac{d}{dx}f(x)
$$

Recursos obtenidos de: <https://math.mit.edu/~yyao1/integrationbee.html>

Herramientas que te pueden ser útiles:

- Calculadora gráfica: <https://www.desmos.com/calculator?lang=es>
- Calculadora de integrales: <https://mathdf.com/es/>
- Te ayuda con ideas: <https://chat.deepseek.com>

## Ejercicio 1

$$  
\int_{0}^{\pi/2} \sin(x) \sin(2x) \sin(3x)  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \{~ \sin(x) \sin(2x) \sin(3x) ~\}_{0}^{\pi/2}\\
    &=& \displaystyle \frac{1}{2} \{~ \sin(x) (\cos(x) - \cos(5x)) ~\}_{0}^{\pi/2} & (1)\\
    &=& \displaystyle \frac{1}{2} \left(\{~ \sin(x)\cos(x) ~\}_{0}^{\pi/2} - \{~ \sin(x) \cos(5x) ~\}_{0}^{\pi/2} \right) \\
    &=& \displaystyle \frac{1}{2} \left( \left(\frac{\sin^2(x)}{2} \right)_{0}^{\pi/2} - \{~ \sin(x) \cos(5x) ~\}_{0}^{\pi/2} \right) \\
    &=& \displaystyle \frac{1}{2} \left( \frac{1}{2} - \{~ \sin(x) \cos(5x) ~\}_{0}^{\pi/2} \right) \\
    &=& \displaystyle \frac{1}{2} \left( \frac{1}{2} - \frac{1}{2}\{~ \sin(6x) - \sin(4x) ~\}_{0}^{\pi/2} \right) & (2)\\
    &=& \displaystyle \frac{1}{2} \left( \frac{1}{2} - \frac{1}{2} \left(~ -\frac{\cos(6x)}{6} + \frac{\cos(4x)}{4} \right)_{0}^{\pi/2} \right) \\
    &=& \displaystyle \frac{1}{2} \left( \frac{1}{2} - \frac{1}{2} \left(~  \frac{2}{6}\right)\right) \\
    &=& \displaystyle \frac{1}{6}
\end{array}
$$

- (1): $\sin(x)\sin(y) = \frac{1}{2} (\cos(x - y) - \cos(x + y))$

- (2): $\sin(x)\cos(y) = \frac{1}{2} (\sin(x - y) + \sin(x + y))$ y $\sin(-x) = - \sin(x)$

## Ejercicio 2

$$  
\int_{0}^{\pi/2} \sin^3(2x) \cos(x)  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \{~ \sin^3(2x) \cos(x) ~\}_{0}^{\pi/2}\\
    &=& \displaystyle \{~ \sin^3(2x) \cos(x) ~\}_{0}^{\pi/2}\\
    &=& \displaystyle \{~ (2\sin(x)\cos(x))^3 \cos(x) ~\}_{0}^{\pi/2} & (1)\\
    &=& \displaystyle 8 \{~ \sin^3(x) \cos^4(x) ~\}_{0}^{\pi/2} & (1)\\
    &=& \displaystyle -8 \{~ (1-t^2) t^4 ~\}_{1}^{0} & (2)\\
    &=& \displaystyle 8 \{~ (1-t^2) t^4 ~\}_{0}^{1} & (3)\\
    &=& \displaystyle 8 \left(~ \frac{t^5}{5} - \frac{t^7}{7} \frac{}{} ~\right)_{0}^{1}\\
    &=& \displaystyle \frac{16}{35}\\
\end{array}
$$

- (1): $\sin(2x) = 2 \sin(x)\cos(x)$

- (2): $ \left\{\begin{array}{rcl} t &=& \cos(x)\\ dt &=& -\sin(x) dx \end{array} \right.$ y $\cos^2(x) + \sin^2(x) = 1$

- (3): $\int_{a}^{b} f(x) dx = -\int_{b}^{a} f(x) dx $

## Ejercicio 3

$$  
\int (x+1)^2 (x-1)^{1/3}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \{~ (t+2)^{2} ~ t^{1/3} ~\}\\
    &=& \displaystyle \{~ (t^2 + 4t + 4) ~ t^{1/3} ~\}\\
    &=& \displaystyle \frac{t^{10/3}}{10/3} + 4 \frac{t^{7/3}}{7/3} + 4\frac{t^{4/3}}{4/3} \\
    &=& \displaystyle 3t^{4/3} \left( \frac{t^2}{10} + \frac{4t}{7} + 1 \right) + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} t &=& x-1\\ dt &=& dx \end{array} \right.$

## Ejercicio 4

$$  
\int x \log \left( 1 + \frac{1}{x} \right) dx  
$$  

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{x^2 \log(1+1/x)}{2}  + \frac{1}{2} \left\{~ \frac{x}{x+1} ~\right\} & (1)\\
    &=& \displaystyle \frac{x^2 \log(1+1/x)}{2}  + \frac{1}{2} \left(~  x - \ln(x+1) ~\right) + C\\
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \log(1+1/x) & x \\ \frac{x}{1+x}(-\frac{1}{x^2}) & \frac{x^2}{2} \end{array}$

## Ejercicio 5

$$  
\int_0^1 \sin^2 (\log x)  dx  
$$  

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I_1 &=& \displaystyle (~ x~\sin^2(\log(x)) ~)_{0}^{1} - \left\{~ \sin(2 \log(x)) ~\right\}_{0}^{1} & (1)\\
    &=& - \left\{~ \sin(2 \log(x)) ~\right\}_{0}^{1}\\ \\

    I_2 &=& \left\{~ \sin(2 \log(x)) ~\right\}_{0}^{1} & (2)\\
    &=& (~ x~\sin(2\log(x)) ~)_{0}^{1} - 2 \left\{~ \cos(2 \log(x)) ~\right\}_{0}^{1} \\
    &=& - 2 \left\{~ \cos(2 \log(x)) ~\right\}_{0}^{1} \\
    &=& -2 (~ x~\cos(2\log(x)) ~)_{0}^{1} - 4 I_2 & (3)\\
    &=& -2 - 4 I_2 \\
    I_2 &=& -\frac{2}{5}\\ \\

    I_1 &=& \frac{2}{5}
\end{array}
$$

- (1): $\begin{array}{|c|c|} D & I \\ \sin^2(\log(x)) & 1 \\ \frac{\sin(2\log(x))}{x} & x \end{array}$

- (2): $\begin{array}{|c|c|} D & I \\ \sin(2\log(x)) & 1 \\ \frac{2~\cos(2 \log(x))}{x} & x \end{array}$

- (3): $\begin{array}{|c|c|} D & I \\ \cos(2\log(x)) & 1 \\ -\frac{2~\sin(2 \log(x))}{x} & x \end{array}$

## Ejercicio 6

$$  
\int \frac{1}{1 + 3e^x}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1}{1+3t} \cdot\frac{1}{t} ~\right\} & (1)\\
    &=& \displaystyle \left\{~ -\frac{3}{1+3t} + \frac{1}{t} ~\right\}\\
    &=& \displaystyle -\ln(1+3t) + \ln(t) +  C\\
    &=& \displaystyle \ln \left( \frac{t}{1 + 3t} \right) +  C
\end{array}
$$

- (1): $ \left\{\begin{array}{rcl} t &=& e^x \\ dt &=& e^x dx \end{array} \right.$

## Ejercicio 7

$$  
\int_{\pi/4}^{\pi/3} \frac{1}{\sin^3 x \cos^5 x}  dx  
$$  

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\sin^2(x) + \cos^2(x)}{\sin^3(x) \cos^5(x)} ~\right\}_{\pi/4}^{\pi/3} & (1)\\
    &=& \displaystyle \left\{~ \frac{1}{\sin(x) \cos^5 (x)} + \frac{1}{\sin^3 (x) \cos^3 (x)} ~\right\}_{\pi/4}^{\pi/3} & (1)\\
    &=& \displaystyle \left\{~  \frac{\sin(x)}{\cos^5 (x)} + \frac{1}{\sin(x) \cos^3 (x)} + \frac{1}{\sin^3 (x) \cos^3 (x)} ~\right\}_{\pi/4}^{\pi/3} & (1)\\
    &=& \displaystyle \left\{~  \tan(x)\sec^4(x) + 2 \frac{1}{\sin(x) \cos^3 (x)} + \frac{1}{\sin^3 (x) \cos(x)} ~\right\}_{\pi/4}^{\pi/3} & (1)\\
    &=& \displaystyle \left\{~  \tan(x)\sec^4(x) + 2 \left( \frac{\sin(x)}{\cos^3 (x)} + \frac{1}{\sin(x) \cos (x)} \right) + \frac{1}{\sin(x) \cos(x)} +\frac{\cos(x)}{\sin^3 (x)} ~\right\}_{\pi/4}^{\pi/3} & (1)\\
    &=& \displaystyle \left\{~  \tan(x)\sec^4(x) + 2 \tan(x) \sec^2(x) + 3 \frac{1}{\sin(x) \cos (x)} + \cot(x)\csc^2(x) ~\right\}_{\pi/4}^{\pi/3}\\
    &=& \displaystyle \left\{~  \tan(x)\sec^4(x) + 2 \tan(x) \sec^2(x) + 3 \left( \tan(x) + \cot(x) \right) + \cot(x)\csc^2(x) ~\right\}_{\pi/4}^{\pi/3} & (1)\\
    &=& \displaystyle \left( \frac{\tan^2(x)}{2} + \frac{\tan^4(x)}{4} \right)_{\pi/4}^{\pi/3} +  2 \left( \frac{\tan^2(x)}{2}\right)_{\pi/4}^{\pi/3} + 3 \left(~ - \ln(\cos(x)) + \ln(\sin(x)) ~\right)_{\pi/4}^{\pi/3} - \left( \frac{\cot^2(x)}{2}\right)_{\pi/4}^{\pi/3}\\
    &=& \frac{16}{3} + \frac{3}{2} \ln(3)
\end{array}
$$

- (1): $\cos^2(x) + \sin^2(x) = 1$

**Nota:**

1. Tenemos la siguiente fórmula de reducción de potencias:

    $$
    \cos^n(\theta) = 2^{-n} ~~ \sum_{k=0}^{n} \binom{n}{k} \cos(~(2k-n) \theta~)
    $$

2. Estudiar la integral $I(n,m) = \left\{\frac{1}{\sin^n(\theta) \cos^m(\theta)} \right\}$ mediante la siguiente recursión:

    $$
    I(n,m) = I(n-2,m) + I(n,m-2) ~~,~~ \text{para } n,m \geq 2
    $$

    Utilizando el metodo de series formales, es decir, estudiando la serie formal en dos variables:

    $$
    \sum_{n,m \geq 0} x^n y^m I(n,m)
    $$

## Ejercicio 8

$$  
\int_1^\infty \frac{1}{x \sqrt{x^4 - 1}}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \frac{1}{2}\left\{~ \frac{\tan \theta}{|\tan \theta|} ~\right\}_{0}^{\pi/2} & (1)\\
    &=& \displaystyle \frac{\pi}{4} & (2)\\
\end{array}
$$

- (1): $ \left\{\begin{array}{rcl} x^2 &=& \sec \theta \\ 2x~dx &=& \sec \theta ~ \tan \theta ~dx \end{array} \right.$, $1 + \tan^2 \theta = \sec^2 \theta$

- (2): $\tan \theta \geq 0$ para todo $\theta \in [0, \pi/2)$

**Nota:**

1. Al hacer sustituciones debemos de asegurarnos que en el intervalo de integración la sustitución sea una biyección.

## Ejercicio 9

$$  
\int \frac{1}{x(x^5 + 1)}  dx  
$$  

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle -\left\{~ \frac{t^4}{t^5 + 1} ~\right\}\\
    &=& \displaystyle - \frac{\ln(t^5+1)}{5} + C
\end{array}
$$

- (1): $ \left\{\begin{array}{rcl} x &=& \frac{1}{t} \\ dx &=& -\frac{1}{t^2} ~dt \end{array} \right.$

## Ejercicio 10

$$  
\int_{0}^{\pi/2} \sqrt{\tan (x)}  ~dx  
$$

$$\textcolor{red}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sqrt{\cot (x)}  ~\right\}_{0}^{\pi/2} & (1) \\ \\

    2 I &=& \displaystyle \left\{~ \sqrt{\tan x} + \sqrt{\cot x}  ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle  \left\{~ \frac{\cos x + \sin x}{\sqrt{\sin(x) \cos(x)}} ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle  \sqrt{2} \left\{~ \frac{\cos x + \sin x}{\sqrt{1 - (\sin(x)-\cos(x))^2} } ~\right\}_{0}^{\pi/2} & (2)\\
    &=& \displaystyle - \sqrt{2} \left\{~ \frac{1}{\sqrt{1 - t^2} } ~\right\}_{-1}^{1} & (3)\\
    &=& \displaystyle - \sqrt{2} \left(~ \arcsin(t) ~\right)_{-1}^{1} & (4)\\
    &=& \displaystyle \sqrt{2} \pi & (4)\\ \\

    I &=& \frac{\pi}{\sqrt{2}}
\end{array}
$$

- (1): $ \left\{\begin{array}{rcl} x &=& \pi/2 - \theta \\ dx &=& -dt \end{array} \right.$, $\sin(\pi/2 - x) = \cos(x)$ y $\cos(\pi/2 - x) = \sin(x)$

- (2): $(\sin(x) - \cos(x))^2 = 1 - 2 \sin(x) \cos(x)$

- (3): $ \left\{\begin{array}{rcl} t &=& \sin(x)-\cos(x) \\ dt &=& (\cos(x) + \sin(x) )~dx \end{array} \right.$

- (4): $[\arcsin(t)] = \frac{1}{\sqrt{1-t^2}}$

**Nota:**

1. Tener cuidado al usar integrales indefinidas pues debemos de determinar sobre que intervalo queremos encontrar la antiderivada.

    Supongamos que $x \in (0, \pi/4)$, entonces si queremos de terminar una antiderivada de:

    $$
    I = \left\{~ \sqrt{\tan (x)} ~\right\} = -\left\{~ \sqrt{\cot (\theta)} ~\right\}
    $$

    Sin embargo, al hacer esta sustitución el intervalo de definición de $\theta \in (\pi/2, \pi/4)$ y tenemos que:

    $$
    \textcolor{red}{2I \ne \left\{~ \sqrt{\tan (x)} - \sqrt{\cot (\theta)} ~\right\}}
    $$

2. bibliografia interesante:

    - <https://www.quora.com/What-is-the-integral-of-sqrt-tan-x-1/answer/Lai-Johnny?ch=17&oid=229121919&share=bbb0ceb7&srid=CCOmo&target_type=answer>

    - <https://math.stackexchange.com/questions/409332/calculus-indefinite-integration-find-int-sqrt-cot-x-sqrt-tan-x-dx?noredirect=1>

## Ejercicio 11

$$  
\int_{0}^{\pi/4} \sqrt{\tan (x)}  ~dx  
$$

$$\textcolor{red}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sqrt{\frac{\cos(\theta) - \sin(\theta)}{\sin(\theta) + \cos(\theta)}}  ~\right\}_{0}^{\pi/4} & (1)\\
    &=& \displaystyle \left\{~ \frac{\cos(\theta) - \sin(\theta)}{\sqrt{\cos^2(\theta) - \sin^2(\theta)}}  ~\right\}_{0}^{\pi/4}\\
    &=& \displaystyle \left\{~ \frac{\cos(\theta)}{\sqrt{\cos^2(\theta) - \sin^2(\theta)}} - \frac{\sin(\theta)}{\sqrt{\cos^2(\theta) - \sin^2(\theta)}}  ~\right\}_{0}^{\pi/4}\\
    &=& \displaystyle \left\{~ \frac{\cos(\theta)}{\sqrt{1 - 2\sin^2(\theta)}} - \frac{\sin(\theta)}{\sqrt{2\cos^2(\theta) - 1}}  ~\right\}_{0}^{\pi/4}\\\\

    I_1 &=& \displaystyle \left\{~ \frac{\cos(\theta)}{\sqrt{1 - 2\sin^2(\theta)}}   ~\right\}_{0}^{\pi/4}\\
    &=& \displaystyle \left\{~ \frac{1}{\sqrt{1 - 2t^2}}   ~\right\}_{0}^{\sqrt{2}/2}\\
    &=& \displaystyle \left(~ \frac{\arcsin(\sqrt{2}t)}{\sqrt{2}} ~\right)_{0}^{\sqrt{2}/2} & (2)\\
    &=& \displaystyle \frac{\pi}{2\sqrt{2}}\\\\

    I_2 &=& \displaystyle \left\{~ \frac{-\sin(\theta)}{\sqrt{2\cos^2(\theta) - 1}}  ~\right\}_{0}^{\pi/4}\\
    &=& \displaystyle \left\{~ \frac{1}{\sqrt{2t^2 - 1}}  ~\right\}_{\sqrt{2}/2}^{1} & (3)\\
    &=& \displaystyle \frac{1}{\sqrt{2}}\left\{~ \frac{\sec(u) \tan(u)}{|\tan (u)|}  ~\right\}_{0}^{\pi/4} & (4)\\
    &=& \displaystyle \frac{1}{\sqrt{2}}\left\{~ \sec(u)  ~\right\}_{0}^{\pi/4} & (5)\\
    &=& \displaystyle \frac{1}{\sqrt{2}}\left(~ \ln(|\tan(u) + \sec(u)|)~\right)_{0}^{\pi/4} & (6)\\
    &=& \displaystyle \displaystyle \frac{\ln(1 + \sqrt{2})}{\sqrt{2}}\\\\

    I &=& \displaystyle  \frac{\pi}{2\sqrt{2}} + \frac{\ln(1 + \sqrt{2})}{\sqrt{2}}\\

\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \pi/4 - \theta \\ dx &=& -d\theta \end{array} \right.$, $\sin(\pi/4 - \theta) = \frac{\sqrt{2}}{2}(\cos(\theta)- \sin(\theta))$ y $\cos(\pi/4 - \theta) = \frac{\sqrt{2}}{2}(\cos(\theta) + \sin(\theta))$

- (2): $\left\{\begin{array}{rcl} t &=& \sin(\theta) \\ dt &=& \cos(\theta)~d\theta \end{array} \right.$

- (3): $\left\{\begin{array}{rcl} t &=& \cos(\theta) \\ dt &=& -\sin(\theta)~d\theta \end{array} \right.$

- (4): $\left\{\begin{array}{rcl} \sqrt{2}t &=& \sec (u) \\ \sqrt{2}~dt &=& \sec(u) \tan(u) ~du \end{array} \right.$

- (5): $\tan (u) \geq 0$ para todo $u \in (0,\pi/2)$

- (6): $\sec(u) = \frac{\sec(u)(\tan(u) + \sec(u))}{\tan(u) + \sec(u)}$ y $\left[ \tan(u) + \sec(u) \right] = \sec(u)(\tan(u) + \sec(u))$

**Nota:**

1. Para diferentes intervalos de integración tenemos diferentes métodos para integrar la misma función.

## Ejercicio 12

$$  
\int_{0}^{1} \frac{\log(1 + x)}{1 + x^2}  dx  
$$  

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \ln(1 + \tan(\theta)) ~\right\}_{0}^{\pi/4} & (1)\\
    &=& \displaystyle \left\{~ \ln \left( \frac{2}{1 + \tan(u)} \right) ~\right\}_{0}^{\pi/4} & (2)\\
    &=& \displaystyle  \frac{\pi}{4}\ln(2) - I \\ \\

    &I& = \displaystyle  \frac{\pi}{8}\ln(2)
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \tan(\theta) \\ dx &=& \sec^2(\theta)d\theta \end{array} \right.$ y $1 + \tan^2(\theta) = \sec^2(\theta)$

- (2): $\left\{\begin{array}{rcl} \theta &=& \pi/4 - u \\ d\theta &=& -du \end{array} \right.$ y $\tan(\pi/4 - u) = \frac{1 - \tan(u)}{1 + \tan(u)}$

## Ejercicio 13

$$  
\int_{64}^{729} \frac{x^{1/2}}{x^{1/2} - x^{1/3}}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 6 \left\{~ \frac{t^{6}}{t - 1} ~\right\}_{2}^{3} & (1)\\
    &=& \displaystyle 6 \left\{~ \frac{(u+1)^{6}}{u} ~\right\}_{1}^{2} & (2)\\
    &=& \displaystyle 6 \left(~ \ln(|u|) + \sum_{k=1}^{6} \binom{6}{k} \frac{1}{k}\cdot u^{k} ~\right)_{1}^{2} & (3)\\
    &=& \displaystyle 6 \left(~ \ln(2) + \sum_{k=1}^{6} \binom{6}{k} \frac{1}{k}\cdot (2^{k}-1) ~\right)\\
    &=& \displaystyle 6 \ln(2) + \frac{10747}{10} & (4)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} t &=& x^{1/6} \\ dt &=& \frac{1}{6} t^{-5} dx \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} u &=& t - 1 \\ du &=& dt \end{array} \right.$

- (3): $(x+1)^n = \sum_{k=0}^{n} \binom{n}{k}x^{k}$

- (4): Usar el triángulo de pascal para este tipo de cuentas.

## Ejercicio 14

$$  
\int x^x (1 + \ln x)  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle x^x + C & (1)\\
\end{array}
$$

- (1): $[x^x] =[e^{x\ln(x)}] =x^x(1 + \ln(x))$

## Ejercicio 15

$$  
\int_0^1 x^{13/2} \sqrt{1 + x^{5/2}}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle 2 \left\{~ t^{4}(t^{5})^2 \sqrt{1 + t^{5}} ~\right\}_{0}^{1} & (1)\\
    &=& \displaystyle \frac{2}{5} \left\{~ (u-1)^2 \sqrt{u} ~\right\}_{1}^{2} & (2)\\
    &=& \displaystyle \frac{2}{5} \left(~ \frac{2}{7}u^{7/2} - \frac{4}{5}u^{5/2} + \frac{2}{3} u^{3/2} ~\right)_{1}^{2}\\
    &=& \displaystyle \frac{2}{5} \left(~ \frac{2}{7}u^{7/2} - \frac{4}{5}u^{5/2} + \frac{2}{3} u^{3/2} ~\right)_{1}^{2}\\
    &\approx& 0.1761  
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& t^{2} \\ dx &=& 2 t ~ dt \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} u &=& t^5 + 1 \\ du &=& 5 t^{4} ~dt \end{array} \right.$

## Ejercicio 16

$$  
\int_1^\infty \frac{1}{(x^2 + 1)^2}  dx  
$$  

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \cos^2(\theta) ~\right\}_{\pi/4}^{\pi/2} & (1)\\
    &=& \displaystyle \frac{1}{2}\left\{~ \cos(2\theta) + 1 ~\right\}_{\pi/4}^{\pi/2} & (2)\\
    &=& \displaystyle \frac{1}{2}\left(~ \frac{\sin(2\theta)}{2} + x ~\right)_{\pi/4}^{\pi/2}\\
    &=& \displaystyle \frac{\pi}{8} - \frac{1}{4}\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \tan(\theta) \\ dx &=& \sec^2(\theta) ~ d\theta \end{array} \right.$

- (2): $\cos(2 \theta) = 2 \cos(\theta) - 1$

## Ejercicio 17

$$  
\int_{0}^{1} \frac{1}{x^4 - 13x^2 + 36}  dx  
$$  

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle - \frac{1}{5} \left\{~ \frac{1}{x^2 -4} - \frac{1}{x^2 -9}  ~\right\}_{0}^{1}\\
    &=& \displaystyle - \frac{1}{5} \left\{~ -\frac{1}{4}\left( \frac{1}{x +2} - \frac{1}{x -2} \right) + \frac{1}{6}\left( \frac{1}{x +3} - \frac{1}{x -3} \right)  ~\right\}_{0}^{1}\\
    &=& \displaystyle - \frac{1}{5} \left(~ -\frac{1}{4}\ln\left( \left| \frac{x+2}{x-2} \right| \right) + \frac{1}{6} \ln\left( \left| \frac{x+3}{x-3} \right|  \right)  ~\right)_{0}^{1}\\
    &=& \displaystyle \frac{\ln(3)}{20} - \frac{\ln(2)}{30}
\end{array}
$$

**Nota:**

1. Hacer fracciones parciales con dos términos es más sencillo que hacer con todos los términos.

2. $\{1/x\} = \ln(|x|)$, importante poner el valor absoluto.

## Ejercicio 18

$$  
\int \frac{\log(\log x)}{x}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \log(t) ~\right\} & (1)\\
    &=& \displaystyle t \ln(t) - t + C & (2)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} t &=& \ln(x) \\ dt &=& \frac{1}{x} ~ dx \end{array} \right.$

- (2): integral importante $\{\ln(x)\} = x \ln(x) - x + C$, usar integración por partes.

## Ejercicio 19

$$  
\int \frac{1 + \cot x}{1 - \cot x}  dx  
$$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle -\left\{~ \cot(\pi/4 - x) ~\right\} & (1)\\
    &=& \displaystyle \ln(~ |\sin(\pi/4 - x)| ~) + C & (2)\\
\end{array}
$$

- (1): $\tan(\pi/4 - x) = \frac{\cos(x) - \sin(x)}{\cos(x) + \sin(x)} = \frac{1 - \tan(x)}{1 + \tan(x)} = \frac{\cot(x) - 1}{\cot(x) + 1}$

- (2): $\{\cot(x)\} = \ln(|\sin(x)|)$

## Ejercicio 20

$$
\int \frac{\cos x + x \sin x}{x(x + \cos x)}  dx  
$$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1 + x \tan(x)}{x(x\sec(x) + 1)} ~\right\}\\
    &=& \displaystyle \left\{~ \frac{\sec(x) + x \sec(x) \tan(x)}{x\sec(x)(x\sec(x) + 1)} ~\right\}\\
    &=& \displaystyle \left\{~ \frac{1}{t(t + 1)} ~\right\} & (1)\\
    &=& \displaystyle \left\{~ \frac{1}{t} - \frac{1}{t + 1} ~\right\}\\
    &=& \displaystyle \ln |t| - \ln|t+1| + C\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} t &=& x \sec(x) \\ dt &=& (\sec(x) + x \sec(x) \tan(x) )~ dx \end{array} \right.$

## Ejercicio 21

$$  
\int_0^{\pi/2} \frac{1}{\sin x + \sec x}  dx  
$$

$$\textcolor{orange}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{1}{\cos(\theta) + \csc(\theta)} ~\right\}_{0}^{\pi/2}& (1)\\ \\

    2I &=& \displaystyle \left\{~ \frac{1}{\sin x + \sec x} + \frac{1}{\cos(\theta) + \csc(\theta)} ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle \left\{~ \frac{\sin(x) + \cos(x)}{\sin(x)\cos(x) + 1}  ~\right\}_{0}^{\pi/2}\\
    &=& \displaystyle 2 \left\{~ \frac{\sin(x) + \cos(x)}{3 - (\sin(x)-\cos(x))^2}  ~\right\}_{0}^{\pi/2} & (2)\\
    &=& \displaystyle 2 \left\{~ \frac{1}{3 - t^2}  ~\right\}_{-1}^{1} & (3)\\
    &=& \displaystyle \frac{1}{\sqrt{3}} \left\{~ \frac{1}{\sqrt{3} - t} + \frac{1}{\sqrt{3} + t}  ~\right\}_{-1}^{1}\\
    &=& \displaystyle \frac{1}{\sqrt{3}} \left(~ \ln|\sqrt{3}+t| - \ln|\sqrt{3}-t|  ~\right)_{-1}^{1}\\
    &=& \displaystyle \frac{1}{\sqrt{3}}\ln \left( \frac{2+\sqrt{3}}{2 - \sqrt{3}} \right)\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& \pi/2 - \theta \\ dx &=& -d\theta \end{array} \right.$, $\sin(\pi/2 - \theta) = \cos(\theta)$ y $\cos(\pi/2 - \theta) = \sin(\theta)$

- (2): $(\sin(x) - \cos(x))^2 = 1 -2\sin(x)\cos(x)$

- (3): $\left\{\begin{array}{rcl} t &=& \sin(x) - \cos(x) \\ dt &=& (\sin(x) + \cos(x))~dx \end{array} \right.$

## Ejercicio 22

$$  
\int_0^\infty \frac{1}{\sqrt{1 + e^x + e^{2x}}}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{e^t}{\sqrt{1 + e^t + e^{2t}}} ~\right\}_{-\infty}^{0}& (1)\\
    &=& \displaystyle \left\{~ \frac{1}{\sqrt{1 + u + u^{2}}} ~\right\}_{0}^{1}& (2)\\
    &=& \displaystyle \left\{~ \frac{1}{\sqrt{(u + 1/2)^2 + 3/4}} ~\right\}_{0}^{1}\\
    &=& \displaystyle \left\{~ \sec(\theta) ~\right\}_{\pi/6}^{\pi/3} & (3)\\
    &=& \displaystyle \left(~ \ln|\tan(\theta) + \sec(\theta)| ~\right)_{\pi/6}^{\pi/3}\\
    &=& \displaystyle \left(~ \ln(2 + \sqrt{3}) - \frac{1}{2}\ln(3) ~\right)_{\pi/6}^{\pi/3}\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& -t \\ dx &=& -dt \end{array} \right.$

- (2): $\left\{\begin{array}{rcl} u &=& e^t \\ du &=& e^t ~dt \end{array} \right.$

- (3): $\left\{\begin{array}{rcl} u + 1/2 &=& \frac{\sqrt{3}}{2}\tan(\theta) \\ du &=& \frac{\sqrt{3}}{2} \sec^2(\theta) dt \end{array} \right.$

## Ejercicio 23

$$  
\int_{0}^{1} x^3 e^{x^2}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ xx^2 e^{x^2} ~\right\}_{0}^{1}\\
    &=& \displaystyle \frac{1}{2} \left\{~ u e^{u} ~\right\}_{0}^{1}\\
    &=& \displaystyle \frac{1}{2} \left(~ u e^{u} - e^u ~\right)_{0}^{1} & (2)\\
    &=& \displaystyle \frac{1}{2}\\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} u &=& x^2 \\ du &=& 2x~dx \end{array} \right.$

- (2): $\begin{array}{|c|c|} D & I \\ u & e^u \\ 1 & e^u \\ 0 & e^u \\ \end{array}$

## Ejercicio 24

$$  
\int_{0}^{1} \sqrt{1 + x\sqrt{1 + x\sqrt{1 + x\sqrt{\cdots}}}}~dx  
$$

$$\textcolor{red}{---\text{ Demostración } ---}$$

Considere la siguiente sucesión:

$$
a_1 = \sqrt{1+x} ~~,~~ a_{n+1} = \sqrt{1+xa_n} ~~~~\text{para } x \in [0,1]
$$

Veamos que $\{a_n\}_{n \geq 1}$ converge para todo $x \in [0,1]$.

**(Monótona Creciente)** Usando induccion matemática tenemos que:

$$
\begin{array}{rclr}
    a_1 &=& \sqrt{1+x} \\
    &\geq& 1 \\ \\

    a_1 - 1 &\geq& 0\\
    x(a_1 - 1) &\geq& 0\\
    xa_1 &\geq& x\\
    1 + xa_1 &\geq& 1 + x\\
    a_2^2 &\geq& a_1^2\\
    a_2 &\geq& a_1\\
\end{array}
$$

Suponiendo que para $n \in \mathbb{N}$ se tiene que $a_{n} \geq a_{n-1}$, entonces:

$$
\begin{array}{rclr}
    a_{n} &\geq& a_{n-1}\\
    xa_{n} &\geq& xa_{n-1}\\
    1 + xa_{n} &\geq& 1 + xa_{n-1}\\
    a_{n+1}^2 &\geq& a_{n}^2\\
    a_{n+1} &\geq& a_{n}\\
\end{array}
$$

Así pues, la sucesión $\{a_n\}_{n \geq 1}$ es monótona creciente.

**(Acotada Superiormente)** veamos que la sucesión $\{a_n\}_{n \geq 1}$ es acotada superiormente por $2$. Razonemos por inducción matemática.

Claramente tenemos que $a_1 \leq \sqrt{2} \leq 2$ pues $x \in [0,1]$, ahora suponiendo que para $n \in \mathbb{N}$ se tiene que $a_n \leq 2$, entonces:

$$
\begin{array}{rclr}
    a_{n} &\leq& 2 \\
    xa_{n} &\leq& 2 \\
    1 + xa_{n} &\leq& 3 \\
    a_{n+1}^2 &\leq& 3 \\
    a_{n+1} &\leq& \sqrt{3} \\
    &\leq& 2 \\
\end{array}
$$

Así pues, la sucesión $\{a_n\}_{n \geq 1}$ es acotada superiormente por $2$.

Considere la función $f(x) = \lim_{n \to \infty} a_n(x)$ para todo $x \in [0,1]$, esta función esta bien definida pues ya vimos que la sucesión $\{a_n\}_{n \geq 1}$ converge para todo $x \in [0,1]$.

$$
\begin{array}{rclr}
    a^2 &=& \displaystyle \lim_{n \to \infty} a^2_n\\
    &=& \displaystyle \lim_{n \to \infty} 1 + xa_{n-1}\\
    &=& \displaystyle 1 + xa\\
    a &=& \displaystyle \frac{x + \sqrt{x^2 + 4}}{2}
\end{array}
$$

Así pues, tenemos que:

$$
f(x) = \lim_{n \to \infty} a_n(x) = \displaystyle \frac{x + \sqrt{x^2 + 4}}{2}
$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{x + \sqrt{x^2 + 4}}{2} ~\right\}_{0}^{1}\\
    &=& \displaystyle \frac{1}{2} \left\{~ x + \sqrt{x^2 + 4} ~\right\}_{0}^{1}\\ \\

    I_1 &=& \displaystyle \left\{~ \sqrt{x^2 + 4} ~\right\}_{0}^{1}\\
    &=& \displaystyle 4 \left\{~ \sec^3(\theta) ~\right\}_{0}^{\arctan(1/2)} & (1)\\
    &=& \displaystyle 2 \left(~ \sec(\theta)\tan(\theta) + \ln |\tan(\theta) + \sec(\theta)| ~\right)_{0}^{\arctan(1/2)} & (2)\\
    &=& \displaystyle 2 \left(~ \frac{x\sqrt{x^2+4}}{4} + \ln \left| \frac{x + \sqrt{x^2+4}}{2} \right| ~\right)_{0}^{1} & (3)\\
    &=& \displaystyle \frac{\sqrt{5}}{2} + 2 \ln \left( \frac{1 + \sqrt{5}}{2} \right) \\\\

    I &=& \displaystyle \frac{1}{4} + \frac{\sqrt{5}}{4} + \ln \left( \frac{1 + \sqrt{5}}{2} \right)
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x &=& 2\tan(\theta) \\ dx &=& 2\sec^2(\theta)~d\theta \end{array} \right.$

- (2):

    $$
    \begin{array}{rclr}
        I(n) &=&\{\sec^n(\theta) \}\\
        &=& \sec^{n-2}(\theta)\tan(\theta) - (n-2) \{\sec^{n-2}(\theta)\tan^2(\theta)\} + C\\
        &=& \sec^{n-2}(\theta)\tan(\theta) - (n-2) \{\sec^{n}(\theta) - \sec^{n-2}(\theta)\} + C\\
        I(n) (n-1) &=& \sec^{n-2}(\theta)\tan(\theta) + (n-2) I(n-2) + C\\
        I(n)&=& \frac{\sec^{n-2}(\theta)\tan(\theta)}{n-1} + \frac{n-2}{n-1} I(n-2) + C\\
    \end{array}
    $$

- (3): Resolver para $\theta$ la siguinete ecuación $\tan (\theta) = \frac{1}{2}$

**Nota:**

1. Toda sucesión monótona ( creciente / decreciente ) acotada ( superiormente / inferiormente ) es convergente.

## Ejercicio 25

$$  
\int \left( \frac{1}{\log x} - \frac{1}{(\log x)^2} \right)  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \frac{\ln(x)-1}{(\ln x)^2} ~\right\}\\
    &=& \displaystyle \frac{x}{\ln(x)} + C & (1)\\
\end{array}
$$

- (1): $\left[ \frac{f(x)}{g(x)} \right] = \frac{f'(x)g(x) - g'(x)f(x)}{g^2(x)}$

## Ejercicio 26

$$  
\int_1^2 \sqrt{(x-1)(2-x)}  dx  
$$

$$\textcolor{green}{---\text{ Demostración } ---}$$

$$
\begin{array}{rclr}
    I &=& \displaystyle \left\{~ \sqrt{1/4 - (x - 3/2)^2} ~\right\}_{1}^{2}\\
    &=& \displaystyle \frac{1}{4} \left\{~ |\cos(\theta)|\cos(\theta) ~\right\}_{3\pi/2}^{\pi/2} & (1)\\
    &=& \displaystyle -\frac{1}{4} \left\{~ \cos^2(\theta) ~\right\}_{3\pi/2}^{\pi/2}\\
    &=& \displaystyle -\frac{1}{8} \left\{~ \cos(2\theta) + 1 ~\right\}_{3\pi/2}^{\pi/2} & (2)\\
    &=& \displaystyle -\frac{1}{8} \left(~  \frac{\sin(2\theta)}{2} + \theta ~\right)_{3\pi/2}^{\pi/2}\\
    &=& \displaystyle \frac{\pi}{8} \\
\end{array}
$$

- (1): $\left\{\begin{array}{rcl} x - 3/2 &=& 1/2 \sin(\theta) \\ dx &=& 1/2\cos(\theta)~d\theta \end{array} \right.$

- (2): $\cos(2 \theta) = 2\cos^2(\theta) - 1$
