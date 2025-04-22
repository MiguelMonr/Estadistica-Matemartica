# Tarea 3  
**Miembros:**  
* Miguel Arturo Monreal Villa **196891**  
* Sebastian Yamil Castellanos Gomez **198090**
* Emiliano Sandoval Pelaez **195557**

---

## Pregunta 1: **Estimadores insesgados de mínima varianza (EIVM) en Poisson**

### Resumen de resultados

| # | $λ$   | $p_0$    | $\theta$     | $n$  | $\hat{p}_0$   | $ee(\hat{p}_0)$ | $\check p_0$   | $ee(\check p_0)$ | $\tilde p_0$   | $ee(\tilde p_0)$ |
|---|-----|--------|-------|----|-------|---------|-------|---------|-------|---------|
| 1 | 0.5 | 0.6065 | 0.6125| 25 | 0.6091| 0.0836  |0.6029 | 0.0965  |0.6031 | 0.0844  |
| 2 | 0.5 | 0.6065 | 0.6096| 50 | 0.6103| 0.0604  |0.6079 | 0.0681  |0.6073 | 0.0607  |
| 3 | 0.5 | 0.6065 | 0.6084| 80 | 0.6085| 0.0478  |0.6068 | 0.0546  |0.6066 | 0.0479  |
| 4 | 1.0 | 0.3679 | 0.3752| 25 | 0.3769| 0.0741  |0.3697 | 0.0970  |0.3696 | 0.0741  |
| 5 | 1.0 | 0.3679 | 0.3716| 50 | 0.3705| 0.0519  |0.3672 | 0.0684  |0.3668 | 0.0519  |
| 6 | 1.0 | 0.3679 | 0.3702| 80 | 0.3710| 0.0409  |0.3680 | 0.0537  |0.3687 | 0.0409  |
| 7 | 2.0 | 0.1353 | 0.1408| 25 | 0.1403| 0.0391  |0.1346 | 0.0691  |0.1348 | 0.0384  |
| 8 | 2.0 | 0.1353 | 0.1381| 50 | 0.1385| 0.0276  |0.1370 | 0.0490  |0.1358 | 0.0273  |
| 9 | 2.0 | 0.1353 | 0.1370| 80 | 0.1370| 0.0220  |0.1348 | 0.0382  |0.1353 | 0.0218  |

### Observaciones
- Los estimadores insesgados ($\check p_0$ y $\tilde p_0$) presentan valores promedio muy cercanos a $p_0$, mientras que $\hat p_0$ tiene un sesgo positivo, especialmente con muestras pequeñas.
- El error estándar disminuye al aumentar el tamaño de muestra, como era de esperarse.
- El estimador $\tilde p_0$ (Rao-Blackwell-Lehmann-Scheffé) muestra la menor varianza entre los insesgados, lo que valida el resultado teórico.

---

## Pregunta 2: **Amplitud de los intervalos de probabilidad**

### Resultados para distribución normal  $N(0, \sigma)$:

| $σ$ | Conf. | $q_i^{sim}$ | $q_s^{sim}$ | $w^{sim}$ | $q_i^{min}$ | $q_s^{min}$ | $w^{min}$ |
|---|-------|--------------|--------------|-------------|---------------|---------------|-------------|
| 1 | 0.90  | -1.6449      | 1.6449       | 3.2897      | -1.6449       | 1.6449        | 3.2897      |
| 1 | 0.95  | -1.9600      | 1.9600       | 3.9199      | -1.9600       | 1.9600        | 3.9199      |
| 1 | 0.99  | -2.5758      | 2.5758       | 5.1517      | -2.5758       | 2.5758        | 5.1517      |
| 2 | 0.90  | -3.2897      | 3.2897       | 6.5794      | -3.2897       | 3.2897        | 6.5794      |
| 2 | 0.95  | -3.9199      | 3.9199       | 7.8399      | -3.9199       | 3.9199        | 7.8399      |
| 2 | 0.99  | -5.1517      | 5.1517       | 10.3033     | -5.1517       | 5.1517        | 10.3033     |
| 5 | 0.90  | -8.2243      | 8.2243       | 16.4485     | -8.2243       | 8.2243        | 16.4485     |
| 5 | 0.95  | -9.7998      | 9.7998       | 19.5996     | -9.7998       | 9.7998        | 19.5996     |
| 5 | 0.99  | -12.8791     | 12.8791      | 25.7583     | -12.8791      | 12.8791       | 25.7583     |

### Resultados para distribución chi-cuadrada $\chi^2_n$:

| $n$  | Conf. | $q_i^{sim}$ | $q_s^{sim}$ | $w^{sim}$ | $q_i^{min}$ | $q_s^{min}$ | $w^{min}$ |
|----|-------|--------------|--------------|-------------|---------------|---------------|-------------|
| 5  | 0.90  | 1.1455       | 11.0705      | 9.9250      | 0.4725        | 9.4299        | 8.9575      |
| 5  | 0.95  | 0.8312       | 12.8325      | 12.0013     | 0.2968        | 11.1921       | 10.8952     |
| 5  | 0.99  | 0.4117       | 16.7496      | 16.3379     | 0.1027        | 15.1286       | 15.0259     |
| 10 | 0.90  | 3.9403       | 18.3070      | 14.3667     | 3.0094        | 16.7029       | 13.6935     |
| 10 | 0.95  | 3.2470       | 20.4832      | 17.2362     | 2.4173        | 18.8639       | 16.4465     |
| 10 | 0.99  | 2.1559       | 25.1882      | 23.0323     | 1.5052        | 23.5402       | 22.0350     |
| 20 | 0.90  | 10.8508      | 31.4104      | 20.5596     | 9.7842        | 29.8741       | 20.0900     |
| 20 | 0.95  | 9.5908       | 34.1696      | 24.5788     | 8.5897        | 32.6128       | 24.0231     |
| 20 | 0.99  | 7.4338       | 39.9968      | 32.5630     | 6.5421        | 38.3872       | 31.8451     |

---

## Pregunta 3: **Comparación de algoritmos (medias y varianzas)**

### Resultados

1. **Intervalo del 90% de confianza para $\mu_1$ $(\sigma_1 = 1)$:**  
   $[9.601,\, 10.259]$

2. **Intervalo del 95% de confianza para $\mu_2$ ($\sigma_2$ desconocida):**  
   $[9.7855,\, 11.0721]$

3. **Intervalos de confianza del 95% para las desviaciones estándar:**  
   - $\sigma_1$: $[0.7904,\, 1.4081]$
   - $\sigma_2$: $[1.2169,\, 2.1680]$

4. **Intervalo de confianza del 95% para el cociente de varianzas $\theta = \sigma_1^2 / \sigma_2^2$:**  
   $[0.1859,\, 0.9573]$

### Estadísticas descriptivas:
- **Algoritmo 1:**  
  Media: 9.93  
  Desviación estándar: 1.0122  
  Varianza: 1.0246

- **Algoritmo 2:**  
  Media: 10.4288  
  Desviación estándar: 1.5584  
  Varianza: 2.4287

### Observaciones
- Los intervalos muestran que la media y la varianza del algoritmo 2 son mayores que las del algoritmo 1.
- El cociente de varianzas indica que el algoritmo 1 es más consistente en sus tiempos de ejecución.
- No hay evidencia clara para asumir igual varianza entre ambos algoritmos.

