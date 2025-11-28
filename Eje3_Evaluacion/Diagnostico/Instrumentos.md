# Instrumento de Caracterización I - Instituciones Educativas Distritales (IED)

**URL del Formulario:** https://ee-eu.kobotoolbox.org/x/q92nmcWE  
**Formato:** XLSForm (para uso en KoboToolbox, ODK, etc.).  
**Versión:** 23.3.  
**Formulario XlSForm:** por definir.
**Fecha de creación:** 2025.

---

## Objetivo del instrumento
Recopilar información clave sobre las características de los maestros y las IEDs, en los niveles de prejardín, preescolar y transición en las Instituciones Educativas Distritales de Bogotá.

---

## Estructura del formulario

| Grupo | Nombre del grupo | Descripción |
|-------|------------------|-------------|
| 1 | Caracterización I | Datos personales del docente |
| 2 | Caracterización II | Información laboral y de contexto institucional |

---

## Resumen técnico del instrumento

| Elemento | Cantidad |
|----------|----------|
| **Variables totales** | 32 |
| **Preguntas abiertas** | 6 |
| **Preguntas cerradas (select_one)** | 25 |
| **Preguntas múltiples (select_multiple)** | 1 |
| **Preguntas condicionales** | 15 |
| **Grupos de preguntas** | 2 |

---

## Tipos de variables

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

## Condicionales (lógica de relevancia)

- Las **sedes educativas** se filtran según la **institución educativa** seleccionada.
- Las **instituciones educativas** se filtran según la **localidad**.
- Las **preguntas por grado** (prejardín, preescolar, transición) solo aparecen si el docente seleccionó ese grado en `_Actualmente_en_qu_grados_dic`.

---

## Archivos asociados
- `Encuesta de caracterizacion I instituciones Educativas Distritales.xlsx`
  - Hoja: `survey` → estructura del formulario
  - Hoja: `choices` → listas de opciones

---

## Uso técnico
Este instrumento está diseñado para ser implementado en plataformas compatibles con **XLSForm** como:
- KoboToolbox
- ODK Collect
- Enketo

---

## Licencia y tratamiento de datos
El formulario incluye un consentimiento informado que autoriza el tratamiento de datos personales e imagen para fines estadísticos, académicos e institucionales, conforme a la normativa colombiana de protección de datos personales.

---

# Instrumento de Caracterización de los Procesos de Valoración y Seguimiento al Desarrollo Infantil

**URL:** https://ee-eu.kobotoolbox.org/x/LIfIkPIR 
**Formato:** XLSForm (para uso en KoboToolbox, ODK).
**Versión:** 21.0.
**Formulario XlSForm:** por definir.
**Fecha de creación:** 2025.

---

## Objetivo del instrumento
Explorar cómo los maestros de prejardín, jardín y transición en las Instituciones Educativas Distritales (IED) de Bogotá conducen los procesos de valoración y seguimiento al desarrollo infantil, tanto en su planeación pedagógica como en los instrumentos y dinámicas institucionales que utilizan para registrar, interpretar y socializar el desarrollo de niñas y niños.

---

## Estructura del formulario

| Grupo | Nombre del grupo | Descripción |
|-------|------------------|-------------|
| 1 | Política de tratamiento de datos | Consentimiento informado |
| 2 | Primera parte | Datos de ubicación y caracterización del docente |
| 3 | Segunda parte | Procesos de valoración y seguimiento al desarrollo infantil |

---

## Resumen técnico del instrumento

| Elemento | Cantidad |
|----------|----------|
| **Variables totales** | 23 |
| **Preguntas abiertas** | 4 |
| **Preguntas cerradas (select_one)** | 17 |
| **Preguntas múltiples (select_multiple)** | 2 |
| **Preguntas condicionales** | 8 |
| **Grupos de preguntas** | 3 |

---

## Tipos de variables

| Tipo de variable | Nombre de la variable | Tipo de campo | Opciones / Valores | Obligatoria |
|------------------|------------------------|----------------|---------------------|-------------|
| **Consentimiento** | `Autorizo_a_la_Fundac_ar_esta_autorizaci_n` | select_one | Sí, No | ✅ |
| **Ubicación** | `Localidad` | select_one | 1 a 20 (ver tabla abajo) | ✅ |
| **Institución** | `Nombre_de_la_Instituci_n_Educativa1...20` | select_one | Dependiente de localidad | ✅ |
| **Sede** | `Nombre_de_la_sede_Educativa` | select_one | Dependiente de institución | ✅ |
| **Identificación** | `Su_nombre_completo` | texto | - | ✅ |
| **Contacto** | `Su_n_mero_de_contacto` | texto numérico | - | ✅ |
| **Grados** | `Grado_que_tiene_a_cargo` | select_multiple | Prejardín, Jardín, Transición | ✅ |
| **Identificación** | `Denominaci_n_del_grupo_que_tiene_a_cargo` | texto | Ejemplo: Jardín A | ❌ |
| **Registros en planeación** | `En_su_planeaci_n_pedag_gica_` | select_one | Sí, No | ✅ |
| **Estructura de registros** | `Si_su_respuesta_fue_afirmativa` | select_one | Ejes, Hitos, Dimensiones, Relaciones, Otro | ✅ (si aplica) |
| **Otra estructura** | `_Cu_les` | texto | - | ❌ (si aplica) |
| **Enfoque del registro** | `De_igual_manera_us_ni_as_en_particular` | select_one | Individual, Grupal, Ambos | ✅ |
| **Instrumento distinto** | `_2_Cuenta_con_un_instrumento_` | select_one | Sí, No | ✅ |
| **Estructura del instrumento** | `Si_su_respuesta_fue_afirmativa_001` | select_one | Ejes, Hitos, Dimensiones, Relaciones, Otro | ✅ (si aplica) |
| **Otra estructura** | `_Cu_les_001` | texto | - | ❌ (si aplica) |
| **Enfoque del instrumento** | `De_igual_manera_us_ni_as_en_particular_001` | select_one | Individual, Grupal, Ambos | ✅ |
| **Frecuencia** | `_3_Cada_cu_nto_hace_as_ni_as_y_los_ni_os` | select_one | Diariamente, Semanalmente, Cada 2 semanas, Mensual, Bimensual, Trimestral, Semestral | ✅ |
| **Organizadores definidos** | `_4_La_IED_tiene_def_miento_al_desarrollo` | select_one | Sí, No | ✅ |
| **Cómo se incluyen** | `_C_mo_incluye_esos_o_laneaci_n_pedag_gica` | texto | - | ✅ (si aplica) |
| **Socialización con familias** | `_5_En_la_IED_se_entregan_bole` | select_one | Sí, No | ✅ |
| **Frecuencia de socialización** | `Si_su_respuesta_fue_n_espacio_de_di_logo` | select_one | Diariamente, Semanalmente, Cada 2 semanas, Mensual, Bimensual, Trimestral, Semestral | ✅ (si aplica) |
| **Metodología de socialización** | `_Cu_l_es_la_metodolog_a_a_trav` | select_multiple | Taller, Escuela de padres, Encuentros con familias, Encuentros individuales, Otro | ❌ (si aplica) |
| **Otra metodología** | `Otro_cu_l` | texto | - | ❌ (si aplica) |
| **Registro en SIEE** | `_6_En_la_IED_carga_de_Estudiantes_SIEE` | select_one | Sí, No | ✅ |

---

## Condicionales (lógica de relevancia)

- Las **sedes** se filtran según la **institución** seleccionada.
- Las **instituciones** se filtran según la **localidad**.
- Las **estructuras de registro** (planeación o instrumento) solo aparecen si el docente respondió *Sí*.
- Las **opciones de “Otro”** solo aparecen si se selecciona esa opción.
- Las **preguntas sobre socialización** solo aparecen si el docente indica que sí se hace.
- La **metodología de socialización** es opcional y aparece solo si aplica.

---

## Archivos asociados
- `INSTRUMENTO DE CARACTERIZACIÓN DE LOS PROCESOS DE VALORACIÓN Y SEGUIMIENTO AL DESARROLLO INFANTIL.xlsx`
  - Hoja: `survey` → estructura del formulario
  - Hoja: `choices` → listas de opciones

---

## Uso técnico
Este instrumento está diseñado para ser implementado en plataformas compatibles con **XLSForm** como:
- KoboToolbox
- ODK Collect
- Enketo

---

## Licencia y tratamiento de datos
El formulario incluye un consentimiento informado que autoriza el tratamiento de datos personales e imagen para fines estadísticos, académicos e institucionales, conforme a la normativa colombiana de protección de datos personales.

---

# Instrumento de Observación a la Calidad Pedagógica en Escenarios de Educación Inicial

**URL:** https://ee-eu.kobotoolbox.org/x/2W2M6BqR  
**Formato:** XLSForm (KoboToolbox / ODK / Enketo)  
**Versión:** 15.1 (actualización de sedes y códigos de institución)  
**Fecha de creación:** 2025

---

## Objetivo
Unificar y evaluar los criterios mínimos de calidad pedagógica en prejardín, jardín y transición mediante observación estructurada de:
- Planeación y estrategias pedagógicas (5 criterios)
- Ambientes de aprendizaje (5 criterios)
- Desarrollo del lenguaje y experiencias comunicativas – EOLE (8 criterios)

---

## Estructura del formulario

| Grupo | Nombre del grupo | Descripción |
|-------|------------------|-------------|
| 1 | Aviso Importante | Uso exclusivo acompañantes UWC |
| 2 | Descripción | Objetivo y alcance |
| 3 | Información general de la observación | Localidad, IED, sede, fecha, docente, observador |
| 4 | Componente 1 – Planeación y estrategias pedagógicas | 5 criterios (1.1 – 1.5) |
| 5 | Componente 2 – Ambientes | 5 criterios (2.1 – 2.5) |
| 6 | Componente 3 – EOLE | 8 criterios (3.1 – 3.8) |
| 7 | Comentarios/Observaciones adicionales | Campo abierto |

---

## Resumen técnico

| Elemento | Cantidad |
|----------|----------|
| **Variables totales** | 58 |
| **Preguntas abiertas** | 19 (descripciones + comentarios) |
| **select_one** | 39 |
| **select_multiple** | 0 |
| **Grupos lógicos** | 7 |
| **Criterios evaluativos** | 18 |
| **Condicionales** | ~25 (sedes según institución; algunas sedes nuevas con relevancia condicional) |

---

## Principales bloques de variables

### Información general
| Variable | Tipo | Obligatoria | Notas |
|----------|------|-------------|-------|
| Localidad | select_one | ✅ | 20 opciones |
| Institución Educativa | select_one | ✅ | Filtrada por localidad |
| Sede Educativa | select_one | ✅ | Filtrada por institución; **nuevos códigos y sedes** en esta versión |
| Fecha | date | ❌ | |
| Número de visita | integer | ❌ | |
| Aula observada | texto | ❌ | |
| Nombre docente | texto | ✅ | |
| Tipo y número de documento del docente | texto + select_one | ✅ | |
| Contacto docente | texto (númerico) | ✅ | |
| Nombre y documento del observador | texto + numérico | ✅ | |

### Criterios evaluativos (18)
Cada criterio incluye:
- `Descripci_n_situaci_l_frente_al_criterio_XXX` → **texto abierto**
- `Resultado_XXX` → **select_one**: “Se evidencia” / “No se evidencia”

**Componentes:**
1. **Planeación y estrategias pedagógicas** (5 criterios)
2. **Ambientes** (5 criterios)
3. **EOLE** (8 criterios)

---

## Cambios respecto a Versión 1
- **Nuevas sedes** agregadas con códigos únicos (ej. `pl0sy93`, `ry4ra66`, `lj1op20`, etc.)
- **Relaciones condicionales** actualizadas para estas sedes:
  - `Nombre_de_la_sede_Educativa_098` → solo si `${Nombre_de_la_Instituci_n_Educativa4} = '111001024686'`
  - `099` → `111001014451`
  - `100` → `111001014176`
  - `101` → `111001024643`
  - `102` → `111001011975`
  - `103` → `111001009831`
- **Opciones de sede “maria” y “luz”** se mantienen para `tv72t8`
- **Listas de opciones** (`choices`) actualizadas con etiquetas descriptivas y códigos DANE/IED

---

## Uso técnico
- Compatible con **KoboToolbox**, **ODK Collect**, **Enketo**
- **Acceso restringido**: solo acompañantes pedagógicos o artistas de **UWC**
- No incluye consentimiento dentro del formulario (se asume previo institucional)

---

## Archivos asociados
`Versión 2 Instrumento de Observación a la Calidad Pedagógica en escenarios de educación inicial.xlsx`
- Hoja `survey` → estructura completa
- Hoja `choices` → listas localidad, instituciones, sedes, resultados

---

# Instrumento de Fotografía de Ambientes de Aprendizaje

**URL:** https://ee-eu.kobotoolbox.org/x/AepjN70u  
**Formato:** XLSForm (KoboToolbox / ODK / Enketo)  
**Versión:** 22.0  
**Fecha de creación:** 2025  

---

## Objetivo
Capturar evidencias fotográficas de los ambientes de aprendizaje de prejardín, jardín y transición que permitan analizar:  
- Organización y funcionalidad del espacio  
- Disponibilidad y estado de materiales  
- Presencia de elementos culturales, lúdicos y de literacidad 
---

## Estructura del formulario

| Grupo | Nombre del grupo | Descripción breve |
|-------|------------------|-------------------|
| 1 | Aviso Importante | Uso exclusivo acompañantes UWC |
| 2 | Descripción | Objetivo y alcance |
| 3 | Información general | Localidad → IED → sede → fecha → grado → docente |
| 4 | Fotografías | 8 tomas estándar + 2 opcionales |
| 5 | Comentarios | Espacio abierto |

---

## Resumen técnico

| Elemento | Cantidad |
|----------|----------|
| **Variables totales** | 25 |
| **Fotos obligatorias** | 8 |
| **Fotos opcionales** | 2 |
| **select_one** | 5 |
| **date** | 1 |
| **text** (abierto) | 5 |
| **image** | 10 |
| **Grupos lógicos** | 5 |
| **Condicionales** | ~20 (sedes según institución) |

---

## Variables principales

| Variable | Tipo | Obligatoria | Hint / Uso |
|----------|------|-------------|------------|
| Localidad | select_one | ✅ | 20 localidades |
| Institución | select_one | ✅ | Filtrada por localidad |
| Sede | select_one | ✅ | Filtrada por institución |
| Fecha | date | ✅ | Día de la visita |
| Grado observado | select_one | ✅ | prejardín / jardín / transición |
| Nombre docente | text | ✅ | |
| Aula / espacio | text | ❌ | Referencia espacial |
| **Foto 1** | image | ✅ | Panorámica general del aula |
| **Foto 2** | image | ✅ | Rincón de literatura o lectura |
| **Foto 3** | image | ✅ | Rincón de juego / manipulativos |
| **Foto 4** | image | ✅ | Rincón de expresión artística |
| **Foto 5** | image | ✅ | Rincón de exploración / ciencia |
| **Foto 6** | image | ✅ | Panel / mural de familia o identidad |
| **Foto 7** | image | ✅ | Estantería o zona de autónomo acceso |
| **Foto 8** | image | ✅ | Suelo, ventanas, iluminación y seguridad |
| Foto 9 (opcional) | image | ❌ | Detalle innovador o buena práctica |
| Foto 10 (opcional) | image | ❌ | Aspecto a mejorar |
| Comentarios | text | ❌ | Espacio abierto |

---

## Criterios de calidad de la foto (recomendados)

- **Resolución mínima:** 1280 × 720 px  
- **Iluminación:** evitar contraluces o sombras densas  
- **Enfoque:** elementos clave nítidos  
- **Privacidad:** no mostrar rostros de niñas o niños; enfocar espacios y materiales  

---

## Lógica condicional

- **Sedes** filtradas por **institución** → **localidad**  
- **Grado** y **fecha** determinan carpeta de almacenamiento en repositorio  
- **Fotos opcionales** solo se activan si el observador marca *“Sí”* a *“¿Desea agregar fotos adicionales?”* (campo no incluido en versión actual; puede agregarse si se requiere)

---

## Uso técnico

- Compatible con **KoboCollect**, **ODK**, **Enketo**  
- Tamaño máximo por imagen: configurable (recomendado 2 MB)  
- **Acceso restringido**: solo personal UWC (enlace interno, no público)  

---

## Archivos asociados

`Fotografía Ambientes de aprendizaje.xlsx`  
- Hoja `survey` → estructura  
- Hoja `choices` → listas localidad, instituciones, sedes, grados  

---

