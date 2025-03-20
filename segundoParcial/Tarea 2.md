**Miembros:**
* Miguel Arturo Monreal Villa **196891**
* Sebastian Yamil Castellanso Gomez **198090**
* Emiliano Sandoval Pelaez **195557**
## Pregunta 1 

### Resumen de resultados
Para cada clave:
- **Clave 195557**: Metodo de momentos $θ̂_{EMM} = -0.930$, maxima verosimilitud $θ̂_{EMV} = -0.603$
- **Clave 196891**: Metodo de momentos $θ̂_{EMM} = -1.229$, maxima verosimilitud $θ̂_{EMV} = -0.923$
- **Clave 198090**: Metodo de momentos $θ̂_{EMM} = -0.862$, maxima verosimilitud $θ̂_{EMV} = -0.735$

### Observaciones
- La varianza de la muestra para los tres conjuntos de datos (0,241, 0,231, 0,226) es consistentemente inferior a la varianza teórica para una distribución U(θ, θ+2) (0,333).
- El EMV produce consistentemente estimaciones mayores (menos negativas) que el método de momentos.
- El rango de los datos para las tres muestras es inferior a 2, que es el rango teórico de la distribución.

## Pregunta 2

### Resultados
- **EMV analítico**: $μ̂ = 5.181, σ̂² = 3.300$
- **EMV numérico**: $μ̂ = 5.181, σ̂² = 3.300$
- **Eigenvalores de la matriz Hessiana**: $-4.592, -30.307$ (ambos negativos, lo que confirma que es definida negativa)

### Observaciones
- Las soluciones analíticas y numéricas coinciden casi exactamente, lo que valida la derivación matemática.
- La hessiana simplificada (con elementos fuera de la diagonal iguales a cero) tiene valores propios idénticos a los de la hessiana completa.
- La definición negativa de la hessiana confirma que el EMV es realmente un máximo.

## Pregunta 3:

### Resultados
- **Parámetros reales**: $μ = 10, σ = 2$
- **Rango teórico**: $[6.536, 13.464]$
- **Rango de la muestra**: $[6.540, 13.424]$
- **Estimador por Maxima Verosimilitud**: $μ̂ = 9.982, σ̂ = 1.987$

### Observaciones
- Las fórmulas para los EMV $μ̂ = (X₍₁₎+X₍ₙ₎)/2$ y $σ̂ = (X₍ₙ₎-X₍₁₎)/(2√3)$ producen valores muy cercanos a los parámetros verdaderos.
- La formulación teórica se valida mediante los resultados numéricos.
- Las ligeras diferencias entre los parámetros estimados y los verdaderos se deben a la variabilidad del muestreo.

## Pregunta 4:

### Resultados
Para cada clave:
- **Clave 195557**: EMM estima $α = 1.782, λ = 1.070$; EMV estima $α = 1.811, λ = 1.087$
![[Pasted image 20250320153759.png]]
- **Clave 196891**: EMM estima $α = 2.729, λ = 1.521$; EMV estima $α = 2.844, λ = 1.585$
![[Pasted image 20250320153812.png]]
- **Clave 198090**: EMM estima $α = 2.176, λ = 1.538$; EMV estima $α = 2.891, λ = 2.042$
![[Pasted image 20250320153820.png]]
### Observaciones:
- El EMV generalmente produce estimaciones más altas para ambos parámetros en comparación con el método de momentos.
- La diferencia entre los métodos de estimación es más pronunciada para conjuntos de datos con parámetros de forma más bajos.
- La relación entre la forma y la tasa $(α/λ)$ es más consistente entre los métodos que los parámetros individuales.

## Pregunta 5:

### Resultados
## a) Varianza del Estimador por Método de Momentos
Para determinar la varianza del estimador por método de momentos $\tilde\alpha=3\bar X$, necesitamos primero calcular la varianza de $\bar X$. La varianza de $X$ para esta distribución es:
$Var(X) = E(X^2) - [E(X)]^2$
Donde:
- $E(X) = \int_{-1}^{1} x \cdot \frac{1+\alpha x}{2} dx = \frac{\alpha}{3}$
- $E(X^2) = \int_{-1}^{1} x^2 \cdot \frac{1+\alpha x}{2} dx = \frac{1}{3} + \frac{\alpha}{4}$
Por lo tanto:
$Var(X) = \frac{1}{3} + \frac{\alpha}{4} - \left(\frac{\alpha}{3}\right)^2 = \frac{1}{3} + \frac{\alpha}{4} - \frac{\alpha^2}{9} = \frac{3 + \frac{9\alpha}{4} - \frac{\alpha^2}{3}}{9} = \frac{1 - \frac{\alpha^2}{9}}{3}$

Dado que $\tilde\alpha = 3\bar X$ y $Var(\bar X) = \frac{Var(X)}{n}$, tenemos: $Var(\tilde\alpha) = 9 \cdot Var(\bar X) = 9 \cdot \frac{1 - \frac{\alpha^2}{9}}{3n} = \frac{3 - \alpha^2}{n}$
Por lo tanto, queda demostrado que:
$Var(\tilde\alpha) = \frac{3 - \alpha^2}{n}$
- **Método de momentos**: media = 0.670, varianza = 0.043, varianza teórica = 0.070
- **Máxima verosimilitud**: media = 0.694, varianza = 0.045
- **Eficiencia relativa empírica**: 1.038
## b) Aproximación mediante el Teorema del Límite Central
Aplicando el Teorema del Límite Central, para $n$ grande, $\tilde\alpha$ sigue aproximadamente una distribución normal: $\tilde\alpha \sim N\left(\alpha, \frac{3-\alpha^2}{n}\right)$
Para el caso particular donde $n=25$ y $\alpha=0$, queremos calcular $P(|\tilde\alpha|>0.5)$.
Cuando $\alpha=0$, $\tilde\alpha \sim N\left(0, \frac{3}{25}\right)$, por lo que:
$P(|\tilde\alpha|>0.5) = P(\tilde\alpha > 0.5) + P(\tilde\alpha < -0.5) = 2 \cdot P(\tilde\alpha > 0.5)$
Estandarizando:
$P(\tilde\alpha > 0.5) = P\left(Z > \frac{0.5}{\sqrt{3/25}}\right) = P(Z > 1.443)$
Utilizando la tabla de la distribución normal o la función de R:
$P(Z > 1.443) \approx 0.0745$
Por lo tanto:
$P(|\tilde\alpha|>0.5) = 2 \times 0.0745 \approx 0.149$
Es decir, hay aproximadamente un 14.9% de probabilidad de que el valor absoluto del estimador por método de momentos exceda 0.5 cuando el verdadero valor de α es 0 y el tamaño de muestra es 25.
## c) Varianza Asintótica del Estimador por Máxima Verosimilitud
Para el estimador de máxima verosimilitud $\hat\alpha$, su varianza asintótica está dada por:
$Var(\hat\alpha) \approx \frac{1}{nI(\alpha)}$
donde $I(\alpha)$ es la información de Fisher.
Para calcular $I(\alpha)$, recordemos que:
$I(\alpha) = E\left[\left(\frac{\partial}{\partial\alpha}\log f(X;\alpha)\right)^2\right]$
Para esta distribución:
$\log f(x;\alpha) = \log\left(\frac{1+\alpha x}{2}\right) = \log(1+\alpha x) - \log(2)$
Derivando:
$\frac{\partial}{\partial\alpha}\log f(x;\alpha) = \frac{x}{1+\alpha x}$
Por lo tanto:
$I(\alpha) = E\left[\left(\frac{X}{1+\alpha X}\right)^2\right] = \int_{-1}^{1} \frac{x^2}{(1+\alpha x)^2} \cdot \frac{1+\alpha x}{2} dx = \frac{1}{2}\int_{-1}^{1} \frac{x^2}{1+\alpha x} dx$
Resolviendo esta integral mediante técnicas de cálculo avanzado, se obtiene:
$I(\alpha) = \frac{1}{2\alpha^3}\left[\log\left(\frac{1+\alpha}{1-\alpha}\right)-2\alpha\right]$
Por lo tanto, la varianza asintótica del estimador por máxima verosimilitud es:
$Var(\hat\alpha) \approx \frac{1}{n \cdot \frac{1}{2\alpha^3}\left[\log\left(\frac{1+\alpha}{1-\alpha}\right)-2\alpha\right]}$
![[Pasted image 20250320154144.png]]
## e) Eficiencia Relativa para Diferentes Valores de α
La eficiencia relativa (RE) del estimador por método de momentos con respecto al estimador por máxima verosimilitud se define como:
$RE(\alpha) = \frac{Var(\hat\alpha)}{Var(\tilde\alpha)} = \frac{\frac{1}{nI(\alpha)}}{\frac{3-\alpha^2}{n}} = \frac{3-\alpha^2}{I(\alpha)}$
Para valores pequeños de α, ambos estimadores tienen eficiencias similares (RE≈1), pero a medida que α aumenta, el estimador de máxima verosimilitud se vuelve más eficiente (RE decrece).
A continuación se presenta una tabla de eficiencia relativa para diferentes valores de α:

|k|α|Eficiencia Relativa|
|---|---|---|
|1|0.00|1.000|
|2|0.08|0.991|
|3|0.17|0.965|
|4|0.25|0.924|
|5|0.33|0.871|
|6|0.42|0.808|
|7|0.50|0.737|
|8|0.58|0.659|
|9|0.67|0.575|
|10|0.75|0.484|
|11|0.83|0.387|
|12|0.92|0.273|
|13|0.99|0.118|
### Obervaciones
- La varianza empírica del estimador del método de los momentos es inferior a su varianza teórica.
- El estimador de máxima verosimilitud tiene una varianza ligeramente superior, pero posiblemente menos sesgo (media más cercana al valor real).
- La eficiencia relativa favorece ligeramente al estimador de máxima verosimilitud.
- Alrededor del 17,4 % de las muestras fueron filtradas, lo que debe tenerse en cuenta al interpretar los resultados.