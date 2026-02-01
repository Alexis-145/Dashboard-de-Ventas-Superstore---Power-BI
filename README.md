
# 📊 Dashboard de Ventas Superstore - Power BI

> Dashboard interactivo profesional desarrollado en Power BI aplicando modelado dimensional, DAX avanzado y mejores prácticas de visualización de datos.

## 🎯 Descripción del Proyecto

Este proyecto presenta un análisis completo de ventas utilizando el dataset Superstore, implementando un dashboard ejecutivo con navegación multi-página, KPIs dinámicos y visualizaciones interactivas profesionales.

### 🔑 Características Principales

- ✅ **Modelo de datos optimizado** - Star Schema con 4 dimensiones + 1 tabla de hechos
- ✅ **Medidas DAX** - Funciones básicas, intermedias y avanzadas
- ✅ **Time Intelligence** - Análisis YoY, YTD, comparaciones temporales
- ✅ **Navegación dinámica** - 3 páginas especializadas con botones interactivos
- ✅ **Diseño UX/UI profesional** - Interfaz limpia tipo aplicación web


## 📊 Páginas del Dashboard

### 1️⃣ Resumen de Ventas
- KPIs principales: Ventas, Ganancias, Margen, Clientes
- Tendencia temporal de ventas
- Distribución por segmento de cliente
- Indicadores de performance

### 2️⃣ ANÁLISIS DE PRODUCTOS SUPERSTORE
- Ventas por categoría y subcategoría
- Top 10 productos más vendidos
- Matriz de performance
- Análisis de rentabilidad


### 3️⃣ ANÁLISIS REGIONAL DE VENTAS
- Mapa interactivo de ventas por estado
- Performance por estado
- Ganancias por Regiónn

## 🛠️ Tecnologías y Técnicas

### Herramientas
- **Power BI Desktop** - Desarrollo del dashboard
- **DAX** - Lenguaje de análisis de datos
- **Power Query (M)** - Transformación de datos

### Técnicas Aplicadas

#### 📐 Modelado de Datos
```
Modelo Estrella (Star Schema):
- FACT_Ventas (tabla de hechos)
- DIM_Productos (productos y categorías)
- DIM_Clientes (segmentación de clientes)
- DIM_Geografia (regiones, estados, ciudades)
- DIM_Calendario (fechas con jerarquías temporales)
```

#### 📈 Medidas DAX Implementadas

**Básicas:**
- `Total Ventas`, `Total Ganancias`, `Margen %`
- `Num Clientes`, `Num Ordenes`, `Ticket Promedio`

**Con CALCULATE y FILTER:**
- `Ventas por Categoría`, `Ventas con Descuento`
- `Ordenes Rentables`, `% Ordenes Rentables`

**Time Intelligence:**
```dax
Ventas YTD = TOTALYTD([Total Ventas], DIM_Calendario[Date])

% Crecimiento YoY = 
DIVIDE(
    [Total Ventas] - [Ventas Año Anterior],
    [Ventas Año Anterior],
    0
)
```

**Avanzadas:**
```dax
Ranking Productos = 
RANKX(
    ALL(DIM_Productos[Product ID]),
    [Total Ventas],
    ,
    DESC,
    DENSE
)

## 🚀 Cómo Usar Este Proyecto

### Requisitos Previos
- Power BI Desktop (descarga gratuita desde [microsoft.com](https://powerbi.microsoft.com/desktop/))
- Windows 10 o superior (Power BI solo funciona en Windows)

## 📚 Aprendizajes Clave

Durante el desarrollo de este proyecto aprendí a:

- ✅ Diseñar modelos relacionales optimizados (Star Schema)
- ✅ Crear medidas DAX complejas con contexto de filtro
- ✅ Implementar funciones de Time Intelligence
- ✅ Desarrollar navegación multi-página profesional
- ✅ Aplicar principios de UX/UI en dashboards
- ✅ Optimizar performance de reportes

---

## 📊 Dataset

**Fuente:** Dataset público Superstore
**Período:** 2014-2024
**Registros:** ~10,000 transacciones

**Incluye:**
- Información de órdenes (Order ID, fechas)
- Productos (categorías, subcategorías)
- Clientes (segmentos)
- Geografía (regiones, estados, ciudades USA)
- Métricas (ventas, cantidad, descuentos, ganancias)
---
## 🔗 Recursos Útiles

- [Documentación Power BI](https://docs.microsoft.com/power-bi/)
- [DAX Guide](https://dax.guide/)
- [SQLBI - DAX Patterns](https://www.daxpatterns.com/)
- [Power BI Community](https://community.powerbi.com/)
---

## 👨‍💻 Autor
**Bryan Alexis Alarcon Palomino**
**👉 [ACCEDER AL DASHBOARD INTERACTIVO](https://app.powerbi.com/groups/me/reports/267479b4-238b-41d1-8716-4fbd17ec370f/031d9e431b305430c004?experience=power-bi)**

- 💼 LinkedIn: https://www.linkedin.com/in/bryan-alexis-alarcon-palomino-158670369/
- 📧 Email: alarconbrayan145@gmail.com

