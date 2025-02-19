**Integrantes:**
* Miguel Arturo Monreal Villa 
* Sebastian Yamil Castellanso Gomez
* Emiliano Sandoval Pelaez

Seed usada a partir de la pregunta 2: 20240905

# Pregunta 1:
Calcule n!; la correspondiente **aproximacion de Stirling** $(S(n))=n!\approx \sqrt{2\pi n} n^n e^{-n}$; la diferencia entre ellas $(D(n)=n!-S(n))$; y la diferencia relativa $(DR(n)=D(n)/n!)$ para $n=1,...,12.$

| n  | n!  | S(n)  | D(n)  | D(n)/n!  |
|---|---|---|---|---|
| 1  | 1  |  9.221370e-01 | 7.786299e-02  | 0.077862991  |
| 2  | 2  |  1.919004e+00 | 8.099565e-02  | 0.040497824  |
| 3  | 6  | 5.836210e+00  | 1.637904e-01  | 0.027298401  |
| 4  | 24  | 2.350618e+01  | 4.938249e-01  | 0.020576036  |
| 5  | 120  |  1.180192e+02 | 1.980832e+00  | 0.016506934  |
| 6  | 720  | 7.100782e+02  | 9.921815e+00  | 0.013780299  |
| 7  | 5040  | 4.980396e+03  | 5.960417e+01  | 0.011826224  |
| 8  | 40320  | 3.990240e+04  |  4.176045e+02 | 0.010357256  |
| 9  | 362880  | 3.595369e+05  | 3.343127e+03  | 0.009212762  |
| 10  | 3628800  | 3.598696e+06  | 3.010438e+04  | 0.008295960  |
| 11  |  39916800 |  3.961563e+07 | 3.011749e+05  | 0.007545067  |
| 12  | 479001600  |  4.756875e+08 | 3.314114e+06  | 0.006918794  |

---

# Pregunta 2 (Simulacion):
Con base en la simulacion anterior determine $p_N=P_N(3< X \leq 4)$ y comparelo con $p=P(3<X\leq4)$, la probabilidad teorica calculada con base en la distribucion de X, $Gamma(\alpha=2, \beta=1)$. La diferencia entre ellas es el **error de estimacion**, $\epsilon=p_N-p=0.1079-0.1076=-0.0003$

* $p_N=0.1077$
* $p=0.1075701$
* $\epsilon=0.000129921$

---

# Pregunta 3: 
Calcule los errores de aproximacion de la distribucion normal teórica $(\phi)$ a la distribucion del promedio de las distintas leyes de probabilidad de la tabla 2 para tamaños de muestra $n=30,100,500$, indicados en la tabla 3. 

| distribucion  | parametros  | n=30  | n=100  | n=500  | 
|---|---|---|---|---|
| Binomial  | $$\begin{align*}p=0.5\\p=0.7\\p=0.9\end{align*}$$  | $$\begin{align*}0.0048076186\\0.0029018996\\0.0015798985\end{align*}$$  | $$\begin{align*}0.0029836734\\5.066061e-03\\1.076412e-03\end{align*}$$ | $$\begin{align*}0.0004332234\\1.646701e-03\\2.079719e-04\end{align*}$$  |
| Poisson  | $$\begin{align*}λ=1\\λ=4\\λ=8\end{align*}$$  |  $$\begin{align*}0.0021613349\\0.0048552849\\1.122741e-02\end{align*}$$ | $$\begin{align*}0.0020205335\\2.654185e-04\\4.772015e-04\end{align*}$$  | $$\begin{align*}0.0004890635\\2.483183e-03\\2.385604e-03\end{align*}$$  |
| Normal  | $$\begin{align*}µ=2\\ σ^2=4\end{align*}$$  |  0.0084982439 |  0.0022024482 |  0.0038983928 |
| Gamma  | $$\begin{align*}α=1,β=3\\α=3,β=1\\α=5,β=5\end{align*}$$ |  $$\begin{align*}1.289979e-02\\0.0087983653\\7.017280e-02\end{align*}$$ |  $$\begin{align*}0.0044094176\\3.361983e-03\\2.067220e-02\end{align*}$$ | $$\begin{align*}0.0036913032\\4.598797e-04\\2.295500e-03\end{align*}$$  |
| Beta  |  $$\begin{align*}θ_1=1,θ_2=1\\θ_1=1/2,θ_2=2\\θ_1=3,θ_2=1/3\\θ_1=1/2,θ_2=1/2\end{align*}$$ |  $$\begin{align*}0.0005558283\\2.461275e-04\\2.038467e-04\\0.0001034358\end{align*}$$ |  $$\begin{align*}0.0005258091\\4.217393e-04\\4.187085e-05\end{align*}$$ | $$\begin{align*}0.0003908928\\3.587558e-05\\6.446036e-05\end{align*}$$  |