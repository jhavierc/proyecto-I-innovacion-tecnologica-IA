## 1. Primera entrega - Reporte de la primera etapa (20%) 
- Análisis del problema: identificación clara del problema, objetivos y árbol de problemas (10%) 
- Estado del arte: revisión bibliográfica y análisis de soluciones existentes (5%) 
- Planeación: tareas y cronograma (5%) 

## **Análisis del Problema** ##

## **Problema central**
La transición energética global desde fuentes fósiles hacia energías limpias continúa siendo desigual, lenta y difícil de predecir. A pesar de la disponibilidad de datos históricos sobre producción energética, emisiones y políticas, estos no se integran de manera efectiva para anticipar escenarios y apoyar decisiones estratégicas.

## **Pregunta problema**
¿Cómo puede el uso de modelos de *Machine Learning* mejorar la predicción y el análisis de la transición energética global, permitiendo evaluar la evolución por país y apoyar la toma de decisiones en materia de política energética y sostenibilidad?

## **Árbol de problemas**

### **Problema principal**
Falta de herramientas predictivas para planificar la transición energética.

### **Causas**
- Datos energéticos dispersos y desestructurados.  
- Alta interdependencia de factores económicos, tecnológicos y políticos.  
- Escasa aplicación de *Machine Learning* en la predicción energética a nivel global.  

### **Consecuencias**
- Políticas públicas reactivas.  
- Inversiones con alto riesgo.  
- Desigualdad en la adopción de energías limpias.  

## **Objetivo general**
Desarrollar un modelo de *Machine Learning* que prediga la evolución de la producción energética por fuente y país, facilitando la planificación de la transición hacia energías renovables.

## **Objetivos específicos**
1. Analizar tendencias históricas de generación energética global utilizando el dataset de producción eléctrica por fuente.  
2. Preprocesar y estructurar los datos para el entrenamiento de modelos.
3. Diseñar y comparar modelos predictivos.  
4. Evaluar su precisión mediante métricas como RMSE, R² y MAE.  
5. Visualizar resultados y proyecciones por región para facilitar la interpretación y la toma de decisiones.  

## **Estado del arte: Modelos de Machine Learning en la Transición Energética** ##

### Contexto

La transición energética global implica reemplazar fuentes fósiles por energías limpias para reducir emisiones de carbono. Este cambio ha aumentado significativamente la participación de renovables en muchas matrices eléctricas, lo que introduce desafíos de variabilidad e incertidumbre. En este contexto, los métodos de *Machine Learning* (ML) han surgido como herramientas potentes para predecir generación, demanda y optimizar la operación de sistemas eléctricos. 

A diferencia de modelos estadísticos tradicionales, los algoritmos de ML pueden aprender patrones no lineales en grandes volúmenes de datos históricos. En particular, los modelos de ML **no neuronales** (como árboles de decisión, SVM y ensambles como XGBoost) ofrecen ventajas como mayor interpretabilidad y menor requerimiento computacional, siendo muy útiles en la planificación energética.

---

### Aplicaciones de ML en la transición energética

Las aplicaciones de ML no neuronales se centran principalmente en:

- **Predicción de generación renovable:** Modelos como Random Forest, SVM o XGBoost se han aplicado exitosamente a la predicción de producción eólica y solar. Estudios recientes han alcanzado coeficientes *R²* cercanos a 0.99 en predicciones horarias, utilizando modelos ensemble bien calibrados.

- **Pronóstico de demanda eléctrica:** Estos modelos también se usan para anticipar picos de carga, facilitando el balance oferta-demanda y la planificación del despacho.

- **Mantenimiento predictivo y redes inteligentes:** El ML permite detectar patrones de fallo antes de que ocurran, mejorando la fiabilidad del sistema.

- **Análisis de escenarios y políticas:** Herramientas de boosting se han utilizado para identificar los factores que impulsan la transición energética a nivel país o empresa.

Ejemplos reales incluyen:
- Google, que optimizó la producción eólica usando ML y aumentó en 20% el valor comercial de esa energía.
- AEMO (Australia), que implementó sistemas ML para mejorar la estabilidad de la red.

---

### Modelos más usados

Entre los modelos más populares se destacan:

- **Árboles de decisión y Random Forest:** Por su capacidad de manejar relaciones complejas y su buena explicabilidad.
- **Gradient Boosting / XGBoost:** Muy precisos en tareas con alta dimensionalidad y variabilidad. Útiles en forecasting y análisis de impacto de políticas.
- **SVM / SVR:** Robustas ante ruido y efectivas con pocos datos. Usadas en pronóstico solar y eólico.
- **k-NN y procesos gaussianos:** Menos frecuentes pero útiles en tareas específicas.

Los **ensambles y modelos híbridos** (combinación de varios métodos) son particularmente efectivos para mejorar precisión y robustez. También se exploran enfoques que integran conocimiento físico con ML para mejorar la generalización.

---

### Desafíos

A pesar de sus beneficios, hay varios retos que aún deben superarse:

- **Intermitencia y datos no estacionarios:** Las fuentes renovables son altamente variables y los modelos deben adaptarse a estos cambios.
- **Falta de datos de calidad:** En muchas regiones, la infraestructura de monitoreo es insuficiente para alimentar modelos precisos.
- **Interpretabilidad:** Aunque algunos modelos son más explicables, todavía se trabaja en traducir resultados complejos a recomendaciones claras.
- **Integración en la operación real:** Las predicciones deben ser confiables, rápidas y seguras para incorporarse en decisiones críticas del sistema eléctrico.

---

### Conclusión

El uso de modelos de ML no neuronales se ha consolidado como una herramienta eficaz y cada vez más adoptada para apoyar la transición energética. Su aplicación en predicción, planificación y análisis de políticas permite operar sistemas más sostenibles, seguros y eficientes. Sin embargo, su efectividad depende de la calidad de datos, capacidad de adaptación y aceptación por parte de los operadores.

---

### Referencias

1. Rajaperumal, T. A., & Columbus, C. C. (2025). *Enhanced wind power forecasting using machine learning...* Scientific Reports, 15, Art. 20572.  
2. Alazemi, T., et al. (2024). *Renewable energy sources integration via machine learning modelling...* Heliyon, 10(4), e026088.  
3. Rhafes, M. Y., et al. (2025). *Machine learning models in renewable energy forecasting...* IJEECS, 37(3), 1874–1886.  
4. Lindas, É., et al. (2025). *Towards accurate forecasting of renewable energy...* arXiv:2504.16100.  
5. Aslam, S., et al. (2025). *Machine learning applications in energy systems...* Energy Informatics, 8, Art. 62.  
6. Ejiyi, C. J., et al. (2025). *AI in renewable energy systems...* Journal of Big Data, 12, Art. 169.  
7. Demolli, H., et al. (2019). *Wind power forecasting based on daily wind speed...* Energy Conv. & Mgmt, 198, 111823.  
8. Lai, J.-P., et al. (2020). *Survey of machine learning in renewable energy...* Applied Sciences, 10(17), 5975.  
9. Sweeney, C., et al. (2019). *The future of forecasting for renewable energy.* WIREs Energy & Environment, 9(2), e365.  
10. Chen, X., et al. (2019). *Transition towards higher penetration of renewables...* JMPSE, 7(1), 1–8.  
11. Benti, N. E., et al. (2023). *Forecasting renewable energy with ML...* Sustainability, 15(9), 7087.  
12. Wang, H., et al. (2019). *A review of deep learning for renewable energy forecasting.* ECM, 198, 111799.  
13. Aslam, S., et al. (2021). *A survey on DL methods for energy forecasting.* RSE Reviews, 144, 110992.  


## **Planeación: tareas y cronograma** ##