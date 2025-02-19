Integrantes: 
* Miguel Arturo Monreal Villa 
* Sebastian Yamil Castellanso Gomez
* Emiliano Sandoval Pelaez

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
| Binomial  | p=0.5,p=0.7,p=0.9  | 0.0048076186  | 0.0017377124  | 0.0038437253  |
| Poisson  | λ=1,λ=4,λ=8  |  0.0048552849 | 0.0000855522  | 0.0004606245  |
| Normal  | µ=2, σ^2=4  |  0.0084982439 |  0.0022024482 |  0.0038983928 |
| Gamma  | (α=1,β=3),(α=3,β=1),(α=5,β=5) |  0.0087983653 |  0.0049537035 | 0.0010603833  |
| Beta  |  (θ_1=1,θ_2=1),(θ_1=1/2,θ_2=2),(θ_1=3,θ_2=1/3),(θ_1=1/2,θ_2=1/2) |  0.0005558283 |  0.0002853538 | 0.0002525465  |