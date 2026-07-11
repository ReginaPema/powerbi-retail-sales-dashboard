# <img src="https://img.icons8.com/?size=50&id=cntP0u7UpRv2&format=png&color=000000" align="center"/> Power BI Dashboard: Retail Sales Analysis
### Dashboard de Ventas Retail de Productos de Limpieza

> **EN** · Interactive Power BI dashboard analyzing retail sales of cleaning products (Cloralex, Vanish, Clorox, Lysol, OxiClean) across 6 Mexican regions from Jan 2022 to Jul 2023. Built on a star schema with 5 tables and DAX measures covering revenue, units, market share and brand performance.
>
> **ES** · Dashboard interactivo en Power BI para análisis de ventas retail de productos de limpieza (Cloralex, Vanish, Clorox, Lysol, OxiClean) en 6 regiones de México de ene 2022 a jul 2023. Construido sobre un esquema estrella con 5 tablas y medidas DAX de ingresos, unidades, participación de mercado y desempeño por marca.

---

## <img src="https://img.icons8.com/?size=40&id=LpCpRq_ztN6C&format=png&color=000000" align="center"/> Dashboard Preview / Vista del Dashboard

### Menú de Navegación
![Menu](screenshots/01_Menú.png)

### Resumen Ejecutivo
![Resumen Ejecutivo](screenshots/02_Resumen_Ejecutivo.png)

### Análisis Regional
![Analisis Regional](screenshots/03_Análisis_Regional.png)

### Segmentos y Marcas
![Segmentos y Marcas](screenshots/04_Segmentos_y_Marcas.png)

### Detalle por Marca (Drill Through)
![Detalle Marca](screenshots/05_Detalle_Marca.png)

### Tabla Completa (Drill Through)
![Tabla Completa](screenshots/06_Tabla_Completa.png)

### Ejemplo de donde usar los dos Drill Throughs
![Ej 2 Drills](screenshots/07_Ejemplo_dos_Drill_Throughs.png)

### Ejemplo visual de Tootltip de Marca
![Ej Tooltip Marca](screenshots/08_Ejemplo_Tootlip_Marca.png)

### Ejemplo visual de Tootltip de Segmento
![Ej Tooltip Seg](screenshots/09_Ejemplo_Tootltip_Segmento.png)

---

## <img src="https://img.icons8.com/?size=40&id=80717&format=png&color=000000" align="center"/> Data Model / Modelo de Datos

---
![Model](screenshots/00_Model.png)
---

| Table / Tabla | Type / Tipo | Description |
|---|---|---|
| `FACT_SALES` | Fact | 122K+ weekly transactions · transacciones semanales |
| `DIM_PRODUCT` | Dimension | Product master · Maestro de productos |
| `DIM_CATEGORY` | Dimension | Category catalog · Catálogo de categorías |
| `DIM_SEGMENT` | Dimension | Segments · Segmentos (Bleach, Powder, Liquid & Gel...) |
| `DIM_CALENDAR` | Dimension | Time dimension · Dimensión de tiempo |

---

## <img src="https://img.icons8.com/?size=40&id=KSDaOFfEpIEF&format=png&color=000000" align="center"/> Report Pages / Páginas del Reporte

| Page / Página | Content / Contenido |
|---|---|
| **Menú** | Navigation hub with buttons · Menú de navegación con botones |
| **Resumen Ejecutivo** | KPIs, total revenue, Growth YoY · KPIs, ingreso total, crecimiento interanual |
| **Análisis Regional** | Sales and trends by region, trends · Ventas y tendencias por región |
| **Segmentos y Marcas** | Market share by segment and brand · Participación por segmento y marca |
| **Detalle Marca** | Drill-down per brand · Detalle por marca con filtros |
| **Tabla Completa** | Full data table with slicers · Tabla completa con segmentadores |

---


## <img src="https://img.icons8.com/?size=40&id=80431&format=png&color=000000" align="center"/> Technical Highlights / Técnicas Utilizadas

<img src="https://img.icons8.com/?size=25&id=V3onoUIHopvo&format=png&color=000000" align="center"/> **Note on YoY Growth Calculation / Nota sobre el cálculo de crecimiento interanual**

EN · Growth YoY calculated using the Common Period (Jan 9 – Jul 17) where both 2022 and 2023 have sales data. After Jul 18, 2023 no records exist, so extending the comparison would not be valid.

ES · El crecimiento YoY se calculó usando el Periodo Común (9 ene – 17 jul) en el que ambos años tienen datos de ventas. A partir del 18 jul 2023 no hay registros, por lo que extender la comparación no sería válido.

<img src="https://img.icons8.com/?size=25&id=V3onoUIHopvo&format=png&color=000000" align="center"/> **DAX Measures / Medidas DAX:**

```dax
% Crecimiento Periodo Comun = 
DIVIDE(
    [Ventas Año Actual Periodo Comun]
        - [Ventas Año Anterior Periodo Comun],
    [Ventas Año Anterior Periodo Comun],
    0
)
```

<img src="https://img.icons8.com/?size=25&id=V3onoUIHopvo&format=png&color=000000" align="center"/> **Features / Funcionalidades:**
- Navigation menu with page buttons · Menú de navegación con botones
- Custom tooltips per brand and segment · Tooltips personalizados por marca y segmento
- Cross-filtering between visuals · Filtrado cruzado entre visualizaciones
- Mobile layout · Vista móvil configurada
- Star schema data model · Modelo de datos en esquema estrella

---

## <img src="https://img.icons8.com/?size=40&id=80351&format=png&color=000000" align="center"/> Key Findings / Hallazgos Clave

- **Bleach/Cloralex** dominates with ~68.7% of total sales
- **Region 2 has the most sales** while Region 3 has the most growth
- **Top 3 segments** (Bleach, Liquid & Gel, Powder) = 91.2% of revenue

---

## <img src="https://img.icons8.com/?size=40&id=VV3ixFIclAcj&format=png&color=000000" align="center"/> Requirements / Requisitos

```
Power BI Desktop (free) — latest version
Download: https://powerbi.microsoft.com/desktop
```

> Open the `.pbix` file directly in Power BI Desktop.
> No additional data sources needed. Data is embedded.
> Abrir el archivo `.pbix` directamente en Power BI Desktop.
> No se requieren fuentes de datos adicionales. Datos embebidos.

---

## <img src="https://img.icons8.com/?size=40&id=PhymLYNNjf3I&format=png&color=000000" align="center"/> Repository Structure / Estructura del Repositorio

```
powerbi-retail-sales-dashboard/
├── screenshots/                                        ← Dashboard previews
├── Power BI Dashboard - Retail Sales Analysis.pbix     ← Power BI file
└── README.md
```

---

*Project developed as part of the Data Scientist Certificate · 
Proyecto desarrollado como parte del certificado Científico de Datos — EBAC (2026)* <img src="https://img.icons8.com/?size=35&id=FgMs84V9yrMV&format=png&color=000000" align="center"/>
