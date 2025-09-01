# Dashboard de Gestión y Mantenimiento de Flota Vehicular en Power BI

![Banner del Proyecto]() 

## 📜 Resumen del Proyecto

Este proyecto presenta un dashboard de Business Intelligence desarrollado íntegramente en Power BI para el análisis, monitoreo y gestión de una flota vehicular. Utilizando un dataset público de Kaggle que simula los registros de mantenimiento de vehículos, el objetivo es transformar datos operativos crudos en insights accionables que permitan a un gerente de flota optimizar costos, mejorar la planificación del mantenimiento y aumentar la fiabilidad de los activos.

**El dashboard interactivo permite identificar rápidamente vehículos en riesgo, analizar el estado general de la flota y detectar patrones en el historial de mantenimiento.**

---

## 🎯 El Problema de Negocio

La gestión eficiente de una flota vehicular es un desafío operativo complejo. Sin una visión centralizada de los datos, los gerentes enfrentan dificultades para:
*   Identificar proactivamente qué vehículos necesitan mantenimiento.
*   Entender la salud general y la condición de los componentes clave (neumáticos, frenos, batería).
*   Analizar la relación entre el historial de mantenimiento, la edad del vehículo y los problemas reportados.
*   Tomar decisiones basadas en datos para optimizar la gestión de garantías y los costos de seguro.

---

## 📊 La Solución: Un Dashboard de BI en Power BI

Se desarrolló un dashboard interactivo en Power BI que consolida y visualiza los datos de la flota para responder a estas preguntas.

### Vista General del Dashboard
*(La página principal ofrece un resumen ejecutivo del estado de la flota, destacando los KPIs más importantes y los vehículos que requieren atención inmediata.)*

![Vista General del Dashboard]()

### Análisis de Mantenimiento y Condición
*(Esta sección permite un análisis más profundo sobre la condición de los componentes y la relación entre el historial de mantenimiento y los problemas actuales.)*

![Vista de Mantenimiento]()

---

## 🔧 Proceso de Datos y Características Clave

1.  **Limpieza y Transformación (Power Query):**
    *   Se corrigieron los tipos de datos, asegurando que las fechas y los valores numéricos fueran interpretados correctamente.
    *   Se manejaron los registros incompletos para garantizar la calidad de los datos.

2.  **Ingeniería de Características (Feature Engineering):**
    *   Se crearon columnas calculadas clave para enriquecer el análisis, como:
        *   **`Dias_Desde_Ultimo_Mantenimiento`**: Calculado usando la fecha máxima del dataset como referencia temporal para identificar los vehículos más desatendidos.
        *   **`Estado_Garantia`**: Una columna condicional ("Vigente" / "Expirada") para facilitar la segmentación y el análisis de costos.
        *   **`Necesita Mantenimiento (Texto)`**: Se transformó la variable binaria (0/1) a etiquetas claras ("Sí"/"No") para mejorar la legibilidad en las visualizaciones.

3.  **Cálculos y KPIs (DAX):**
    *   Se desarrollaron medidas DAX para calcular los principales indicadores de rendimiento, incluyendo:
        *   `Total Vehículos`
        *   `% de Vehículos que Necesitan Mantenimiento`
        *   `Edad Promedio de la Flota`
        *   `Costo de Seguro Promedio`

---

## 🛠️ Herramientas Utilizadas

*   **Microsoft Power BI:**
    *   **Power Query:** Para la extracción, limpieza y transformación de los datos (ETL).
    *   **DAX (Data Analysis Expressions):** Para la creación de KPIs y medidas calculadas.
    *   **Visualización:** Para el diseño del dashboard interactivo.


---

## 🚀 Cómo Explorar este Repositorio

*   **/data/vehicle_maintenance_data.csv**: Contiene el dataset original utilizado en el proyecto.
*   **/images/**: Carpeta con las capturas de pantalla del dashboard utilizadas en esta documentación.
*   **mantenimiento de vehículos.pbix**: El archivo fuente de Power BI con el modelo de datos, las medidas y el informe completo.
