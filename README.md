
# Análisis de Deserción de Clientes (Churn) en TelecomX

Este notebook realiza un análisis detallado sobre los factores que impulsan la pérdida de clientes (Churn) en TelecomX utilizando el conjunto de datos **TelecomX_Data.json**. El objetivo es identificar patrones críticos y proporcionar recomendaciones que ayuden a mejorar las estrategias de retención de clientes.

## Objetivo del Proyecto

Este proyecto tiene como objetivo transformar los datos crudos en información estratégica para comprender los motivos de la deserción de clientes y ofrecer recomendaciones basadas en datos para mejorar la retención. A través de este análisis, se busca ayudar a la compañía a mitigar la pérdida de clientes, especialmente durante los primeros meses de suscripción.

## Estructura del Proyecto

1. **Limpieza y Preprocesamiento de Datos**:

   * Normalización del archivo JSON para estructurar los datos de manera tabular.
   * Creación de nuevas variables, como `Cuentas_Diarias`, que dividen el costo mensual entre 30 para obtener una visión más precisa del gasto diario por cliente.
   * Depuración de los datos eliminando registros con valores vacíos en columnas críticas como `Churn`.

2. **Análisis Exploratorio de Datos**:

   * Identificación de la "fuga temprana", destacando que la mayoría de los clientes abandonan antes de cumplir su primer año.
   * Análisis de los diferentes tipos de contratos y su relación con la tasa de abandono. Los contratos a corto plazo (mes a mes) muestran una tasa de deserción significativamente mayor.

3. **Análisis de Sensibilidad al Precio**:

   * Evaluación de la relación entre el costo mensual de los usuarios y su decisión de abandonar el servicio. Se detectó que los clientes con cargos más altos (por encima de los 70 USD) son mucho más propensos a cancelar el servicio.

4. **Recomendaciones para Mejorar la Retención**:

   * Implementación de alertas para clientes con cargos superiores a 70 USD, lo que podría ayudar a identificar clientes con mayor riesgo de deserción.
   * Mejora de la experiencia del cliente en los primeros meses, especialmente entre el mes 6 y 10, cuando se produce la mayor parte de la deserción.
   * Ofrecer incentivos para contratos a largo plazo, lo cual mejora significativamente la retención de clientes.

## Requisitos

Este análisis fue realizado con las siguientes bibliotecas de Python:

* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `json`

Puedes instalar las dependencias necesarias con el siguiente comando:

```bash
pip install -r requirements.txt
```

## Instrucciones de Uso

1. **Carga de Datos**:
   Asegúrate de tener el archivo `TelecomX_Data.json` en la misma carpeta que este notebook o modifica la ruta de carga según sea necesario.

2. **Ejecutar el Notebook**:
   Ejecuta cada celda para realizar el análisis y ver los resultados.

3. **Explora los Resultados**:
   El análisis incluye varias visualizaciones y métricas clave sobre el comportamiento de deserción y la sensibilidad al precio. Al final, encontrarás las recomendaciones clave para mejorar las estrategias de retención.

## Recomendaciones

Algunas recomendaciones clave extraídas del análisis:

* Enfocar las estrategias de retención en los primeros 6 a 10 meses de vida del cliente, cuando es más probable que abandonen.
* Evaluar la competitividad de los precios, especialmente para los servicios premium, que parecen ser un factor de deserción importante.
* Utilizar los datos sobre tipos de contratos para diseñar campañas que fomenten contratos a largo plazo, los cuales muestran mayor retención.
