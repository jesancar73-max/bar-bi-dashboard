# 🍸 Dashboard BI — Análisis de Negocio (Bar, 2015–2025)

## 📌 Contexto

Negocio real de hostelería con 10 años de actividad. Los socios se plantean la opción de dejar de gestionar el negocio de forma intuitiva y tener una visión clara y centralizada de la evolución financiera y operativa: ventas, gastos, rentabilidad, aforo y productividad del personal. Nota: Este proyecto está realizado con datos sintetizados de los datos reales.

## 🎯 Objetivo

Diseñar e implementar un sistema de Business Intelligence completo en entorno local que permitiera a los socios monitorizar la evolución del negocio durante 10 años y tomar decisiones basadas en datos reales.

## 🏗️ Arquitectura del sistema

El sistema sigue una arquitectura profesional de extremo a extremo:

Excel origen → Power Query ETL → Modelo estrella DAX → Dashboard Power BI

**Tablas de dimensiones:** Productos, Precios históricos, Proveedores, Empleados, Calendario

**Tablas de hechos:** Ventas, Gastos, Caja diaria, Aforo, Turnos de personal

## 🔧 Proceso técnico

| Fase | Descripción |
|------|-------------|
| Extracción | Datos históricos reales registrados en Excel durante 10 años |
| Transformación | Limpieza y estructuración con Power Query. Separación de datos maestros y operacionales |
| Modelado | Modelo estrella con 5 tablas de hechos y 5 dimensiones. Medidas DAX para todos los KPIs |
| Despliegue | Entorno local con control de versiones DEV/TEST/PROD y sistema de backups |
| Mantenimiento | Changelog estructurado, manual de usuario y diccionario de datos y KPIs |

## 📋 KPIs implementados

| KPI | Descripción |
|-----|-------------|
| Ventas totales | Ingresos del periodo filtrado |
| Margen bruto % | Ventas menos coste de producto |
| Resultado operativo | Margen bruto menos gastos totales |
| Aforo total | Clientes atendidos en el periodo |
| Ticket medio | Ventas por cliente |
| Caja neta | Ingresos menos gastos de caja |
| Ventas por hora trabajada | Productividad del personal |
| Evolución YoY | Comparativa año sobre año |
| Evolución PVP y coste unitario | Análisis de presión de márgenes por año |

## 💼 Valor para el negocio

El sistema permitió a los socios pasar de la gestión intuitiva al análisis basado en datos, identificar los productos y categorías con mayor y menor rentabilidad a lo largo de la década, detectar tendencias estacionales y tomar decisiones sobre precios, personal y surtido con base objetiva.

## 🛠️ Stack tecnológico

`Power BI Desktop` `Power Query` `DAX` `Modelo Estrella` `Excel` `Control de versiones local`

## 📁 Estructura del repositorio

- README.md
- data/ → DATOS_MAESTROS.xlsx, DATOS_OPERACIONALES.xlsx
- report/ → Dashboard_Tandem_PROD.pbix
- docs/ → Diccionario_Datos_y_KPIs.pdf, Manual_Operacion_Usuario.pdf, Presentacion_Dashboard.pptx, changelog.xlsx
