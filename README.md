# Proyectos de Estadística I — 2025

## Autores

Sharon Dayana Blanco Piedra
Mikel Rojas Rodríguez
Jojashley Chaves Aguilar
Cristopher Rodríguez Salazar
Sharon Blanco Piedra
Matthew  Carballo Lopez

## ¿De qué trata este repositorio?

Este repositorio contiene **tres proyectos de estadística** desarrollados como parte del curso de Estadística I. Cada proyecto aplica técnicas estadísticas progresivamente más avanzadas, comenzando con intervalos de confianza y terminando con modelos de regresión. Los dos primeros proyectos usan una base de datos real de vuelos de Nueva York; el tercero aborda casos variados con datos de diferentes áreas.

Todo el análisis fue programado en **R** y ejecutado en **Google Colab**.

---

## ¿Qué se hizo en cada fase?

### Fase I — Intervalos de confianza y estadística descriptiva
**Archivo:** `R_Flights.ipynb`

Usando la base de datos `nycflights13` (que contiene información de todos los vuelos que salieron de Nueva York en 2013), se construyeron intervalos de confianza para responder preguntas concretas sobre la operación aeroportuaria. Entre los análisis realizados:

- **Comparación de variabilidad entre aeropuertos**: ¿los vuelos desde JFK tienen distancias más variables que los de LaGuardia? Se aplicó una prueba de cociente de varianzas para determinarlo.
- **Análisis de una varianza**: se validó si la variabilidad en las distancias de vuelo desde el aeropuerto EWR coincide con las estimaciones internas de una aerolínea.
- **Proporciones de aerolíneas**: se estimó qué porcentaje de vuelos corresponde a United Airlines y si esa participación se mantiene estable.
- **Puntualidad entre aerolíneas**: se comparó la puntualidad entre United Airlines y JetBlue Airways para determinar si realmente hay diferencia.
- **Retrasos promedio**: se evaluó si el promedio de retraso en salidas del aeropuerto LaGuardia supera los 10 minutos (el estándar aceptable), usando distribuciones Z y T-Student.
- **Diferencia de temperaturas**: se comprobó si la temperatura promedio de julio es significativamente mayor que la de enero en Nueva York.
- **Visualizaciones**: se crearon gráficos de caja con degradado, violin plots, gráficos de barras, lollipops, radar, pastel y dona para comunicar los hallazgos.

---

### Fase II — Pruebas de hipótesis
**Archivo:** `R_Flights_II_Etapa.ipynb`

En esta fase se retomaron los mismos datos de vuelos, pero ahora aplicando **pruebas de hipótesis formales** con sus respectivos valores p, regiones de aceptación y rechazo, y conclusiones estadísticas rigurosas. Cada análisis incluye un resumen estructurado con valor observado, estadístico de prueba, grados de libertad, región de aceptación/rechazo, nivel de significancia y valor p. Entre los análisis:

- **Cociente de varianzas (F)**: prueba formal sobre si la variabilidad en distancias de JFK vs. LGA es significativamente diferente. Resultado: no se rechaza la igualdad de varianzas (p = 0.057).
- **Diferencia de medias (T-Student)**: ¿la distancia promedio de vuelos desde JFK es diferente a la de LGA? Resultado: no hay diferencia significativa (p = 0.95).
- **Una varianza (Chi-cuadrado)**: ¿la varianza de distancias desde EWR es menor que 553,200? Resultado: no se rechaza la hipótesis (p = 0.061).
- **Proporción (Z)**: ¿más del 15% de los vuelos de JFK son de United Airlines? Resultado: la proporción real es menor (~5.7%), se rechaza la afirmación.
- **Diferencia de proporciones**: comparación de puntualidad entre UA y B6. Resultado: no hay diferencia significativa.
- **Promedio con Z**: ¿el retraso promedio en LGA supera los 10 minutos? Resultado: el promedio es de ~5.8 minutos, no supera el estándar.
- **Promedio con T-Student**: ¿el tiempo promedio de vuelo desde JFK es de 150 minutos? Resultado: no se rechaza (p = 0.25).
- **Diferencia de medias con Z**: ¿la temperatura de julio supera significativamente la de enero? Resultado: sí, con altísima significancia (p ≈ 0).

---

### Fase III — Normalidad, chi-cuadrado, ANOVA y regresión
**Archivo:** `Proyecto_estadística_FASE_III.ipynb`

Esta fase es la más extensa y aborda **siete casos** independientes que cubren los temas más avanzados del curso:

**Caso 1 — Pruebas de normalidad (longitud de pie en niños):** Se analizó si los datos de longitud de pie en niños y niñas siguen una distribución normal, usando QQ-plots, pruebas de Shapiro-Wilk, Anderson-Darling, Kolmogorov-Smirnov-Lilliefors, D'Agostino-Pearson, y análisis de curtosis y simetría. Conclusión: ambos grupos son aproximadamente normales.

**Caso 2 — Pruebas de normalidad (medidas de bíceps):** Se repitió el análisis de normalidad con datos de bíceps. Conclusión: los datos no siguen una distribución normal (distribución bimodal con curtosis baja).

**Caso 3 — Prueba de independencia Chi-cuadrado:** Se determinó si el tipo de delito (homicidio, robo o asalto) está relacionado con la condición del criminal (extraño vs. conocido/pariente), usando datos del Departamento de Justicia de EE.UU. Conclusión: sí existe dependencia significativa entre ambas variables.

**Caso 4 — ANOVA (seguridad vehicular):** Se comparó la desaceleración de pecho en pruebas de choque entre autos compactos, medianos y grandes. Se aplicó ANOVA de un factor y prueba post-hoc de Tukey. Conclusión: el tamaño del vehículo sí influye en la seguridad; los autos grandes ofrecen mayor protección que los compactos.

**Caso 5 — Regresión lineal simple (edad vs. grasa corporal):** Se construyó un modelo de regresión para predecir el nivel de grasa corporal a partir de la edad. Se evaluó el modelo con R² = 0.70, pruebas de normalidad de residuos, intervalos de confianza y predicción, y prueba de significancia de la pendiente. Conclusión: la edad es un buen predictor de la grasa corporal.

**Caso 6 — Regresión lineal múltiple (publicidad vs. ventas):** Se construyeron y compararon **cuatro modelos** para predecir ventas a partir de inversión en publicidad (TV, radio, periódico). Se usaron criterios de R², AIC, análisis de residuos (paquete DALEX) y ANOVA para seleccionar el mejor modelo. Conclusión: el mejor modelo incluye TV, radio y su interacción (R² = 0.97).

**Caso 7 — Regresión no lineal (mandíbulas de venados):** Se ajustaron dos modelos no lineales (exponencial asintótico y logístico) para predecir la longitud de mandíbula según la edad en venados. Conclusión: el modelo exponencial asintótico ofrece mejor ajuste numérico.

---

## Archivos del repositorio

| Archivo | Descripción |
|---|---|
| `R_Flights.ipynb` | Fase I: intervalos de confianza y gráficos descriptivos |
| `R_Flights_II_Etapa.ipynb` | Fase II: pruebas de hipótesis formales |
| `Proyecto_estadística_FASE_III.ipynb` | Fase III: normalidad, ANOVA, chi-cuadrado y regresión |
| `Proyecto_Estadística_I 2025.pdf` | Enunciado / especificaciones de la Fase I |
| `Proyecto_Estadística_I 2025_II Fase_especificaciones.docx` | Especificaciones de la Fase II |
| `Proyecto_Estadística_I 2025_III Fase.pdf` | Especificaciones de la Fase III |

---

## Datos utilizados

- **Fases I y II**: paquete `nycflights13` de R, que contiene datos reales de 336,776 vuelos que partieron de los aeropuertos de Nueva York (JFK, LaGuardia, Newark) en 2013, incluyendo aerolínea, origen, destino, horarios, retrasos, distancia y datos meteorológicos.
- **Fase III**: datasets variados proporcionados por el curso (longitud de pie en niños, medidas de bíceps, datos de criminalidad, pruebas de choque vehicular, grasa corporal, datos de publicidad y ventas, y crecimiento de mandíbulas de venados).

---

## Tecnologías utilizadas

| Herramienta | Para qué se usó |
|---|---|
| R | Lenguaje de programación estadística para todo el análisis |
| Google Colab | Entorno de ejecución en la nube |
| nycflights13 | Paquete con la base de datos de vuelos de Nueva York |
| dplyr | Manipulación y transformación de datos |
| ggplot2 | Visualizaciones y gráficos estadísticos |
| stests | Pruebas de hipótesis especializadas |
| BSDA | Pruebas Z para medias con varianza conocida |
| DALEX | Análisis de residuos y evaluación de modelos |
| bbmle | Cálculo de criterio AIC para comparación de modelos |

---

