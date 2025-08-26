Predicción de insolvencia de las 500 empresas colombianas más importantes a partir de sus perfiles financieros.

Objetivo

Predecir la probabilidad de insolvencia o quiebra de las 500 empresas más importantes de Colombia, a partir de su información financiera disponible, con el fin de facilitar un diagnóstico temprano del riesgo empresarial, fortalecer la toma de decisiones financieras al interior de las organizaciones y proporcionar información relevante a inversionistas, acreedores y aliados estratégicos interesados en evaluar la estabilidad y sostenibilidad de dichas empresas.

Descripción

Este proyecto tiene como objetivo construir una herramienta predictiva, basada en técnicas de inteligencia artificial, capaz de anticipar la probabilidad de quiebra o insolvencia de las 500 empresas más grandes e importantes de Colombia. Para ello, se implementará un enfoque en dos etapas complementarias:
1.	Segmentación financiera de las empresas: A partir de indicadores clave como liquidez, rentabilidad, apalancamiento, utilidades, entre otros, se buscará clasificar a las empresas según su perfil financiero utilizando técnicas de aprendizaje no supervisado, como las técnicas de K-means y análisis exploratorio de datos. Esta segmentación permitirá identificar patrones comunes entre grupos de empresas y facilitará el entendimiento de sus características financieras.
2.	Predicción del riesgo de insolvencia: En una segunda fase, se aplicarán técnicas de aprendizaje supervisado, particularmente el modelo Random Forest, con el fin de identificar patrones asociados a situaciones de quiebra o crisis financiera. Este modelo permitirá anticipar riesgos mediante el análisis de variables históricas y estructurales de las empresas, generando alertas tempranas que pueden ser útiles tanto para la gestión interna como para actores externos.

Desafíos

El proyecto presenta múltiples desafíos que deben ser considerados desde el inicio. Uno de los más evidentes es su estructura en dos etapas: una fase inicial de aprendizaje no supervisado, orientada a segmentar las empresas según su perfil financiero, y una segunda fase de aprendizaje supervisado, enfocada en predecir la probabilidad de insolvencia. Esta combinación lo convierte en un proyecto ambicioso, pero con un alto potencial de generación de valor.
Otro desafío importante radica en la disponibilidad y accesibilidad de información financiera completa y confiable para cada empresa, especialmente considerando el elevado número de entidades que se pretende analizar. La calidad, consistencia y nivel de detalle de los datos será un factor determinante para el éxito del modelo.
Adicionalmente, la definición de la variable objetivo (la probabilidad de insolvencia o quiebra) implica establecer criterios financieros sólidos y bien justificados. La construcción de este indicador de riesgo deberá fundamentarse en metodologías reconocidas y métricas adecuadas que garanticen su validez.
Finalmente, se debe considerar que la técnica de clasificación seleccionada, el modelo de Random Forest, aunque eficaz en términos de precisión, puede presentar limitaciones en cuanto a su interpretabilidad. Debido a que se basa en la combinación de múltiples árboles de decisión, cada uno con diferentes trayectorias, puede resultar difícil rastrear y explicar con claridad cómo se llegó a una predicción específica, lo cual puede representar un obstáculo en escenarios donde la transparencia del modelo es crítica.

Puesta de Valor

Este proyecto pone en valor la información financiera reportada por las 500 empresas más importantes de Colombia, mediante la aplicación de técnicas avanzadas de machine learning. A través de este enfoque, se busca identificar perfiles financieros diferenciados y predecir la probabilidad de insolvencia de manera más precisa y anticipada.
Los resultados generarán insumos valiosos para la gestión del riesgo financiero y la toma de decisiones estratégicas, no solo para las propias empresas, sino también para sus accionistas, posibles inversionistas y otros actores del entorno empresarial. Esta capacidad de anticipación y segmentación puede convertirse en una herramienta clave para prevenir crisis financieras, optimizar recursos y fomentar decisiones de inversión más informadas.

Stakeholders del proyecto

El proyecto de predicción de insolvencia involucra a diferentes actores con intereses específicos:
Empresas analizadas: Buscan conocer su posición de riesgo financiero y compararse con otras del mismo sector.
Directivos y gerentes financieros: Requieren información anticipada para mejorar la toma de decisiones internas y fortalecer estrategias de sostenibilidad.
Inversionistas y acreedores: Necesitan señales tempranas de quiebra para reducir pérdidas, diversificar riesgos y optimizar portafolios.
Entidades de supervisión Entidades interesadas en el diagnóstico temprano para vigilancia prudencial.
Docentes y equipo académico: Interesados en la validez metodológica, trazabilidad y aplicabilidad de las técnicas de IA empleadas.
Equipo técnico de ciencia de datos: Responsable de la calidad de la información, construcción de variables y validación del desempeño de los modelos.

Técnicas a utilizar en el estudio de los datos

1.	Segmentación financiera (no supervisada)
o	Uso de K-means y análisis exploratorio de datos (EDA) para identificar patrones comunes en liquidez, rentabilidad, apalancamiento, etc.
o	Complementado con análisis de correlaciones, reducción de dimensiones (PCA) y validación de la coherencia de los grupos.
2.	Predicción del riesgo de insolvencia (supervisada)
o	Aplicación de Random Forest, un algoritmo robusto para clasificación que permite detectar relaciones no lineales entre variables financieras.
o	Posible comparación con modelos base (Regresión Logística, Gradient Boosting) para validar desempeño.
o	Se utilizarán métricas de evaluación como ROC-AUC, Precision-Recall y calibración para medir la calidad predictiva.
3.	Interpretabilidad del modelo
o	Uso de técnicas como SHAP values para explicar la contribución de cada variable en la predicción de insolvencia.

Fuente de los datos

La información analizada en este proyecto se extrae del informe anual de la Superintendencia de Sociedades, publicado el 26 de junio de 2025. Este reporte reúne datos financieros con corte al 31 de diciembre de 2024 reportados por las empresas vigiladas por dicha entidad y continene variables fundamentales como ingresos operacionales, utilidades, activos, pasivos y patrimonio, esenciales para caracterizar el desempeño empresarial y construir indicadores claves para la segmentación y predicción de riesgo de insolvencia.

Variables 

El análisis utilizará tanto variables originales de la base como derivadas:
•	Identificación y clasificación:
o	NIT, Razón social, Supervisor, Región/Departamento/Ciudad, CIIU, Macrosector.
•	Variables financieras originales:
o	Ingresos operacionales, Activos totales, Pasivos, Patrimonio, Utilidades (operacional y neta).
•	Variables derivadas:
o	Liquidez: Activos corrientes/Pasivos corrientes (si disponible).
o	Apalancamiento: Pasivos/Activos, Activos/Patrimonio.
o	Rentabilidad: ROA = Utilidad neta/Activos; ROE = Utilidad neta/Patrimonio; Margen neto = Utilidad neta/Ingresos.
o	Eficiencia: Rotación de activos = Ingresos/Activos.
o	Crecimiento: variación porcentual de ingresos y utilidades (si hay datos de años previos).
o	Variables binarias de riesgo: patrimonio negativo, márgenes negativos, niveles altos de apalancamiento.
Estas variables permitirán caracterizar a las empresas y formar grupos homogéneos en la etapa de segmentación y alimentar el modelo predictivos de insolvencia.
