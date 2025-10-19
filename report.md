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

## Panorama general del uso de ML en energía

El aprendizaje automático (Machine Learning, ML) se ha convertido en una herramienta potente para abordar la complejidad de los sistemas energéticos modernos ([energyinformatics.springeropen.com](https://energyinformatics.springeropen.com)). En las últimas dos décadas ha ocurrido un aumento dramático en la aplicación de técnicas de ML en el sector energético ([mdpi.com](https://www.mdpi.com)). Los modelos de ML (excluyendo las redes neuronales profundas) abarcan métodos como árboles de decisión, bosques aleatorios (Random Forest), máquinas de vectores de soporte (SVM), modelos ensemble (p. ej., gradient boosting), y enfoques de aprendizaje por refuerzo. Estos métodos permiten extraer patrones de grandes datos dinámicos para predecir la demanda energética, estimar la generación renovable y optimizar la operación de recursos ([energyinformatics.springeropen.com](https://energyinformatics.springeropen.com)). Gracias a su precisión, rapidez y eficiencia, los modelos de ML se han vuelto esenciales en la modelización predictiva de la producción, consumo y análisis de demanda en sistemas eléctricos ([mdpi.com](https://www.mdpi.com)). La combinación de múltiples técnicas (modelos híbridos) ha demostrado mejorar la exactitud y robustez de las predicciones, especialmente en energías renovables. En suma, el estado del arte indica que las técnicas de ML no neuronales complementan y, en ciertos casos, rivalizan con los métodos basados en redes neuronales, aportando mayor interpretabilidad y menores requerimientos computacionales en aplicaciones clave de la transición energética ([orca.cardiff.ac.uk](https://orca.cardiff.ac.uk)).

## Predicción de demanda y generación eléctrica

Los métodos de ML tradicionales se han aplicado ampliamente para pronosticar el consumo energético a corto y mediano plazo. Algoritmos como bosques aleatorios y boosting (XGBoost) logran alta precisión en pronósticos de carga horaria mediante modelos ensemble ([arxiv.org](https://arxiv.org)). Las SVM se han usado eficazmente para pronóstico solar y eólico, con errores medios de ~4%, comparables a redes neuronales ([pmc.ncbi.nlm.nih.gov](https://pmc.ncbi.nlm.nih.gov)). Modelos basados en árboles y bosques aleatorios también son efectivos para predicción energética a nivel de edificios, con ventajas como bajo requerimiento de ajuste y manejo de variables categóricas ([orca.cardiff.ac.uk](https://orca.cardiff.ac.uk)). En la predicción de generación renovable, se ha demostrado que modelos SVM híbridos y Random Forest pueden mejorar estabilidad y reducir error de predicción ([researchgate.net](https://researchgate.net)).

## Planificación y operación del sistema eléctrico

Árboles de decisión se han utilizado para planificar microredes y respaldar el despacho de seguridad en sistemas eléctricos con gas natural, proporcionando reglas interpretables y resiliencia ante contingencias ([mdpi.com](https://www.mdpi.com)). Técnicas de aprendizaje por refuerzo (RL), incluso sin redes neuronales, se aplican para optimizar programación de recursos distribuidos y respuesta a la demanda, con capacidad de adaptación a incertidumbre ([energyinformatics.springeropen.com](https://energyinformatics.springeropen.com)). Modelos predictivos no neuronales también ayudan a estimar potencia no servida y ajustar requerimientos de reserva operativa.

## Análisis de políticas y escenarios energéticos

Árboles optimizados (boosted trees) permiten identificar factores que impulsan la transición energética (políticas, costos, estructuras de mercado). Por ejemplo, Alova y Caldecott (2021) usaron CatBoost para analizar 20 años de datos en 33 países, cuantificando el efecto de políticas sobre la expansión de capacidad renovable ([researchgate.net](https://researchgate.net)). También se emplean algoritmos de clasificación, clustering y metamodelos para explorar miles de escenarios y predecir eventos como el pico de emisiones. Estos métodos detectan no linealidades clave en la evolución del sistema energético ([sciencedirect.com](https://www.sciencedirect.com), [nature.com](https://www.nature.com)).

Finalmente, ML apoya políticas adaptativas mediante análisis de grandes volúmenes de datos históricos, modelando demanda a largo plazo y balanceando objetivos económicos, sociales y ambientales, especialmente en países en desarrollo ([mdpi.com](https://www.mdpi.com)).

## Referencias

1. Lahouar & Slama (2015). DOI: 10.1016/j.enconman.2015.07.041  
2. Moutis et al. (2016). DOI: 10.1016/j.apenergy.2015.10.017  
3. Ahmad et al. (2017). DOI: 10.1016/j.enbuild.2017.04.038  
4. Mosavi et al. (2019). DOI: 10.3390/en12071301  
5. Donti & Kolter (2021). DOI: 10.1146/annurev-environ-020220-061831  
6. Alova & Caldecott (2021). DOI: 10.1016/j.isci.2021.102929  
7. Yao et al. (2023). DOI: 10.1038/s41578-022-00490-5  
8. Yang et al. (2020). DOI: 10.1016/j.arcontrol.2020.04.015  
9. Arslan Tuncar et al. (2024). DOI: 10.1016/j.egyr.2024.06.006  
10. Atiç & Izgi (2024). DOI: 10.3390/su16125193  
11. Aslam et al. (2025). DOI: 10.1186/s42162-025-00524-6  


## **Planeación: tareas y cronograma** ##