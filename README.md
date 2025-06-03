### ¿Por qué dejan de asistir al gimnasio? Un análisis de datos reales en Model Fitness

#### Objetivo del proyecto
Identificar los factores clave que indican la pérdida de clientes en Model Fitness mediante el análisis de datos de asistencia y perfiles digitales, con el fin de:

- Detectar señales tempranas de abandono

- Diseñar estrategias de retención basadas en datos

- Mejorar la fidelización y prolongar la relación cliente-gimnasio

#### Lenguaje de programación, librerías y habilidades
![Python](https://img.shields.io/badge/PYTHON-%232A5D9F.svg?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/PANDAS-%232A5D9F.svg?style=for-the-badge&logo=pandas&logoColor=white)
![SciPy](https://img.shields.io/badge/SCIPY-%232A5D9F.svg?style=for-the-badge&logo=scipy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/SCIKIT--LEARN-%232A5D9F.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/MATPLOTLIB-%232A5D9F.svg?style=for-the-badge&logo=plotly&logoColor=white)
![Seaborn](https://img.shields.io/badge/SEABORN-%232A5D9F.svg?style=for-the-badge&logo=seaborn&logoColor=white)
![Limpieza de Datos](https://img.shields.io/badge/LIMPIEZA%20DE%20DATOS-%233B7DD8.svg?style=for-the-badge&logoColor=white)
![Análisis de Datos](https://img.shields.io/badge/ANÁLISIS%20DE%20DATOS-%233B7DD8.svg?style=for-the-badge&logoColor=white)
![Modelos de Predicción](https://img.shields.io/badge/MODELOS%20DE%20PREDICCIÓN-%233B7DD8.svg?style=for-the-badge&logoColor=white)
![Visualización de Datos](https://img.shields.io/badge/VISUALIZACIÓN%20DE%20DATOS-%233B7DD8.svg?style=for-the-badge&logoColor=white)

#### Preguntas clave
- ¿Qué características diferencian a los clientes leales de los que abandonan?

- ¿Qué tan efectivo es un modelo predictivo para anticipar la cancelación de usuarios?

- ¿Cómo se pueden segmentar los clientes para diseñar estrategias personalizadas de retención?

#### Metodología
- **Preprocesamiento de datos:** Se limpiaron y estandarizaron los datos, se eliminaron duplicados y se manejaron valores ausentes para asegurar la calidad del análisis.

- **Análisis exploratorio de datos (EDA):** Se analizaron estadísticas descriptivas y distribuciones. Se compararon características de clientes que permanecieron frente a los que cancelaron, y se exploraron correlaciones entre variables.

- **Modelado predictivo:** Se entrenaron modelos de clasificación binaria (regresión logística y bosque aleatorio) para predecir la probabilidad de cancelación en el siguiente mes. Se evaluó el desempeño con métricas como precisión, exactitud y recall.

- **Clustering:** Se segmentaron los clientes en grupos utilizando K-means para identificar comportamientos similares y calcular las tasas de cancelación por clúster.

#### Conclusiones generales
- Se identificaron cinco clústeres de usuarios con características distintas en edad, visitas, duración de membresía, gastos y tasa de cancelación.

- El clúster 3 tiene la tasa de cancelación más alta; el clúster 2 la más baja, mostrando mayor lealtad.

- El clúster 4 agrupa a usuarios jóvenes y frecuentes; el clúster 2 gasta más en cargos adicionales, mientras que el 3 gasta menos y es más propenso a cancelar.

#### Recomendaciones para la estrategia de retención

- **Clúster 3** – Alta cancelación: Mejorar experiencia con clases gratuitas y descuentos; brindar atención personalizada para entender motivos de baja.

- **Clúster 2** – Alta lealtad: Ofrecer beneficios exclusivos y servicios premium personalizados.

- **Clúster 4** – Jóvenes con alta frecuencia: Diseñar promociones y contratos flexibles; reforzar programas de referidos.

- **Clúster 1** – Buena retención: Recompensar antigüedad y adaptar servicios a sus necesidades mediante encuestas.

- **Clúster 0** – Cancelación moderada: Combinar retención y adquisición con promociones atractivas.

#### Diccionario de datos
Model Fitness aportó archivos CSV que contienen los datos sobre la cancelación de un mes en concreto e información del mes que lo precedía. El dataset incluye los siguientes campos:

- `'Churn'` — la cancelación para el mes en cuestión

- Campos de dataset actuales:

  - Datos del usuario del mes anterior

    - `'gender'`.
    
    - `'Near_Location'` — si el/la usuario/a vive o trabaja en el vecindario donde se encuentra el gimnasio.

    - `'Partner'` — si el/la usuario/a trabaja en una compañía asociada (el gimnasio tiene empresas asociadas cuyos empleados obtienen descuentos; en esos casos el gimnasio almacena información sobre los empleadores de los clientes).

    - `Promo_friends` — si el/la usuario/a originalmente se inscribió mediante una oferta “trae a un/a amigo/a” (se utilizó el código promocional de un/a amigo/a cuando pagaron el primer abono).

    - `'Phone'` — si el/la usuario/a aportó el número de teléfono.

    - `'Age'.`
    
    - `'Lifetime'` — el tiempo (en meses) desde que el/la usuario/a llegó por primera vez al gimnasio.
  
  - Datos del registro de visitas y compras y datos sobre el estado actual de la membresía:

    - `'Contract_period'` — 1 mes, 3 meses, 6 meses o 1 año.

    - `'Month_to_end_contract'` — los meses que faltan hasta que expire el contrato.

    - `'Group_visits'` — si el/la usuario/a participa en sesiones grupales.
    
    - `'Avg_class_frequency_total'` — frecuencia media de visitas por semana a lo largo de la vida del cliente.
    
    - `'Avg_class_frequency_current_month'` — frecuencia media de visitas por semana durante el mes en curso.
    
    - `'Avg_additional_charges_total'` — cantidad total de dinero gastado en otros servicios del gimnasio: cafetería, productos deportivos, cosméticos, masajes, etc.
