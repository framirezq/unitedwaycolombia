# Tablero de Gestión – Acompañamiento Situado

**Plataforma:** Power BI  
**Frecuencia de actualización:** diaria (API Kobo → Power BI)  
**Última actualización:** 27/11/2025  
**URL:** https://app.powerbi.com/view?r=eyJrIjoiYTEzZjY1ZDgtZTQ5My00NTI1LWI4YTAtMmIyZTk4YjhlYWVkIiwidCI6Ijk4YzUyOTJjLTZmODUtNDU2NS04YWNlLTk2OWRhZGE3ODgwOCIsImMiOjR9

<img width="776" height="440" alt="image" src="https://github.com/user-attachments/assets/9ce4b068-689c-44ef-b578-c3c68cc6ceca" />


Este tablero monitorear en tiempo real la ejecución física del acompañamiento situado que pedagógos y artistas de United Way realizan con los maestros de prejardín, jardín y transición de las IED del convenio, detectando desviaciones, oportunidades de intervención y necesidades de apoyo.


| Origen | Dataset en Power BI | Llave principal | Frecuencia |
|--------|---------------------|-----------------|------------|
| **Formulario “Reporte de acompañamiento”** (XLSForm – Kobo) | `factAcompanamiento` | `id_reporte` (uuid) | Diaria 06:00 a.m. |
| **Catálogo de IED y nodos** (SharePoint) | `dimIED` | `cod_dane_ied` | Semanal |
| **Catálogo de profesionales UWC** (SharePoint) | `dimProfesional` | `email_profesional` | Semanal |

## Definiciones operativas

| Concepto | Cálculo | Descripción |
|----------|---------|-------------|
| **Acompañamientos planeados** | `SUM(planificado_anual)` | Meta anual pactada por nodo (pre-jardín + jardín + transición) |
| **Acompañamientos reportados** | `COUNTROWS(factAcompanamiento)` | Formularios enviados y aprobados en Kobo |
| **% Avance** | `reportados / planeados` | Indicador de ejecución física |
| **Diferencia** | `planeados - reportados` | Número de aulas pendientes por visitar |
| **Estado IED** | Regla segmentada (ver punto 6) | Clasificación visual: crítico, alerta, desarrollo, completo |

## KPIs principales (página resumen)

| KPI | Valor actual (27/11/2025) | Fórmula DAX |
|-----|---------------------------|-------------|
| Total acompañamientos reportados | 2,397 | `COUNTROWS(factAcompanamiento)` |
| Total planeados a la fecha | 2,397 | `SUM(planificado_hasta_hoy)` |
| Avance global | 100 % | `DIVIDE(reportados, planeados)` |
| Promedio de % por profesional | 72 % | `AVERAGEX(dimProfesional, [% individual])` |
| IEDs en estado “completo” | 27 | `COUNTROWS(FILTER(dimIED, estado = "completo"))` |
| IEDs en estado “crítico” | 6 | `COUNTROWS(FILTER(dimIED, estado = "crítico"))` |

## Vistas y gráficos

| Vista | Gráfico / tabla | Uso |
|-------|-----------------|-----|
| **Panel Ejecutivo** | Tarjetas de KPI y gauge de avance global | Seguimiento rápido a la meta |
| **Desempeño por Profesional** | Tabla con % avance, diferencia y última fecha de reporte | Identificar profesionales que requieran apoyo |
| **Mapa de calor por IED** | Scatter % realizado vs. % faltante, coloreado por estado | Detectar IEDs rezagadas |
| **Evolución mensual** | Líneas de reportados vs. planeados acumulados | Ver tendencia y proyección de cierre |
| **Análisis por Nodo** | Barras apiladas de realizado/faltante por nodo | Distribución geográfica del esfuerzo |
| **Detalle de maestro** | Tabla filtrable: IED, sede, grado, fecha, componente, línea, momento | Auditoría y seguimiento de calidad |

## Reglas de estado de IED (medida calculada)

```dax
estado IED =
SWITCH(
    TRUE(),
    [% realizado] >= 95, "completo",
    [% realizado] >= 70, "desarrollo",
    [% realizado] >= 50, "alerta",
    "crítico"
)
```

> El umbral se puede ajustar desde el panel de configuración sin tocar el modelo.

---

## Segmentadores globales

- Localidad  
- Nodo  
- Profesional (email)  
- Rango de fechas  
- Grado (prejardín / jardín / transición)  
- Estado IED  

Acceso y soporte

| Recurso | URL / contacto |
|---------|----------------|
| Tablero de Gestión (lectura) | [https://app.powerbi.com/groups/xxxxx/reports/aaaaa](https://app.powerbi.com/groups/xxxxx/reports/aaaaa) |
| Dataset (editores) | [https://app.powerbi.com/groups/xxxxx/datasets/bbbbb](https://app.powerbi.com/groups/xxxxx/datasets/bbbbb) |
| Formulario origen (Kobo) | [https://kobo.unitedwaycolombia.org/acompanamiento](https://kobo.unitedwaycolombia.org/acompanamiento) |
| Soporte técnico | [comunicaciones@uwcolombia.org](mailto:comunicaciones@uwcolombia.org) |

---

## 10. Próximos pasos

1. Automatizar alertas por correo cuando una IED pase a estado “crítico” ≥ 3 días  
2. Incorporar **meta semanal** dinámica (pro-rrateo de la anual) para visualizar desviación en tiempo real  
3. Publicar versión pública (sin RLS) con agregados por localidad para la SED  

---

> **Nota:** esta documentación se mantiene en `/docs/tablero-gestion-acompanamiento.md` del repositorio oficial y se versiona con cada cambio significativo del modelo.
```
