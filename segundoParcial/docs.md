**Integrantes:**
* Miguel Arturo Monreal Villa
* Sebastian Yamil Castellanos
* Emiliano Sandoval 

---

# **Pregunta 1**: Estimadores de theta para una distribución uniforme

Dada una muestra aleatoria de una población uniforme en el intervalo (theta, theta + 2), se deben encontrar los estimadores por:

- **Método de Momentos**: Se obtiene igualando la esperanza de la muestra con la esperanza teórica:

  - Estimador por momentos: `theta_mom = media_muestra - 1`

- **Máxima Verosimilitud**: Se obtiene considerando la función de verosimilitud:

  - Estimador de máxima verosimilitud: `theta_mv = min(muestra)`

**Resultados calculados**:
- `theta_mom = -0.9199078`
- `theta_mv = -0.9199078`

---

# **Pregunta 2**: Estimadores de máxima verosimilitud para una normal

Dada una muestra de una distribución normal `X ~ N(mu, sigma^2)`, se deben encontrar los estimadores de máxima verosimilitud para `mu` y `sigma^2`.

Fórmulas:

- `mu_hat = media_muestra`
- `sigma2_hat = varianza_muestra * (n - 1) / n`

Además, se debe verificar que la matriz Hessiana de la función de log-verosimilitud es definida negativa.

**Resultados calculados**:
- `mu_hat = 1.415389`
- `sigma2_hat = 0.8942962`
- `La matriz Hessiana es definida negativa: Sí`

---

# **Pregunta 3**: Estimadores de máxima verosimilitud para una distribución dada

Dada la función de densidad de probabilidad:

`f(x; mu, sigma) = 1 / (2 * sqrt(3) * sigma)`

Se deben calcular los estimadores de máxima verosimilitud:

- `mu_mv = (min(muestra) + max(muestra)) / 2`
- `sigma_mv = (max(muestra) - min(muestra)) / (2 * sqrt(3))`

**Resultados calculados**:
- `mu_mv = 2.32797`
- `sigma_mv = 1.106696`
- `Media de mu estimado = 2.241126`
- `Varianza de mu estimado = 0.03644516`
- `Media de sigma estimado = 1.037116`
- `Varianza de sigma estimado = 0.01203285`

---

# **Pregunta 4**: Estimadores para una distribución Gamma

Dada una muestra de una distribución Gamma con parámetros `alpha` y `lambda`, se deben encontrar:

- **Estimadores de momentos**:
  - `alpha_mom = (media_muestra)^2 / varianza_muestra`
  - `lambda_mom = media_muestra / varianza_muestra`

- **Estimadores de máxima verosimilitud** (calculados numéricamente).

**Resultados calculados**:
- `alpha_mom = 2.176113`
- `lambda_mom = 1.537466`
- `alpha_mv = 2.890545`
- `lambda_mv = 2.042225`

**Gráficas**
![Gráfica de estimadores Gamma](images/Screenshot%202025-03-20%20at%2010.14.01 a.m..png)
![Gráfica de estimadores Gamma](images/Screenshot%202025-03-20%20at%2010.14.28 a.m..png)
---
# **Pregunta 5**: Distribución angular

Dada la distribución angular:

`f(x; alpha) = (1 + alpha * x) / 2`

Se deben calcular los estimadores de:

- **Método de Momentos**:
  - `alpha_mom = 3 * media_muestra`

- **Máxima Verosimilitud** (resuelto numéricamente).

Además, se evalúa la eficiencia relativa de ambos estimadores.

### **Resultados calculados**:

**Estadísticas descriptivas después del filtrado:**
- Número de muestras válidas: **4129 de 5000**

**Estimador por Método de Momentos (`alpha_tilde`):**
- Media: **0.6696887**
- Varianza: **0.04300503**
- Varianza teórica: **0.06964286**

**Estimador por Máxima Verosimilitud (`alpha_hat`):**
- Media: **0.6935898**
- Varianza: **0.04465401**

**Eficiencia relativa empírica:**
- **1.038344**

**Gráfica.**
![Gráfica de estimadores Gamma](images/Screenshot%202025-03-20%20at%2011.40.37 a.m..png)
