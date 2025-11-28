# 📋 Instrumento de Caracterización I - Instituciones Educativas Distritales (IED)

**Proyecto:** Fortalecimiento a docentes de educación inicial en colegios distritales de Bogotá  
**Formato:** XLSForm (para uso en KoboToolbox, ODK, etc.)  
**Versión:** 1.0  
**Fecha de creación:** 2025

---

## 🎯 Objetivo del instrumento
Recopilar información clave sobre las **características de los docentes**, **la infraestructura educativa**, y **la cantidad de estudiantes** en los niveles de **prejardín, preescolar y transición** en las Instituciones Educativas Distritales de Bogotá.

---

## 🧩 Estructura del formulario

| Grupo | Nombre del grupo | Descripción |
|-------|------------------|-------------|
| 1 | Caracterización I | Datos personales del docente |
| 2 | Caracterización II | Información laboral y de contexto institucional |

---

## 🧾 Resumen técnico del instrumento

| Elemento | Cantidad |
|----------|----------|
| **Variables totales** | 32 |
| **Preguntas abiertas** | 6 |
| **Preguntas cerradas (select_one)** | 25 |
| **Preguntas múltiples (select_multiple)** | 1 |
| **Preguntas condicionales** | 15 |
| **Grupos de preguntas** | 2 |

---

## 🧮 Tipos de variables

| Tipo de variable | Nombre de la variable | Tipo de campo | Opciones / Valores | Obligatoria |
|------------------|------------------------|----------------|---------------------|-------------|
| **Identificación** | `N_mero_de_documento_de_identidad` | texto | - | ✅ |
| **Identificación** | `Tipo_de_documento` | select_one | CC, CE, PAS, PEP, Otro | ✅ |
| **Identificación** | `Nombres` | texto | - | ✅ |
| **Identificación** | `Apellidos` | texto | - | ✅ |
| **Contacto** | `Correo_de_contacto` | texto | - | ✅ |
| **Contacto** | `N_mero_de_tel_fono_de_contacto` | texto | - | ✅ |
| **Ubicación** | `Zona_en_la_que_est_ubicada_la_IED` | select_one | Urbana, Rural | ✅ |
| **Formación** | `Id_del_nivel_de_formaci_n` | select_one | Normalista, Profesional, Especialización, Maestría, Doctorado, Postdoctorado | ❌ |
| **Edad** | `Id_del_rango_de_edad` | select_one | 18-25, 26-35, 36-45, 46-55, &gt;55 | ❌ |
| **Género** | `Sexo` | select_one | Hombre, Mujer, Otro | ✅ |
| **Ubicación** | `Localidad` | select_one | 1 a 20 (ver tabla abajo) | ✅ |
| **Institución** | `Nombre_de_la_Instituci_n_Educativa1...20` | select_one | Dependiente de localidad | ✅ |
| **Sede** | `Nombre_de_la_sede_Educativa` | select_one | Dependiente de institución | ✅ |
| **Jornada** | `_Cu_l_es_la_jornada_en_la_que_trabaja` | select_one | Única, Mañana, Tarde | ✅ |
| **Vinculación** | `Tipo_de_vinculaci_n` | select_one | De planta, Provisional | ✅ |
| **Experiencia** | `_Cu_ntos_a_os_de_exp_en_educaci_n_inicial` | select_one | &lt;1, 1-5, 6-10, 11-20, &gt;20 | ✅ |
| **Grados** | `_Actualmente_en_qu_grados_dic` | select_multiple | Prejardín, Preescolar, Transición | ✅ |
| **Estudiantes** | `_Cu_ntos_estudiantes_e_el_grado_Prejard_n` | entero | - | ✅ (si aplica) |
| **Estudiantes** | `_Cu_ntos_estudiantes_el_grado_Preescolar` | entero | - | ✅ (si aplica) |
| **Estudiantes** | `_Cu_ntos_estudiantes_el_grado_Transici_n` | entero | - | ✅ (si aplica) |
| **Observaciones** | `coloque_aqui_cualqui_n_en_alguna_pregunta` | texto | - | ❌ |

---

## 🔍 Condicionales (lógica de relevancia)

- Las **sedes educativas** se filtran según la **institución educativa** seleccionada.
- Las **instituciones educativas** se filtran según la **localidad**.
- Las **preguntas por grado** (prejardín, preescolar, transición) solo aparecen si el docente seleccionó ese grado en `_Actualmente_en_qu_grados_dic`.

---

## 📂 Archivos asociados
- `Encuesta de caracterizacion I instituciones Educativas Distritales.xlsx`
  - Hoja: `survey` → estructura del formulario
  - Hoja: `choices` → listas de opciones

---

## 🧑‍💻 Uso técnico
Este instrumento está diseñado para ser implementado en plataformas compatibles con **XLSForm** como:
- KoboToolbox
- ODK Collect
- Enketo

---

## 🧾 Licencia y tratamiento de datos
El formulario incluye un **consentimiento informado** que autoriza el tratamiento de datos personales e imagen para fines estadísticos, académicos e institucionales, conforme a la normativa colombiana de protección de datos personales.

---

## 📬 Contacto
Para dudas técnicas o metodológicas sobre el instrumento:  
📧 [comunicaciones@uwcolombia.org](mailto:comunicaciones@uwcolombia.org)

