# GrowthInsight — Evaluación y Predicción Empresarial

GrowthInsight es una aplicación web de página única diseñada para ayudar a las empresas a analizar su rendimiento histórico y predecir tendencias futuras clave. Permite a los usuarios cargar sus propios datos para generar visualizaciones interactivas y obtener proyecciones basadas en modelos estadísticos simples.

## 🎯 Objetivo

El objetivo principal de GrowthInsight es proporcionar a los dueños de negocios y analistas una herramienta sencilla y poderosa para:
- **Evaluar el estado actual de la empresa** a través de indicadores clave de rendimiento (KPIs) y gráficos históricos.
- **Identificar tendencias** en áreas críticas como el crecimiento de la plantilla, los ingresos, los gastos y la rotación de personal.
- **Predecir el rendimiento futuro** bajo diferentes escenarios (optimista, realista, conservador) para facilitar la toma de decisiones estratégicas.
- **Generar reportes consolidados** que puedan ser compartidos fácilmente.

## ✨ Características Principales

- **Carga de Datos Simplificada:** Sube tus datos de empleados y finanzas a través de archivos CSV directamente en el navegador.
- **Dashboard Interactivo:**
    - **Tarjetas de KPI:** Métricas clave como número de empleados, ingresos del último mes y tasa de rotación.
    - **Gráficos Históricos:** Visualiza la evolución de empleados, la comparación de ingresos vs. gastos y las tendencias de contratación vs. salidas.
- **Módulo de Predicción Avanzado:**
    - **Modelo de Regresión Lineal:** Para proyectar tendencias de empleados e ingresos.
    - **Análisis de Escenarios:** Ajusta las predicciones a un escenario conservador, realista u optimista.
    - **Bandas de Confianza:** Visualiza el rango de incertidumbre de la predicción para una evaluación más precisa.
- **Gráficos Complementarios:** Analiza la tasa de crecimiento mensual (histórica y proyectada) para entender la velocidad del cambio.
- **Alertas Tempranas:** Recibe notificaciones si la tasa de rotación es muy alta o si los gastos crecen más rápido que los ingresos.
- **Generación de Reportes en PDF:** Exporta un informe completo con un solo clic, incluyendo KPIs, todos los gráficos (históricos y predictivos) y las tablas de datos crudos.
- **Interfaz Moderna:** Diseño responsivo con tema claro y oscuro, construido con Bootstrap 5.

## 🛠️ Implementación y Stack Tecnológico

Este proyecto está construido como una **Single-Page Application (SPA)**, contenida en un único archivo `index.html`. Esto asegura la máxima portabilidad y facilidad de uso (no requiere un servidor web).

- **HTML5** y **CSS3**: Para la estructura y el estilo base.
- **JavaScript (ES6+)**: Para toda la lógica de la aplicación, incluyendo el procesamiento de datos y los modelos predictivos.
- **Bootstrap 5**: Utilizado para el layout, los componentes de la interfaz y el diseño responsivo.
- **Chart.js**: Librería empleada para generar todos los gráficos interactivos y dinámicos.
- **PapaParse**: Para procesar los archivos CSV cargados por el usuario directamente en el navegador de forma eficiente.
- **jsPDF** y **jsPDF-AutoTable**: Utilizadas para generar los reportes profesionales en formato PDF.

## 🚀 Cómo Utilizar

1.  **Abrir la Aplicación**: Simplemente abre el archivo `index.html` en un navegador web moderno (como Google Chrome, Mozilla Firefox, Microsoft Edge).

2.  **Cargar los Datos**:
    - En el Dashboard, localiza la sección **"Cargar Datos (CSV)"**.
    - **Archivo de Empleados**: Haz clic para seleccionar tu archivo CSV. Debe contener las siguientes columnas:
        - `ID`: Identificador único del empleado.
        - `fecha_ingreso`: Fecha en que el empleado se unió a la empresa (formato `YYYY-MM-DD`).
        - `fecha_salida`: Fecha en que el empleado dejó la empresa (formato `YYYY-MM-DD`). *Dejar en blanco si el empleado sigue activo*.
        - `rol`: Puesto del empleado.
        - `area`: Departamento o área del empleado.
    - **Archivo Financiero**: Haz clic para seleccionar tu archivo CSV. Debe contener las siguientes columnas:
        - `mes`: El mes al que corresponden los datos (formato `YYYY-MM` o `YYYY-MM-DD`).
        - `ingresos`: Monto total de ingresos para ese mes.
        - `gastos`: Monto total de gastos para ese mes.
    - Haz clic en el botón **"Cargar y Procesar Datos"**.

3.  **Explorar el Dashboard**:
    - Una vez cargados los datos, el dashboard se poblará automáticamente con los KPIs y los gráficos históricos.

4.  **Realizar Predicciones**:
    - Navega a la pestaña **"Predicciones"**.
    - Elige la **métrica** a predecir (Empleados o Ingresos), el **horizonte** de tiempo y el **escenario** deseado.
    - Haz clic en **"Ejecutar Predicción"**. Se mostrará un resumen del resultado y dos gráficos: la proyección con bandas de confianza y la tasa de crecimiento mensual.

5.  **Generar un Reporte**:
    - Ve a la pestaña **"Reportes"**.
    - Haz clic en **"Exportar a PDF"**. Se generará y descargará un informe completo que incluye el estado del dashboard y el último análisis predictivo realizado.
