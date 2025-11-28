# Tablero Multimedia – Acompañamiento Situado en Línea de Tiempo

**Plataforma:** Power BI  
**Frecuencia de actualización:** diaria (API Kobo → SharePoint → Power BI)  
**Última actualización:** 27/11/2025  
**URL:** https://app.powerbi.com/view?r=eyJrIjoiNzY2MDYyNzgtODYwNi00YjI4LTlkYTAtNmRjNjM4ODdiYTdmIiwidCI6Ijk4YzUyOTJjLTZmODUtNDU2NS04YWNlLTk2OWRhZGE3ODgwOCIsImMiOjR9

<img width="865" height="486" alt="image" src="https://github.com/user-attachments/assets/0a9ec5b8-1a24-44aa-914b-2d6b83e6b5cb" />

En este tablero se visualiza cada sesión de acompañamiento situado en una línea de tiempo interactiva que permite:

- Reproducir audios sobre lo acontecido  
- Ver imágenes, materiales y momentos pedagógicos  
- Abrir las actas / PDFs firmadas o reportes impresos  
- Filtrar por fecha, profesional, IED, grado, tipo de archivo y Nodo  
- Analizar evolución cualitativa del aula a lo largo del año  

&gt; El tablero convierte el “formulario con archivos adjuntos” en una **cronoteca pedagógica** navegable.

---

## Fuentes y arquitectura

| Capa | Origen | Llave | Detalle |
|------|--------|-------|---------|
| **Metadatos** | Kobo (formulario “Reporte de acompañamiento”) | `id_reporte` | fecha, profesional, IED, sede, grado, componente, línea, momento |
| **Archivos** | SharePoint Online (carpeta `/multimedia/`) | `id_reporte` + extensión | rutas firmes: `https://uwc.sharepoint.com/sites/edinicial/multimedia/{id_reporte}_audio.mp3` |
| **Modelo Power BI** | Power Query | `id_reporte` | tabla `factMultimedia` con columnas: &lt;br&gt;`url_audio`, `url_imagen`, `url_acta`, `url_pdf`, `fecha_local`, `orden_timeline` |

---

## Tipos de archivo soportados

| Tipo | Extensiones | Visualización nativa Power BI | Almacenamiento |
|------|-------------|-------------------------------|----------------|
| **Audio** | `.mp3`, `.m4a` | ✅ Reproductor incrustado | SharePoint (stream embed) |
| **Imagen** | `.jpg`, `.png` | ✅ Image URL | SharePoint (rendición público) |
| **PDF / Acta** | `.pdf` | 🔗 Abrir en nueva pestaña (Web URL) | SharePoint (direct link) |
| **Video corto** | `.mp4` ≤ 50 MB | ✅ Stream (opcional) | SharePoint / OneDrive |

&gt; Todos los archivos se **renombran automáticamente** al llegar a SharePoint con el patrón:  
&gt; `{id_reporte}_{tipo}.{ext}` → facilita la generación dinámica de URLs.

---

## Modelo de datos (resumido)

```mermaid
erDiagram
    factAcompanamiento {
        string id_reporte PK
        date fecha
        string profesional
        string cod_dane_ied
        string grado
        string componente
        string linea
        string momento
    }
    factMultimedia {
        string id_reporte PK/FK
        string url_audio
        string url_imagen
        string url_acta
        string url_pdf
        int orden_timeline
    }
    dimIED {
        string cod_dane_ied PK
        string nombre_ied
        string nodo
        string localidad
    }
    factAcompanamiento ||--o{ factMultimedia : "1 a 1"
    factAcompanamiento }o--|| dimIED : "pertenece"
