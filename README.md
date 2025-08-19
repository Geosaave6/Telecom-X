# 📊 Análisis de Churn - TelecomX

## Descripción del proyecto
Este proyecto analiza la evasión de clientes (Churn) de la empresa de telecomunicaciones **TelecomX**, aplicando técnicas de **ETL y análisis exploratorio de datos (EDA)** con Python. El objetivo es identificar patrones de abandono de clientes y generar insights que ayuden a la empresa a tomar decisiones para mejorar la retención.

---

## Datos
- **Fuente:** JSON proporcionado por el curso de Alura.  
- **Archivo:** `TelecomX_Data.json`  
- **Formato:** JSON anidado con información de clientes, cuentas, servicios de internet y teléfono.

---

## Tecnologías y librerías utilizadas
- Python 3  
- Pandas  
- Matplotlib  
- Seaborn  
- Requests  
- Pandas `json_normalize` para aplanar JSON anidado

---

## Proceso ETL
1. **Extracción:** Se descargan los datos desde el JSON provisto en GitHub.  
2. **Transformación:**  
   - Se aplana el JSON con `json_normalize`.  
   - Se eliminan columnas con datos anidados (`dict` o `list`) que puedan causar errores.  
   - Se normalizan los nombres de columnas.  
   - Se convierten columnas numéricas (`tenure`, `monthlycharges`, `totalcharges`) y la variable `churn` a formatos adecuados.  
   - Se rellenan valores nulos: numéricos con mediana y categóricos con “Desconocido”.  
3. **Carga:** El DataFrame limpio está listo para análisis exploratorio y visualización.

---

## Análisis Exploratorio (EDA)
- **Distribución de Churn:** Identifica qué porcentaje de clientes se queda vs se va.  
- **Churn por tipo de contrato:** Evalúa la relación entre la duración del contrato y la evasión.  
- **Churn por servicio de internet:** Analiza el impacto del tipo de servicio en el churn.  
- **Tenure vs Churn:** Relación entre antigüedad del cliente y probabilidad de abandono.  
- **Monthly Charges vs Churn:** Cómo el gasto mensual afecta la evasión.  
- **Mapa de correlación:** Identificación de relaciones entre variables numéricas.  
- **Pie chart de Churn:** Visualización clara del porcentaje de clientes que se van vs los que se quedan.

---

## Conclusiones
1. La tasa de churn es aproximadamente **X%** de los clientes totales.  
2. Contratos mensuales muestran mayor tendencia a cancelación.  
3. Clientes con Fibra óptica tienden a irse más que los de DSL.  
4. Clientes nuevos (menos de 1 año de antigüedad) tienen mayor riesgo de churn.  
5. Clientes con facturas mensuales altas se van más que los de menor gasto.

### Recomendaciones
- Incentivar contratos a largo plazo.  
- Ofrecer planes competitivos de fibra óptica.  
- Diseñar programas de retención para clientes nuevos y de alto gasto.

---

## Uso
1. Clonar este repositorio o descargar los archivos.  
2. Subir `TelecomX_Data.json` a la misma carpeta del notebook.  
3. Ejecutar el notebook `TelecomX_Churn_Analysis.ipynb` en Google Colab o Jupyter.  
4. Revisar gráficos y conclusiones en la última sección del notebook.

