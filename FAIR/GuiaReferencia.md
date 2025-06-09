# FAIR: Guía de Referencia General

## Índice

1. [Introducción](#1-introduccion)  
2. [Principios FAIR](#2-principios-fair)  
   2.1 [Findable (Encontrable)](#21-findable-encontrable)  
   2.2 [Accessible (Accesible)](#22-accessible-accesible)  
   2.3 [Interoperable](#23-interoperable)  
   2.4 [Reusable (Reutilizable)](#24-reusable-reutilizable)  
3. [Consideraciones éticas, lingüísticas y culturales](#3-consideraciones-eticas-linguisticas-y-culturales)  
4. [Metadatos y Estándares](#4-metadatos-y-estandares)  
5. [Formatos de Datos y Recomendaciones](#5-formatos-de-datos-y-recomendaciones)  
6. [Licencias y Derechos de Uso](#6-licencias-y-derechos-de-uso)  
7. [Evaluación FAIR y Herramientas](#7-evaluacion-fair-y-herramientas)  
8. [Tipos de Investigación y Requisitos FAIR](#8-tipos-de-investigacion-y-requisitos-fair)  
   8.1 [Investigación Observacional](#81-investigacion-observacional)  
   8.2 [Investigación Experimental](#82-investigacion-experimental)  
   8.3 [Investigación Computacional](#83-investigacion-computacional)  
   8.4 [Investigación Clínica y Social](#84-investigacion-clinica-y-social)  
9. [Planificación estructurada de productos de investigación](#9-planificacion-estructurada-de-productos-de-investigacion)  
   9.1 [Planes de Gestión de Datos (DMP)](#91-planes-de-gestion-de-datos)  
   9.2 [Planes de Gestión de Software (SMP)](#92-planes-de-gestion-de-software)  
   9.3 [Planes Accionables por Máquina (maDMPs y maSMPs)](#93-planes-maquina)  
10. [Extensiones para la trazabilidad e interoperabilidad FAIR](#10-extensiones-trazabilidad-interoperabilidad-fair)  
   10.1 [Trazabilidad, versionado y mantenimiento](#101-trazabilidad-versionado-mantenimiento)  
   10.2 [Gestión de flujos de trabajo y modelos computacionales](#102-gestion-flujos-modelos)  
   10.3 [Requisitos técnicos para la interoperabilidad FAIR](#103-requisitos-tecnicos-interoperabilidad)  
   10.4 [Citación y métricas de uso de productos FAIR](#104-citacion-metricas-fair)
   10.5 [Estructura de metadatos procesables por máquinas](#105-estructura-metadatos-procesables-maquinas)  
11. [Anexos](#11-anexos)  
   11.1 [Anexo A: Checklist de Evaluación FAIR](#111-anexo-a-checklist-de-evaluacion-fair)  
   11.2 [Anexo B: Ejemplo de Metadatos Estructurados](#112-anexo-b-ejemplo-de-metadatos-estructurados)  
   11.3 [Anexo C: Datos mínimos para un Plan de Gestión de Datos (DMP)](#113-anexo-c-datos-minimos-para-un-plan-de-gestion-de-datos-dmp)  
   11.4 [Anexo D: Datos mínimos para un Plan de Gestión de Software (SMP)](#114-anexo-d-datos-minimos-para-un-plan-de-gestion-de-software-smp)  


**Este documento está disponible bajo la licencia CC BY 4.0** y puede ser actualizado con nuevas colaboraciones.

## Colaboradores

Esta guía ha sido elaborada en colaboración diversas personas comprometidas con la promoción de los principios FAIR. Se invita a otr@s colaborador@s a contribuir con mejoras, actualizaciones y ejemplos adicionales.

- Ricardo Hartley Belmar @ricnadamas [ORCID:0000-0001-5058-9309](https://orcid.org/my-orcid?orcid=0000-0001-5058-9309)
- Isabel Abedrapo @yolaisa [ORCID:0000-0001-9990-0436](https://orcid.org/0000-0001-9990-0436)
- Priyanka Ojha @priya-gitTest [ORCID:0000-0002-6844-6493](https://orcid.org/0000-0002-6844-6493)
- Carlos Martinez-Ortiz @c-martinez [ORCID:0000-0001-5565-7577](https://orcid.org/0000-0001-5565-7577)
- ...

---

## 1. Introducción <a name="1-introduccion"></a>

# 1. Introducción

Esta guía fue concebida como una herramienta práctica para facilitar la adopción de los principios **FAIR** en la gestión de datos y otros productos digitales vinculados a la investigación. Está pensada no solo para investigadores, sino también para profesionales que desempeñan roles clave en la gestión de información científica: bibliotecarios, desarrolladores de infraestructura, gestores de datos y responsables de políticas públicas.

Los principios FAIR —**Encontrables, Accesibles, Interoperables y Reutilizables**— promueven la organización y publicación de datos de manera que otras personas (y sistemas informáticos) puedan encontrarlos, acceder a ellos, integrarlos y reutilizarlos con facilidad. Lejos de ser una lista rígida, representan una aspiración hacia un ecosistema de conocimiento más abierto y eficiente.

Aunque originalmente diseñados para datos, estos principios también han sido adaptados al software de investigación, dando origen a la iniciativa FAIR4RS. En este contexto, el término "software" abarca desde líneas de código simples hasta sistemas complejos desarrollados en colaboración.

A lo largo de esta guía se abordan también temas prácticos y estratégicos: recomendaciones sobre **estándares de metadatos**, **formatos abiertos**, **licencias de uso**, **evaluación del cumplimiento FAIR**, así como ejemplos aplicables a distintos tipos de proyectos y disciplinas. Se incluyen listas de verificación y recursos para facilitar su implementación en entornos reales.

---

# 2. Principios FAIR

Los principios FAIR aseguran que los datos sean **Encontrables (Findable)**, **Accesibles (Accessible)**, **Interoperables (Interoperable)** y **Reutilizables (Reusable)**. Estos principios facilitan el acceso a los datos científicos, promoviendo su reutilización y fomentando el intercambio de conocimientos en diversos contextos.

Aquí se detallan los principios clave de FAIR:

## 2.1 Findable (Encontrable)

**Objetivo:** Hacer que los datos y sus metadatos sean fácilmente descubribles por las personas y los sistemas.

**Requisitos clave:**
- Los datos deben tener un **identificador único**, como un DOI, que permita encontrarlos fácilmente.
- Los metadatos deben incluir estos identificadores persistentes, lo que facilita su localización automática.
- Los metadatos deben ser detallados y estar en formatos comprensibles tanto para personas como para máquinas.
- Los datos deben ser indexados en **repositorios certificados**, como Zenodo, DataCite o aquellos registrados en CoreTrustSeal.

## 2.2 Accessible (Accesible)

**Objetivo:** Garantizar que los datos y metadatos estén accesibles de forma abierta y transparente.

**Requisitos clave:**
- Los datos deben estar disponibles a través de **enlaces seguros y abiertos**, como HTTPS o APIs RESTful.
- Si se requiere control de acceso, deben implementarse sistemas de **autenticación y autorización** bien definidos.
- Los **metadatos** deben ser accesibles independientemente del acceso a los datos subyacentes, especialmente si existen restricciones de acceso.

## 2.3 Interoperable

**Objetivo:** Facilitar la integración de los datos con otros sistemas y su reutilización en diversos contextos.

**Requisitos clave:**
- Los datos deben estar en **formatos abiertos** y estandarizados, como JSON, XML o RDF, que sean fáciles de procesar y convertir a otros formatos.
- Se deben utilizar **vocabularios controlados** y **ontologías** reconocidas, como Schema.org o DCMI Terms, para asegurar la compatibilidad semántica.
- Los metadatos deben incluir relaciones claras entre los datos, como enlaces a recursos relacionados que aporten contexto o información adicional.

## 2.4 Reusable (Reutilizable)

**Objetivo:** Asegurar que los datos puedan ser utilizados de nuevo en otros contextos científicos, por otros investigadores y en diferentes momentos.

**Requisitos clave:**
- Los datos deben tener **licencias claras y abiertas**, como CC BY o CC0, que permitan su reutilización sin restricciones.
- La **documentación** debe ser completa, explicando cómo se generaron, transformaron, validaron y versionaron los datos.
- Es fundamental mantener un **registro de versiones** para asegurar que los datos se puedan actualizar de forma coherente, señalando las fechas y responsables de las modificaciones.
- Los datos deben seguir **estándares y buenas prácticas** dentro de la comunidad científica, como diccionarios de datos o glosarios, y ser proporcionados en formatos reutilizables como notebooks reproducibles.

📌 **Más información:**
- [Principios FAIR (material para taller). Autores: Meyers, N., Escapil-Inchauspé, P., Egaña Aranguren, M., & Hartley Belmar, R.](https://doi.org/10.6075/J0TM7BG5)  
  Recurso didáctico adaptado para talleres sobre principios FAIR y su aplicación práctica.
- [Traducción del documento guía para el Plan de Gestión de Datos FAIR en Organizaciones e Instituciones. Autores: Kirkpatrick, C. R., Cragin, M. H., & Meyers, N. (2024) (Traductores: Hartley Belmar, R.; Meyers, N.)](https://doi.org/10.6075/J0ZC836W)  
  Traducción comentada de la guía FAIR de DMPs institucionales, contextualizada para públicos hispanohablantes.
- [Ten Simple Rules for FAIR Data](https://doi.org/10.1371/journal.pcbi.1007854)  
  Artículo que sintetiza recomendaciones clave para implementar datos FAIR.


---

## 3. Consideraciones éticas, lingüísticas y culturales

Los principios **FAIR** no consideran explícitamente los derechos de las comunidades, por lo que es necesario complementarlos con los principios **CARE** (Colectivo, Autoridad, Responsabilidad, Ética), desarrollados por la **Global Indigenous Data Alliance (GIDA)**. Estos principios guían el uso justo y respetuoso de los datos sobre pueblos indígenas, garantizando la soberanía digital y el respeto hacia los derechos colectivos.

📌 **Más información:**
- [Más información sobre CARE](https://www.gida-global.org/care)  
  Declaración de principios para la gobernanza ética de datos sobre pueblos indígenas, centrada en valores de colectividad, autoridad, responsabilidad y ética.

### Accesibilidad lingüística

- La mayoría de las herramientas, guías y vocabularios relacionados con la ciencia abierta están disponibles principalmente en inglés, lo que limita su acceso global.
- Promover traducciones, crear glosarios en español y ofrecer capacitación multilingüe son pasos esenciales para avanzar hacia una verdadera **equidad en ciencia abierta**.
- Ejemplos de recursos adaptados al español incluyen materiales de OpenAIRE, el Grupo de Trabajo de RDA en español, y la traducción de guías FAIR institucionales.

### Contextos locales y epistemologías diversas

- La definición de metadatos, estándares y licencias debe considerar normas culturales, marcos legales nacionales y derechos colectivos, respetando la diversidad epistémica.
- El principio de **reutilización responsable** no solo aborda lo técnico, sino también lo ético y contextual. Los datos deben ser gestionados con responsabilidad y en consonancia con los derechos de las comunidades.
- En contextos con pueblos originarios, es esencial tener en cuenta instrumentos como el **Convenio 169 de la OIT** sobre derechos de los pueblos indígenas y tribales, así como las leyes locales que protegen el patrimonio cultural y los datos sensibles.

> ⚠️ Se recomienda evitar aplicar los principios FAIR de manera rígida y exclusivamente técnica. Es fundamental incorporar principios de **justicia epistémica**, accesibilidad cultural y pluralismo de saberes.

📌 **Más información:**
- [Ethical Data Initiative](https://ethicaldatainitiative.org)  
  Iniciativa que promueve la justicia de datos, la soberanía digital y los derechos de comunidades en entornos digitales.

---

## 4. Formatos de Datos y Recomendaciones <a name="4-formatos-de-datos-y-recomendaciones"></a>

| **Tipo de Datos**       | **Formato Recomendado** | **Observaciones** |
|-------------------------|-------------------------|--------------------|
| **Datos tabulares**     | CSV, TSV (UTF-8)        | Separados por comas o tabulaciones, con codificación **UTF-8** y encabezados claros. |
| **Datos jerárquicos**   | JSON, XML               | Uso de esquemas estandarizados para facilitar la validación e interoperabilidad. |
| **Datos geoespaciales** | GeoJSON, GML            | Incluir metadatos sobre sistemas de referencia y proyecciones. |
| **Datos biológicos**    | FASTA, NetCDF           | Seguir las especificaciones de la comunidad científica correspondiente. |
| **Imágenes científicas**| TIFF, DICOM             | Preservar metadatos embebidos; considerar directrices de interoperabilidad. |
| **Otros formatos específicos** | FITS, NetCDF     | Usar conforme a estándares de dominio y versiones documentadas. |

### Consideraciones

#### Formatos abiertos vs. formatos propietarios
- Favorecer **formatos abiertos, legibles por máquinas y con documentación pública**.
- Evitar formatos propietarios que limiten el acceso, conservación o reutilización.

#### Codificación y preservación
- Emplear codificación **UTF-8** de forma consistente.
- Documentar explícitamente cualquier transformación aplicada y la estructura interna de los archivos.

#### Compresión y verificación de integridad
- Describir los algoritmos de compresión y su configuración (ej. `.zip`, `.tar.gz`).
- Incluir **sumas de verificación** (ej. `SHA-256`, `MD5`) para validar la integridad del archivo descargado.

#### Interoperabilidad semántica
- Cuando corresponda, utilizar formatos que integren estructuras semánticas (ej. **RDF**, **JSON-LD**) para habilitar el enlace e interpretación automática.

📌 **Más información:**
- [Formatos preferidos para la preservación y publicación en repositorios (Zenodo)](https://doi.org/10.5281/zenodo.8432009)  
  Recomendaciones de Zenodo para formatos sostenibles a largo plazo.

- [DANS - Recomendaciones de formatos de archivo](https://dans.knaw.nl/en/file-formats/)  
  Directrices del Instituto Holandés DANS para asegurar el archivo digital confiable.

- [UK Data Service - Formatos recomendados](https://ukdataservice.ac.uk/learning-hub/research-data-management/format-your-data/recommended-formats/)  
  Tabla de formatos compatibles con buenas prácticas de gestión, preservación y difusión.


---

## 5. Metadatos y estándares <a name="5-metadatos-y-estandares"></a>

Los **metadatos** son descripciones estructuradas que permiten entender, descubrir y reutilizar los datos. Siguen estructuras normalizadas conocidas como **esquemas de metadatos** y, cuando se alinean con vocabularios compartidos, habilitan la interoperabilidad semántica.

### Importancia de la metadata

- Permiten describir el contenido, contexto y estructura de los datos de manera detallada y legible por máquinas.
- Facilitan la búsqueda, comprensión, interoperabilidad y reutilización de los datos por parte de los usuarios y los sistemas informáticos.

### Estándares de metadatos

#### Generales
- **Dublin Core**: Estándar general y ampliamente utilizado para describir una amplia variedad de recursos digitales y físicos. Proporciona un conjunto básico de elementos de metadatos para facilitar la interoperabilidad.
- **DataCite Metadata Schema**: Enfocado en la citación y el registro de datos de investigación, incluyendo identificadores persistentes como DOI. Facilita la identificación, acceso y reutilización de conjuntos de datos.
- **ISO 19115**: Estándar internacional para metadatos de información geoespacial. Define la estructura y contenido de los metadatos para describir datos geoespaciales y servicios relacionados.

#### Ciencias sociales y economía
- **DDI (Data Documentation Initiative)**: Estándar para metadatos en ciencias sociales, comportamiento y economía.
- **SDMX (Statistical Data and Metadata eXchange)**: Estándar para el intercambio de datos y metadatos estadísticos, utilizado por organizaciones estadísticas y bancos centrales.

#### Ciencias de la salud
- **CDISC (Clinical Data Interchange Standards Consortium)**: Estándares para datos clínicos y ensayos clínicos.
- **HL7 (Health Level Seven)**: Conjunto de estándares para el intercambio e integración de información electrónica de salud.

#### Ciencias de la vida y biología
- **Darwin Core (DwC)**, **MIAME**, **MINSEQE**, **EML**, **SBML**, **BioPAX**: Estándares clave para la descripción de datos biológicos, ecológicos y genómicos.

#### Humanidades digitales y patrimonio cultural
- **TEI**, **METS**, **PREMIS**, **MODS**, **VRA Core**, **LIDO**, **EAD**, **ONIX**, **CIDOC CRM**, **IIIF**: Diversos estándares para la representación, preservación y descripción de objetos digitales, documentos textuales y obras culturales.

#### Ciencias de la tierra y medio ambiente
- **CF Conventions**, **INSPIRE**, **CSDGM**: Normativas para asegurar documentación coherente de datos espaciales y ambientales.

#### Ingeniería y manufactura
- **STEP**: Estándar para el intercambio de modelos de productos industriales.

#### Educación
- **LOM (Learning Object Metadata)**: Estándar para describir objetos de aprendizaje.

#### Servicios web y datos abiertos
- **DCAT**, **OAI-PMH**: Vocabularios para facilitar la interoperabilidad en catálogos y recolección automatizada de metadatos.

### Uso de vocabularios controlados y ontologías

- Emplear vocabularios y ontologías estandarizados como **Schema.org**, **FOAF**, **DCMI Terms**.
- Favorecen la interoperabilidad semántica y una comprensión común de los términos.
- Asegurar que estos vocabularios estén alineados con los principios **FAIR** y sean sostenibles a largo plazo.

### Elementos clave de los metadatos

- **Título**
- **Autores/Colaboradores** (con **ORCID** y **ROR**)
- **Resumen/Descripción**
- **Palabras clave** (preferentemente con vocabularios controlados)
- **Fecha de publicación**
- **Fecha de creación y modificación**
- **Licencia** (ej. **CC BY**, **CC0**)
- **Identificador persistente** (ej. **DOI**)
- **Proveniencia**
- **Métodos**
- **Estándares y formatos utilizados**
- **Información de contacto**

📌 **Más información:**
- [FAIR Metadata Recommendations](https://doi.org/10.1371/journal.pcbi.1009041)  
  Recomendaciones prácticas para mejorar la calidad de los metadatos según los principios FAIR.

---

## 6. Licencias y Derechos de Uso <a name="6-licencias-y-derechos-de-uso"></a>

Las licencias abiertas facilitan la reutilización de datos:

### Tipos de Licencias Comunes para Datos:
- **Creative Commons Zero (CC0)**: Sin restricciones, dominio público. Permite el uso, compartición y modificación sin atribución.
- **Creative Commons Attribution (CC BY)**: Requiere atribución al creador. Permite el uso comercial y modificaciones siempre que se otorgue el crédito adecuado.
- **Creative Commons Attribution-ShareAlike (CC BY-SA)**: Requiere atribución y compartir bajo la misma licencia. Promueve la distribución en los mismos términos.
- **Open Data Commons Open Database License (ODbL)**: Requiere atribución y compartir con la misma licencia para bases de datos. Específico para conjuntos de datos y bases de datos.
- **Public Domain Dedication and License (PDDL)**: Equivalente a CC0 para datos y bases de datos, dedicando los datos al dominio público.

### Tipos de Licencias Comunes para Código y Software:
- **Apache 2.0 License**:
  - Licencia permisiva que permite el uso, modificación y distribución del software.
  - Requiere atribución y proporciona una concesión de patentes, protegiendo a los usuarios del software contra reclamaciones de patentes.
- **MIT License**:
  - Licencia permisiva simple que permite el uso, copia, modificación y distribución del software.
  - Requiere atribución al autor original en copias o modificaciones.
- **GNU General Public License (GPL)**:
  - Licencia copyleft que permite el uso, modificación y distribución del software, siempre que las obras derivadas se distribuyan bajo la misma licencia.
  - Promueve que el software derivado permanezca libre y abierto.
- **3-clause BSD License**:
  - Licencia permisiva que permite el uso, modificación y distribución con atribución obligatoria.
  - No impone restricciones en trabajos derivados.
- **Mozilla Public License (MPL) 2.0**:
  - Licencia híbrida que permite combinar código abierto con código propietario, siempre que las modificaciones al código con licencia MPL se compartan bajo la misma licencia.

📌 **Más información:**
- [Recopilación de licencias según tipo de objeto digital](https://doi.org/10.5281/zenodo.8222781)  
  Tabla resumen que vincula tipos de productos digitales con licencias recomendadas para su publicación y reutilización.

- [Choose a License](https://choosealicense.com/)  
  Herramienta interactiva para entender y seleccionar licencias de software de forma accesible.

- [SPDX License List](https://spdx.org/licenses/)  
  Lista estandarizada de licencias mantenida por la Linux Foundation, útil para referencias técnicas y automatización.

- [Software Licenses in Plain English](https://www.tldrlegal.com/)  
  Sitio que ofrece explicaciones accesibles y legibles para no especialistas sobre licencias comunes de software.

---

### Consideraciones al elegir una licencia:

#### Para Datos:

##### **Objetivos de Reutilización**
- ¿Se desea permitir el uso comercial y/o modificaciones de los datos?
- ¿Se requiere que las derivaciones se compartan bajo la misma licencia?

##### **Regulaciones Legales y Éticas**
- Cumplir con leyes de derechos de autor, protección de datos personales (ej. **GDPR**) y otras regulaciones locales o internacionales.
- Considerar implicaciones éticas, especialmente si los datos incluyen información sensible o de poblaciones vulnerables.

##### **Licencias Legibles por Máquina**
- Usar formatos que permitan que la licencia sea interpretada por sistemas informáticos, como **Creative Commons Rights Expression Language (CC REL)** o **DCAT** para catálogos de datos.

#### Para Código y Software:

##### **Tipo de Licencia**
- **Licencias Permisivas** (Apache 2.0, MIT, BSD):
  - Permiten el uso, modificación y distribución con pocas restricciones.
  - Adecuadas si se busca maximizar la adopción y flexibilidad en el uso del código.
- **Licencias Copyleft** (GPL, LGPL):
  - Requieren que los trabajos derivados se distribuyan bajo la misma licencia.
  - Ideales si se desea asegurar que el software y sus derivados permanezcan libres y abiertos.

##### **Compatibilidad de Licencias**
- Asegurar que la licencia elegida sea compatible con las licencias de cualquier código de terceros utilizado.
- Evitar conflictos legales al combinar código con diferentes licencias.

##### **Requisitos de Atribución y Aviso**
- Incluir cualquier aviso de derechos de autor y atribución requerido por la licencia.

##### **Transparencia y Consistencia**
- Especificar claramente la licencia en los metadatos, documentación, repositorios y puntos de acceso a datos y código.
- Incluir archivos de licencia (por ejemplo, **LICENSE.txt**) en los repositorios de código.

##### **Implicaciones en Interoperabilidad y Reutilización**
- Licencias más abiertas y permisivas facilitan una mayor interoperabilidad y reutilización.
- Licencias más restrictivas pueden limitar la capacidad de terceros para reutilizar o integrar los datos y código en otros proyectos.

##### **Consultas Legales**
- Si hay dudas sobre qué licencia elegir, considerar consultar con un experto legal para garantizar cumplimiento y adecuación.

---

### Pasos para Implementar la Licencia:

#### **Seleccionar la Licencia Apropiada**
- Evaluar los objetivos del proyecto y consideraciones legales y éticas para elegir la licencia más adecuada para los datos y el código.

#### **Aplicar la Licencia a los Datos y el Código**

##### **Para Datos:**
- Incluir una nota de licencia en la documentación, archivos **README** y metadatos.
- Usar identificadores y enlaces a la licencia oficial.

##### **Para Código:**
- Incluir un archivo de licencia (**LICENSE.txt**) en el repositorio.
- Agregar encabezados de licencia en los archivos de código fuente si es apropiado.

#### **Usar Enlaces y Recursos Estándar**
- Proporcionar enlaces a la versión oficial de la licencia para facilitar su acceso y verificación.

#### **Licencias Legibles por Máquina**
- Para datos y código, utilizar formatos que permitan la interpretación de la licencia por sistemas informáticos.

---

## 7. Evaluación FAIR y Herramientas <a name="7-evaluacion-fair-y-herramientas"></a>

Los principios FAIR no son una lista de chequeo cerrada, sino un marco evaluable. Existen herramientas comunitarias que permiten medir el cumplimiento FAIR de un conjunto de datos o de un repositorio, ya sea mediante formularios interactivos, validadores en línea o integraciones automatizadas con APIs. Estas herramientas comparan los metadatos, licencias, formatos y persistencia de los identificadores con estándares aceptados, y asignan una puntuación o nivel de madurez FAIR.

### FAIR-Aware
- **Descripción**: FAIR-Aware es una plataforma educativa desarrollada por **DANS (Data Archiving and Networked Services)** que ayuda a investigadores y gestores de datos a comprender mejor los principios **FAIR** y cómo aplicarlos a sus datos. Proporciona una autoevaluación guiada que **no entrega puntuaciones**, pero sensibiliza sobre los aspectos clave de FAIR.  
- **Enlace**: [FAIR-Aware](https://fairaware.dans.knaw.nl/)

### F-UJI
- **Descripción**: Herramienta automática para la evaluación de **FAIRness** de conjuntos de datos registrados con DOI en DataCite. La evaluación de F-UJI está basada en 16 de las 17 métricas desarrolladas en el proyecto [FAIRsFAIR](https://www.fairsfair.eu/).  
- **Enlace**: [F-UJI](https://catalogue.fair-impact.eu/resources/f-uji)

### FAIR Data Maturity Model
- **Descripción**: Modelo desarrollado por el **Grupo de Trabajo de la RDA** para evaluar sistemáticamente el grado de cumplimiento de los principios **FAIR**. Proporciona un conjunto de indicadores y métricas para evaluar la madurez FAIR de los datos.  
- **Enlace**: [FAIR Data Maturity Model](https://zenodo.org/records/3909563)

### How FAIR is
- **Descripción**: Herramienta de línea de comando que permite analizar el cumplimiento del software con las recomendaciones de [fair-software.eu](https://fair-software.eu/). Especialmente útil para proyectos de código abierto alojados en plataformas como GitHub o GitLab.  
- **Enlace**: [howFAIRis](https://github.com/fair-software/howfairis)

### Autoevaluación de FAIR software
- **Descripción**: Lista interactiva de verificación con preguntas sobre el **FAIRness** del software de investigación. Esta lista genera una insignia (badge) que los propietarios de proyectos pueden incluir en su README para comunicar el estado del proyecto a los visitantes.  
- **Enlace**: [FAIR software check-list](https://fairsoftwarechecklist.net/v0.2/)

### FAIR Cookbook
- **Descripción**: Colección de recetas prácticas que guían a los usuarios a través de los pasos necesarios para implementar los principios **FAIR** en la gestión y publicación de datos.  
- **Enlace**: [FAIR Cookbook](https://faircookbook.elixir-europe.org/)

### FAIRification Process
- **Descripción**: Guía detallada y mantenida por la iniciativa **GO FAIR**, que describe el proceso de "FAIRificación" de los datos, incluyendo pasos prácticos y consideraciones técnicas.  
- **Enlace**: [FAIRification Process](https://www.go-fair.org/fair-principles/fairification-process/)

### Otros recursos relevantes

#### DMT Clearinghouse
- **Descripción**: Repositorio curado de materiales educativos, herramientas y recursos sobre gestión de datos. Permite buscar guías, plantillas y presentaciones útiles para investigadores y data stewards.  
- **Enlace**: [https://dmtclearinghouse.esipfed.org/search](https://dmtclearinghouse.esipfed.org/search)

#### The Turing Way
- **Descripción**: Proyecto comunitario que ofrece una guía integral para la ciencia de datos reproducible, colaborativa y ética. Incluye aspectos técnicos y sociales complementarios a FAIR, como liderazgo, diversidad y colaboración abierta.  
- **Enlace**: [https://the-turing-way.netlify.app/](https://the-turing-way.netlify.app/)

---

## 8. Tipos de Investigación y Requisitos FAIR <a name="8-tipos-de-investigacion-y-requisitos-fair"></a>

Los principios FAIR deben adaptarse a las particularidades de cada tipo de investigación. A continuación, se presentan recomendaciones específicas para garantizar su aplicación adecuada en contextos observacionales, experimentales, computacionales y clínico-sociales.

### 8.1 Investigación Observacional <a name="81-investigacion-observacional"></a>

#### Requisitos:
- **Documentar instrumentos y métodos**  
  Describir en detalle los instrumentos utilizados y los métodos de recopilación de datos. Utilizar estándares reconocidos en el dominio, como **Darwin Core** para biodiversidad o **ISO 19115** para metadatos geoespaciales.
  
- **Registrar coordenadas y tiempo**  
  Proporcionar información precisa sobre la ubicación geográfica (coordenadas GPS) y marcas de tiempo, usando formatos estandarizados como **ISO 8601**.

- **Incluir metadatos contextuales**  
  Documentar condiciones ambientales, contexto del estudio y factores que puedan influir en los datos.

- **Considerar aspectos éticos y legales**  
  Obtener consentimiento informado cuando corresponda y cumplir con regulaciones de protección de datos.

---

### 8.2 Investigación Experimental <a name="82-investigacion-experimental"></a>

#### Requisitos:
- **Describir condiciones experimentales y diseño**  
  Documentar el diseño experimental, procedimientos y protocolos utilizados. Incluir información sobre materiales, reactivos y sujetos experimentales.

- **Registrar calibraciones y configuraciones**  
  Documentar calibraciones de equipos, configuraciones de instrumentos y parámetros relevantes.

- **Preservar datos brutos y procesados**  
  Almacenar y compartir tanto datos en bruto como procesados, incluyendo métodos de procesamiento y análisis.

- **Usar estándares del dominio**  
  Utilizar estándares como **MIAME** para microarrays o consultar **FAIRsharing** para otros estándares biomédicos pertinentes.

- **Cumplir con requisitos éticos**  
  Obtener aprobaciones de comités de ética y cumplir con normativas institucionales y legales.

---

### 8.3 Investigación Computacional <a name="83-investigacion-computacional"></a>

#### Requisitos:
- **Documentar código, dependencias y entorno**  
  Proporcionar acceso al código fuente, scripts y bibliotecas utilizadas. Utilizar sistemas de control de versiones como `Git` y describir el entorno de ejecución (SO, versiones, `Docker`, `Singularity`, etc.).

- **Preservar entornos y reproducibilidad**  
  Compartir contenedores, imágenes de máquina virtual o notebooks (`Jupyter`, `RMarkdown`) que permitan la reproducción completa del análisis.

- **Registrar parámetros y seeds**  
  Documentar todos los parámetros de entrada, configuraciones y semillas aleatorias utilizadas en simulaciones o modelos.

- **Publicar y citar el código**  
  Asignar un **DOI** al código y depositarlo en repositorios como **Zenodo**, **GitHub** o **GitLab**.

- **Aplicar licencias adecuadas**  
  Usar licencias como **Apache 2.0** o **GPL** y documentarlas claramente en el repositorio (`LICENSE.txt`).

---

### 8.4 Investigación Clínica y Social <a name="84-investigacion-clinica-y-social"></a>

#### Requisitos:
- **Cumplir con regulaciones de protección de datos**  
  Observar normativas como **GDPR** (UE), **LGPD** (Brasil), **HIPAA** (EE.UU.) u otras locales aplicables.

- **Aplicar técnicas de anonimización y seudonimización**  
  Reducir riesgos de reidentificación mediante estrategias técnicas y documentar dichas medidas en los metadatos.

- **Obtener consentimiento informado**  
  Recoger autorizaciones explícitas para la recopilación, uso y posible compartición de datos.

- **Gestionar aprobaciones éticas y regulatorias**  
  Contar con la aprobación de los comités de ética y cumplir con normativas institucionales.

- **Implementar acceso restringido y controlado**  
  Establecer mecanismos que limiten el acceso a los datos sensibles, tales como acuerdos de uso o plataformas seguras de datos.

---

## 9. Planificación estructurada de productos de investigación <a name="9-planificacion-estructurada-de-productos-de-investigacion"></a>

En proyectos de investigación contemporáneos, es crucial planificar desde el inicio cómo se gestionarán, compartirán y preservarán los productos digitales. Esta planificación aplica a los datos, el software, los flujos de trabajo, la documentación y los metadatos. A continuación se presentan los tipos principales de planes, su evolución hacia formatos estructurados y herramientas clave para su elaboración.

### 9.1 Planes de Gestión de Datos (DMP) <a name="91-planes-de-gestion-de-datos"></a>

Los Planes de Gestión de Datos (DMP) son documentos vivos que describen cómo se generarán, organizarán, documentarán, almacenarán, compartirán y preservarán los datos de investigación. Son obligatorios en convocatorias de financiamiento y en muchos repositorios.

[Ejemplo completo: ver Anexo 9.3](#93-anexo-c-datos-minimos-para-un-plan-de-gestion-de-datos-dmp)

Elementos clave:
- Tipos de datos y métodos de recopilación.
- Estrategias de documentación, licencias y estándares de metadatos.
- Planes de preservación, seguridad y acceso.
- Repositorios y licencias seleccionadas.

Herramientas recomendadas:
- [Data Stewardship Wizard (DSW)](https://ds-wizard.org/)
- [DMPonline (DCC)](https://dmponline.dcc.ac.uk/)
- [RDMO](https://rdmorganiser.github.io/)

### 9.2 Planes de Gestión de Software (SMP) <a name="92-planes-de-gestion-de-software"></a>

El Plan de Gestión de Software (SMP) es el equivalente a un DMP, orientado al desarrollo, documentación, publicación y sostenibilidad del software producido en investigación. Se alinean con los principios FAIR4RS, que promueven software reutilizable, reproducible y citable.

[Ejemplo completo: ver Anexo 9.4](#94-anexo-d-datos-minimos-para-un-plan-de-gestion-de-software-smp)

Aspectos incluidos:
- Ciclo de vida del software, control de versiones y gobernanza.
- Publicación en repositorios como Zenodo o Software Heritage.
- Licencias, citación, documentación y pruebas.
- Estrategias de sustentabilidad al finalizar el proyecto.

Guías útiles:
- [Guía del Netherlands eScience Center](https://doi.org/10.5281/zenodo.6245751)
- [SMP Checklist – Software Sustainability Institute](https://software.ac.uk/resources/guides/software-management-plans)

### 9.3 Planes accionables por máquina (maDMPs y maSMPs) <a name="93-planes-maquina"></a>

Los maDMPs y maSMPs están diseñados para ser interpretados por sistemas automatizados, APIs y herramientas de seguimiento FAIR. Representan la evolución natural de los planes tradicionales hacia esquemas estructurados y legibles por máquina.

Características:
- Uso de formatos estructurados como JSON o JSON-LD.
- Validación mediante plantillas y esquemas sintácticos.
- Integración con sistemas institucionales, repositorios y plataformas de gestión.

Recurso clave:
- [RDA maDMP WG – DMP Common Standard](https://github.com/RDA-DMP-Common/RDA-DMP-Common-Standard)

Herramientas disponibles:
- Data Stewardship Wizard (DSW)
- RDMO
- DMPonline

Estos esquemas estructurados se articulan con las herramientas de evaluación descritas en la sección [7. Evaluación FAIR y Herramientas](#7-evaluacion-fair-y-herramientas), fortaleciendo la trazabilidad y cumplimiento desde etapas tempranas del proyecto.


## 10. Extensiones para la trazabilidad e interoperabilidad FAIR <a name="10-extensiones-trazabilidad-interoperabilidad-fair"></a>

Este bloque aborda elementos avanzados que refuerzan la trazabilidad, la citación y la interoperabilidad técnica de los productos de investigación, en línea con los principios FAIR y las infraestructuras internacionales emergentes.

### 10.1 Trazabilidad, versionado y mantenimiento <a name="101-trazabilidad-versionado-mantenimiento"></a>

- Usar versionado semántico (ej. `v1.0`, `v2.1`) en datos, software, metadatos y notebooks.
- Asignar identificadores persistentes por versión (ej. DOI en Zenodo o Figshare).
- Relacionar versiones usando propiedades como `isNewVersionOf`, `isPreviousVersionOf` o `isVersionOf`.
- Documentar cambios relevantes mediante archivos `CHANGELOG.md` o descripciones en repositorios.
- Incluir estrategias de preservación digital y registro de modificaciones (logs o auditorías institucionales).

### 10.2 Gestión de flujos de trabajo y modelos computacionales <a name="102-gestion-flujos-modelos"></a>

- Documentar workflows con herramientas como Galaxy, Nextflow, Snakemake o CWL.
- Asignar DOIs a flujos de trabajo mediante repositorios como [WorkflowHub](https://workflowhub.eu/) o [Dockstore](https://dockstore.org/).
- Detallar entradas, salidas, software usado y contenedores (ej. Docker, Singularity).
- Describir los flujos con metadatos estructurados compatibles con esquemas FAIR.
- Incluir notebooks interactivos (Jupyter, RMarkdown) como parte de los pipelines.

### 10.3 Requisitos técnicos para la interoperabilidad FAIR <a name="103-requisitos-tecnicos-interoperabilidad"></a>

- Asegurar el uso de protocolos estándar: HTTPS, RESTful APIs, OAI-PMH, SPARQL.
- Usar formatos abiertos y estructurados: JSON-LD, RDF, NetCDF, CSV con delimitadores consistentes.
- Describir recursos mediante vocabularios como **DCAT**, **schema.org**, **DATS**.
- Habilitar el descubrimiento a través de endpoints públicos y catálogos abiertos institucionales.
- Estos elementos son clave para lograr **interoperabilidad técnica y accionabilidad por máquinas**.

### 10.4 Citación y métricas de uso de productos FAIR <a name="104-citacion-metricas-fair"></a>

- Incluir archivos de citación en software (`CITATION.cff`), datos (`datacite.yml`) y código (`codemeta.json`).
- Validar periódicamente los archivos de citación con herramientas automatizadas.
- Usar identificadores como DOI y ARK también para materiales complementarios (datasets intermedios, notebooks, visualizaciones).
- Promover la citación en estilos formales (APA, MLA, Vancouver), reconociendo datasets y software como productos académicos.
- Crear páginas persistentes (landing pages) con metadatos completos y enlaces a versiones.
- Monitorear el uso mediante plataformas como:
  - [Make Data Count](https://makedatacount.org/)
  - [Software Heritage](https://www.softwareheritage.org/)
  - [Data Citation Corpus](https://datasetsearch.research.google.com/)

### 10.5 Estructura de metadatos procesables por máquinas <a name="105-metadatos-maquina"></a>

- Adoptar estructuras de metadatos legibles por máquinas para permitir la automatización de validación, monitoreo y evaluación FAIR.
- Usar esquemas como `codemeta.json` para software, `datacite.yml` para datos, y `CITATION.cff` para citación formal.
- Emplear vocabularios como **DCAT**, **schema.org**, **DATS** y **DCMI Terms** para describir recursos de forma estandarizada.
- Generar planes de gestión FAIR con herramientas como **Data Stewardship Wizard**, habilitando la producción de **maDMPs**.

📌 **Más información:**
- [FAIR Cookbook](https://faircookbook.elixir-europe.org/)  
  Guía técnica para implementar prácticas FAIR con ejemplos detallados por tipo de dato y dominio.

- [WorkflowHub](https://workflowhub.eu/)  
  Repositorio especializado para compartir, versionar y describir workflows científicos siguiendo los principios FAIR.

- [Software Heritage](https://www.softwareheritage.org/)  
  Archivo global de software fuente, útil para garantizar trazabilidad y preservación a largo plazo de código científico.

- [FAIRsharing](https://fairsharing.org/)  
  Registro curado de estándares, repositorios y políticas FAIR, categorizado por disciplina y tipo de producto digital.

- [FAIR Principles (GO FAIR)](https://www.go-fair.org/fair-principles/)  
  Referencia oficial de los principios FAIR, mantenida por la iniciativa internacional GO FAIR.

- [Data Stewardship Wizard – maDMPs](https://ds-wizard.org/machine-actionability)  
  Plataforma para generar planes de gestión de datos legibles por máquina y alineados con metadatos estructurados.

---

📌 **Más información:**

- [FAIR Cookbook](https://faircookbook.elixir-europe.org/)  
  Guía técnica para implementar prácticas FAIR con ejemplos detallados por tipo de dato y dominio.

- [WorkflowHub](https://workflowhub.eu/)  
  Repositorio especializado para compartir, versionar y describir workflows científicos siguiendo los principios FAIR.

- [Software Heritage](https://www.softwareheritage.org/)  
  Archivo global de software fuente, útil para garantizar trazabilidad y preservación a largo plazo de código científico.

- [FAIRsharing](https://fairsharing.org/)  
  Registro curado de estándares, repositorios y políticas FAIR, categorizado por disciplina y tipo de producto digital.

- [FAIR Principles (GO FAIR)](https://www.go-fair.org/fair-principles/)  
  Referencia oficial de los principios FAIR, mantenida por la iniciativa internacional GO FAIR.


---

## 11. Anexos <a name="11-anexos"></a>

### 11.1 Anexo A: Checklist de Evaluación FAIR <a name="111-anexo-a-checklist-de-evaluacion-fair"></a>

Esta checklist permite autoevaluar el cumplimiento de los principios FAIR en productos digitales de investigación. Se recomienda utilizarla al momento de planificar o depositar datos, software o documentos para asegurar su trazabilidad y reutilización.

#### **Findable (Encontrable)**

- [ ] ¿Los datos tienen un identificador único y persistente (por ejemplo, DOI, Handle)?
- [ ] ¿Los metadatos proporcionan una descripción detallada del conjunto de datos e incluyen el identificador persistente de los datos descritos?
- [ ] ¿Los datos y metadatos están almacenados en repositorios especializados o catálogos accesibles por usuarios y sistemas?
- [ ] ¿Se utilizan estándares de metadatos reconocidos y vocabularios controlados (ej. Dublin Core, DataCite, Schema.org)?
- [ ] ¿Se incluyen palabras clave relevantes utilizando vocabularios controlados para facilitar la búsqueda?

#### **Accessible (Accesible)**

- [ ] ¿Los datos son accesibles a través de protocolos abiertos, gratuitos y universalmente implementables (ej. HTTPS, APIs RESTful)?
- [ ] ¿Las condiciones y procedimientos para acceder a los datos están claramente especificados, incluyendo procesos de autenticación si son necesarios?
- [ ] Si es necesario, ¿existen mecanismos de autenticación y autorización bien definidos, estandarizados y seguros?
- [ ] ¿Los metadatos siguen siendo accesibles sin restricciones, incluso si los datos ya no están disponibles?

#### **Interoperable (Interoperable)**

- [ ] ¿Se utilizan formatos de datos abiertos y ampliamente aceptados (ej. RDF, OWL, JSON-LD)?
- [ ] ¿Se emplean vocabularios estandarizados y ontologías compartidas que siguen los principios FAIR?
- [ ] ¿Los datos y metadatos incluyen referencias claras a otros recursos relacionados especificando la naturaleza de la relación?
- [ ] ¿Se aplican estándares de codificación consistentes (ej. UTF-8) y está la codificación documentada claramente?

#### **Reusable (Reutilizable)**

- [ ] ¿Se aplican licencias abiertas y bien definidas (ej. CC0, CC BY)?
- [ ] ¿Se proporciona información detallada sobre el origen e historial de los datos?
- [ ] ¿Los metadatos incluyen suficiente contexto para comprender y reutilizar los datos?
- [ ] ¿Se siguen estándares y convenciones de la comunidad en el dominio de los datos?
- [ ] ¿Se han realizado controles de calidad y están documentados los procedimientos de validación?

---

### 11.2 Anexo B: Ejemplo de Metadatos Estructurados <a name="112-anexo-b-ejemplo-de-metadatos-estructurados"></a>

A continuación se muestra un ejemplo básico de metadatos estructurados en formato YAML, adaptado para ser comprensible por personas sin formación técnica, según el esquema Dublin Core.

```yaml
title: "Datos climáticos diarios de la región andina (2000-2020)"
authors:
  - "Dr. María Pérez (Instituto de Climatología)"
  - "Dr. Juan Gómez (Universidad Nacional)"
editor: "Repositorio Nacional de Datos Científicos"
publication_date: "2023-05-15"
identifier: "DOI: 10.1234/abcd.2023.efgh"
summary: "Este conjunto de datos contiene registros diarios de temperatura, precipitación y humedad relativa en la región andina, recopilados entre los años 2000 y 2020. Los datos fueron obtenidos de estaciones meteorológicas certificadas y pueden ser utilizados para estudios climáticos y ambientales."
keywords:
  - "Climatología"
  - "Región Andina"
  - "Temperatura"
  - "Precipitación"
  - "Humedad Relativa"
spatial_coverage:
  latitude: "-9.19 to -5"
  longitude: "-81.33 to -34.79"
temporal_coverage: "2000-01-01 / 2020-12-31"
format: "CSV (valores separados por comas)"
file_size: "150 MB"
license: "Creative Commons Attribution 4.0 International (CC BY 4.0)"
language: "Español"
relationship: "Este conjunto de datos complementa el estudio 'Impacto del Cambio Climático en la Región Andina' (DOI: 10.5678/ijkl.2022.mnop)"
rights: "El uso de estos datos requiere atribución a los autores originales bajo la licencia CC BY 4.0."
source: "Los datos fueron recopilados por el Instituto de Climatología en colaboración con la Universidad Nacional."
contact:
  email: "contacto@datosclimaticos.org"
  phone: "+56 2 1234 5678"
```

```yaml
additional_metadata:
  data_origin: "Los datos fueron procesados y validados utilizando ClimateDataTool v2.1. Se eliminaron registros incompletos y se corrigieron valores atípicos identificados mediante análisis estadístico."
  methodology: "Se usaron sensores calibrados de alta precisión para la recolección de datos. La frecuencia de medición fue diaria, y los datos fueron almacenados y respaldados siguiendo protocolos estándar."
```

### 11.3 Anexo C: Datos mínimos para un Plan de Gestión de Datos (DMP) <a name="113-anexo-c-datos-minimos-para-un-plan-de-gestion-de-datos-dmp"></a>

Un **Plan de Gestión de Datos (DMP)** es un documento esencial que describe cómo se generarán, documentarán, almacenarán, compartirán y preservarán los datos de investigación. A continuación, se presentan los elementos mínimos que debe contener un DMP.

### 1. Información del Proyecto
- [ ] **Título del proyecto:** Nombre oficial del estudio o iniciativa.
- [ ] **Investigadores responsables:** Nombres y afiliaciones de los principales responsables del proyecto.
- [ ] **Fuentes de financiamiento:** Instituciones, agencias o programas que financian el proyecto.

### 2. Descripción de los Datos
- [ ] **Tipos de datos:** ¿Qué tipo de datos se generarán o recopilarán? (Ej.: encuestas, imágenes, datos tabulares, secuencias genómicas, etc.)
- [ ] **Formatos de datos:** Formatos recomendados para garantizar la interoperabilidad y accesibilidad a largo plazo (Ej.: CSV, JSON, XML, NetCDF, FITS).
- [ ] **Volumen estimado de datos:** Aproximación del tamaño de los datos generados (Ej.: 100 GB, 1 TB, etc.).
- [ ] **Metodología de recolección:** ¿Cómo se generarán los datos? (Ej.: sensores, simulaciones, encuestas, bases de datos existentes).

### 3. Documentación y Metadatos
- [ ] **Estándares de metadatos:** Especificar qué estándares se utilizarán para describir los datos (Ej.: Dublin Core, DataCite, ISO 19115).
- [ ] **Herramientas de documentación:** Métodos y plataformas usadas para generar documentación (Ej.: README.txt, Data Dictionaries, esquemas JSON-LD).
- [ ] **Vocabularios controlados y ontologías:** Identificar si se utilizarán vocabularios estandarizados (Ej.: FOAF, Schema.org, Darwin Core).

### 4. Almacenamiento y Seguridad
- [ ] **Ubicación de los datos durante el proyecto:** ¿Dónde se almacenarán los datos en curso? (Ej.: servidores locales, nube, repositorios de universidades).
- [ ] **Estrategia de respaldo:** Métodos de respaldo y periodicidad (Ej.: copias diarias/semanales en almacenamiento redundante).
- [ ] **Medidas de seguridad:** ¿Qué protocolos se implementarán para garantizar la seguridad de los datos? (Ej.: encriptación, acceso restringido).

### 5. Preservación y Compartición
- [ ] **Repositorio seleccionado:** ¿Dónde se depositarán los datos para su preservación a largo plazo? (Ej.: Zenodo, Dryad, re3data).
- [ ] **Periodo de retención:** ¿Por cuánto tiempo se almacenarán los datos después de finalizado el proyecto? (Ej.: 5 años, 10 años, indefinido).
- [ ] **Estrategia de acceso:** ¿Quién podrá acceder a los datos?  
  - [ ] Acceso abierto (CC BY, CC0).  
  - [ ] Acceso restringido (solo colaboradores del proyecto).  
  - [ ] Acceso limitado (solicitud previa requerida).
- [ ] **Licencias y condiciones de uso:** ¿Qué licencia se aplicará a los datos? (Ej.: CC BY 4.0, ODbL, MIT License).
- [ ] **Planes de interoperabilidad:** ¿Cómo se garantizará la compatibilidad con otras plataformas y estándares FAIR?

Un **DMP bien estructurado** es clave para asegurar la **transparencia, reproducibilidad e interoperabilidad** de los datos científicos. Se recomienda revisar periódicamente este plan para adaptarlo a nuevas necesidades o requisitos institucionales.

---

### 11.4 Anexo D: Datos mínimos para un Plan de Gestión de Software (SMP) <a name="114-anexo-d-datos-minimos-para-un-plan-de-gestion-de-software-smp"></a>

El **Plan de Gestión de Software (PGS)** describe cómo se desarrollará, documentará y compartirá el software durante un proyecto de investigación. Su objetivo es garantizar que el software sea **mantenido, utilizable y accesible a largo plazo**, apoyando la trazabilidad de su desarrollo y facilitando su reutilización, de acuerdo con los principios FAIR4RS (Findable, Accessible, Interoperable, Reusable for Research Software).

### Comparación entre FAIR y FAIR4RS

| Principio      | FAIR (datos)                                                     | FAIR4RS (software)                                                                 |
|----------------|------------------------------------------------------------------|------------------------------------------------------------------------------------|
| **Findable**   | Los datos deben tener un identificador persistente y estar indexados en un repositorio. | El software debe tener un identificador, versión persistente y estar registrable. |
| **Accessible** | Los metadatos y datos deben estar disponibles con protocolos abiertos. | El código fuente, documentación y ejecutables deben estar accesibles (repositorio abierto, instrucciones de instalación). |
| **Interoperable** | Uso de vocabularios controlados y formatos estándar.          | Uso de lenguajes estándar, interoperabilidad entre módulos, y metadatos de ejecución. |
| **Reusable**   | Licencias claras, documentación adecuada y proveniencia completa. | Licencia de software compatible, documentación, dependencias y entorno reproducible. |

📌 **Más información:**
- [Martínez-Ortiz, C., Bakker, P., & Koning, H. (2022). *Practical guide to Software Management Plans*. Netherlands eScience Center](https://doi.org/10.5281/zenodo.6245751)  
  Guía práctica para desarrollar y aplicar planes de gestión de software en proyectos de investigación.

### Elementos mínimos recomendados que debe contener un PGS:

1. **Información general del software**
   - Nombre del software y del proyecto asociado
   - Instituciones y responsables (desarrolladores, mantenedores)
   - Periodo de desarrollo y/o mantenimiento
   - Recursos necesarios (infraestructura, personal)

2. **Propósito y alcance**
   - Objetivo científico del software
   - Problema que resuelve
   - Usuarios esperados y contexto de aplicación

3. **Repositorio y control de versiones**
   - URL del repositorio (por ejemplo, GitHub, GitLab)
   - Uso de control de versiones (por ejemplo, Git)
   - Estrategia de *releases* y asignación de DOI (por ejemplo, Zenodo)
   - Historial de cambios

4. **Documentación**
   - Manuales de usuario
   - Guías de instalación y despliegue
   - Documentación para desarrolladores
   - Herramientas de documentación (Markdown, ReadTheDocs, etc.)

5. **Calidad del software**
   - Pruebas (unitarias, integración, regresión)
   - Revisión de código (*code review*)
   - Uso de herramientas de calidad (linters, CI/CD)
   - Gestión de *issues* y errores

6. **Licenciamiento y aspectos legales**
   - Licencia elegida (MIT, GPL, Apache, etc.)
   - Consideraciones de copyright y atribución
   - Restricciones legales o éticas (por ejemplo, uso dual, privacidad)

7. **Publicación, citación y visibilidad**
   - Plataforma de publicación (Zenodo, Software Heritage, repositorio institucional)
   - Especificación de citación (CITATION.cff, codemeta.json)
   - Registro en catálogos o directorios de software científico

8. **Preservación y sostenibilidad**
   - Responsable(s) del mantenimiento
   - Plan de archivado a largo plazo
   - Compatibilidad futura (contenedores, gestión de dependencias)
   - Nivel de soporte tras el proyecto

9. **Soporte y gobernanza**
   - Canales de contacto o soporte para usuarios
   - Roles y responsabilidades del equipo
   - Recursos estimados para sostenibilidad

---

📌 **Más información**

**Principios y lineamientos FAIR para software:**

- [FAIR4RS Principles (RDA, FORCE11, ReSA)](https://doi.org/10.15497/RDA00068)  
  Principios FAIR adaptados para software, desarrollados por comunidades como RDA, FORCE11 y ReSA.

- [SMP Checklist – Software Sustainability Institute](https://software.ac.uk/resources/guides/software-management-plans)  
  Lista de verificación para planes de gestión de software, cubriendo documentación, licencias y sostenibilidad.

- [Plantilla de PGS – Wageningen University & Research](https://zenodo.org/record/10696023)  
  Ejemplo práctico de plan de gestión de software alineado con FAIR y adoptado por instituciones europeas.

**Herramientas para elaborar y gestionar PGS:**

- [Data Stewardship Wizard (DSW)](https://ds-wizard.org/)  
  Herramienta interactiva para construir DMPs y SMPs con vocabularios controlados y lógica FAIR.

- [RDA Workshop on Machine Actionable DMPs](https://www.dcc.ac.uk/events/RDAcolocated_machine_actionable_DMPs)  
  Taller de RDA y DCC sobre el desarrollo y adopción de DMPs automatizados.

- [DMPonline](https://dmponline.dcc.ac.uk/)  
  Plataforma para crear planes de gestión personalizados según requisitos de proyectos y financiadores.

- [RDMO – Research Data Management Organizer](https://rdmorganiser.github.io/)  
  Herramienta modular para planificar la gestión de datos y software a lo largo del ciclo de vida del proyecto.

**Preservación, licencias y metadatos:**

- [Software Heritage](https://www.softwareheritage.org/)  
  Archivo universal para preservar código fuente con identificadores persistentes (SWHID).

- [Codemeta](https://codemeta.github.io/)  
  Esquema de metadatos interoperables para describir y facilitar la citación de software científico.

**Herramientas para gestionar software científico:**

- [Tutorial GloBI (en español)](https://www.globalbioticinteractions.org/es/tutorial.html)  
  Guía práctica para documentar, versionar y publicar software científico con GitHub y Zenodo.

---
