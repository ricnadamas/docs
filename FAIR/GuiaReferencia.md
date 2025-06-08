# FAIR: Guía de Referencia General

## Índice

1. [Introducción](#1-introduccion)  
2. [Principios FAIR](#2-principios-fair)  
   2.1 [Findable (Encontrable)](#21-findable-encontrable)  
   2.2 [Accessible (Accesible)](#22-accessible-accesible)  
   2.3 [Interoperable](#23-interoperable)  
   2.4 [Reusable (Reutilizable)](#24-reusable-reutilizable)  
3. [Formatos de Datos y Recomendaciones](#3-formatos-de-datos-y-recomendaciones)  
4. [Metadatos y Estándares](#4-metadatos-y-estandares)  
5. [Licencias y Derechos de Uso](#5-licencias-y-derechos-de-uso)  
6. [Evaluación FAIR y Herramientas](#6-evaluacion-fair-y-herramientas)  
7. [Tipos de Investigación y Requisitos FAIR](#7-tipos-de-investigacion-y-requisitos-fair)  
   7.1 [Investigación Observacional](#71-investigacion-observacional)  
   7.2 [Investigación Experimental](#72-investigacion-experimental)  
   7.3 [Investigación Computacional](#73-investigacion-computacional)  
   7.4 [Investigación Clínica y Social](#74-investigacion-clinica-y-social)  
8. [Consideraciones éticas, lingüísticas y culturales](#8-consideraciones-eticas-linguisticas-y-culturales)  
9. [Anexos](#9-anexos)  
   9.1 [Anexo A: Checklist de Evaluación FAIR](#91-anexo-a-checklist-de-evaluacion-fair)  
   9.2 [Anexo B: Ejemplo de Metadatos Estructurados](#92-anexo-b-ejemplo-de-metadatos-estructurados)  
   9.3 [Anexo C: Datos mínimos para un Plan de Gestión de Datos (DMP)](#93-anexo-c-datos-minimos-para-un-plan-de-gestion-de-datos-dmp)  
   9.4 [Anexo D: Datos mínimos para un Plan de Gestión de Software (SMP)](#94-anexo-d-datos-minimos-para-un-plan-de-gestion-de-software-smp)  


**Este documento está disponible bajo la licencia CC BY 4.0** y puede ser actualizado con nuevas colaboraciones.

## Colaboradores

Esta guía ha sido elaborada con el apoyo de diversas personas y organizaciones comprometidas con la promoción de los principios FAIR. Se invita a otros colaboradores a contribuir con mejoras, actualizaciones y ejemplos adicionales.

- Ricardo Hartley Belmar @ricnadamas [ORCID:0000-0001-5058-9309](https://orcid.org/my-orcid?orcid=0000-0001-5058-9309)
- Isabel Abedrapo @yolaisa [ORCID:0000-0001-9990-0436](https://orcid.org/0000-0001-9990-0436)
- Priyanka Ojha @priya-gitTest [ORCID:0000-0002-6844-6493](https://orcid.org/0000-0002-6844-6493)
- Carlos Martinez-Ortiz @c-martinez [ORCID:0000-0001-5565-7577](https://orcid.org/0000-0001-5565-7577)

---

## 1. Introducción

Esta guía práctica tiene como objetivo facilitar la implementación de los principios **FAIR** en la gestión de datos de investigación y otros contextos donde la organización, trazabilidad y accesibilidad de la información digital son esenciales. No está dirigida únicamente a investigadores, sino también a bibliotecarios, gestores de datos, responsables de políticas científicas, desarrolladores de infraestructuras y cualquier persona interesada en la gestión eficiente de datos digitales.

Los principios FAIR buscan garantizar que los datos sean **Encontrables (Findable), Accesibles (Accessible), Interoperables (Interoperable) y Reutilizables (Reusable)**. Implementar estos principios facilita el acceso y reutilización de datos, mejora su visibilidad, y fomenta la colaboración científica.

Los principios FAIR fueron inicialmente pensados para su aplicación a datos, pero han sido adaptados a software de investigación mediante la creación de de los principios **FAIR4RS** (FAIR for Research Software). Cabe mencionar que en este contexto, software es utilizado como un termino inclusivo, abarcando desde pequeños scripts hasta complejas librerias.

Además de describir los principios FAIR, esta guía proporciona información sobre:
- **Estándares de metadatos** recomendados.
- **Formatos de datos** y su interoperabilidad.
- **Licencias y derechos de uso** para facilitar la reutilización.
- **Herramientas y metodologías** para evaluar la adopción de FAIR.
- **Ejemplos y recursos prácticos** para la implementación en diferentes contextos.

Para facilitar su aplicación, se incluyen listas de verificación y directrices para distintos tipos de proyectos.

---

## 2. Principios FAIR

📌 **Más información:**
- [Principios FAIR (material para taller). Autores Meyers, N., Escapil-Inchauspé, P., Egaña Aranguren, M., & Hartley Belmar, Ricardo](https://doi.org/10.6075/J0TM7BG5)
- [Traducción del Documento guía para el Plan de Gestión de Datos FAIR en Organizaciones e Instituciones. Autores Kirkpatrick, C. R., Cragin, M. H., & Meyers, N. (2024) (Translators Hartley Belmar, Ricardo; Meyers, Natalie)](https://doi.org/10.6075/J0ZC836W)

### 2.1 Findable (Encontrable)
Objetivo: Asegurar que los datos y metadatos puedan ser descubiertos fácilmente.

**Requisitos clave:**
- Uso de **identificadores persistentes (PIDs)** como DOI, Handle, ARK u otros, que permiten la referencia inequívoca a los conjuntos de datos.
- Almacenamiento de metadatos los identificadores persistentes. E.g. [PIDs](https://support.orcid.org/hc/en-us/articles/360006971013-What-are-persistent-identifiers-PIDs)
- Metadatos ricos que describan los datos de manera clara y estructurada.
- Indexación en **repositorios especializados** como Zenodo, DataCite o re3data  o busque aquí repositorios certificados [Current CoreTrustSeal certified data repositories](https://amt.coretrustseal.org/certificates)

📌 **Más información:** 
- [FAIR Data Principles - GO FAIR](https://www.go-fair.org/fair-principles/)

### 2.2 Accessible (Accesible)
Objetivo: Garantizar el acceso a datos y metadatos de manera clara y transparente.

**Requisitos clave:**
- Uso de protocolos de comunicación abiertos y seguros (**HTTPS, APIs RESTful**).
- Implementación de mecanismos de autenticación y autorización cuando sea necesario.
- **Disponibilidad de metadatos**, incluso si los datos tienen restricciones.
- Metadatos descriptivos que permitan comprender los datos y la accesibilidad para personas con discapacidades.

📌 **Más información:** 
- [FAIR Data - OpenAIRE](https://www.openaire.eu/fair-data)

### 2.3 Interoperable
Objetivo: Facilitar la integración de datos con otros sistemas y garantizar su reutilización automatizada.

**Requisitos clave:**
- Uso de **formatos estándar** como JSON, RDF, XML.
- Uso de **vocabularios controlados y ontologías** (ej. COAR, Schema.org).
- Inclusión de referencias a otros datos con relaciones bien definidas en los metadatos.

📌 **Ejemplo práctico:** 
- [FAIRsharing.org](https://fairsharing.org/)

### 2.4 Reusable (Reutilizable)
Objetivo: Permitir la reutilización de los datos en distintos contextos.

**Requisitos clave:**
- Asignación de **licencias claras** (ej. CC BY, CC0).
- Documentar exhaustivamente la **proveniencia** de los datos: cómo fueron generados, transformados y validados.
- Mantener un **registro de versiones** de los datos y los metadatos asociados, incluyendo fecha de creación, modificación y autor responsable.
- Cumplimiento de estándares y buenas prácticas de la comunidad (ej. diccionario de datos, cuaderno de código).

📌 **Guía complementaria:** 
- [Ten Simple Rules for FAIR Data](https://doi.org/10.1371/journal.pcbi.1007854)

---

## 3. Formatos de Datos y Recomendaciones

| **Tipo de Datos**      | **Formato Recomendado** | **Observaciones** |
|------------------------|------------------------|--------------------|
| **Datos Tabulares**    | CSV, TSV (UTF-8)       | Valores separados por comas o tabulaciones, asegurando el uso de codificación **UTF-8** y la inclusión de encabezados de columna claros. |
| **Datos Jerárquicos**  | JSON, XML              | Uso de esquemas estandarizados para facilitar la interoperabilidad. |
| **Datos Geoespaciales** | GeoJSON, GML          | Incluir información sobre sistemas de coordenadas y proyecciones utilizadas. |
| **Datos Biológicos**   | FASTA, NetCDF          | Seguir las especificaciones y versiones recomendadas por la comunidad científica correspondiente. |
| **Imágenes Científicas** | TIFF, DICOM          | Seguir las especificaciones y versiones recomendadas por la comunidad científica correspondiente (Cuidado con metadatos embebidos) |
| **Otros específicos**  | FITS, NetCDF           | Seguir las especificaciones y versiones recomendadas por la comunidad científica correspondiente. |

### Consideraciones:

#### Formatos Abiertos vs. Formatos Propietarios
- Preferir formatos abiertos y estandarizados para promover la interoperabilidad y la reutilización a largo plazo.
- Evitar formatos propietarios que puedan limitar el acceso y uso de los datos.

#### Compresión y Codificación
- Utilizar codificaciones de caracteres estándar como UTF-8.
- Documentar claramente la codificación utilizada para garantizar la correcta interpretación de los datos.

#### Compresión y Verificación de Integridad
- Documentar los métodos de compresión y cualquier configuración especial utilizada.
- Proporcionar sumas de verificación (por ejemplo, MD5, SHA-256) para permitir la verificación de la integridad de los archivos.

#### Interoperabilidad Semántica
- Cuando sea apropiado, utilizar formatos que faciliten la interoperabilidad semántica, como RDF o JSON-LD.

📌 **Guía complementaria:** 
- [Formatos preferidos para la preservación y publicación en repositorios (Zenodo)](https://doi.org/10.5281/zenodo.8432009)  
  Recomendaciones sobre formatos aceptados y sostenibles para la preservación digital a largo plazo.

- [DANS - Recomendaciones de formatos de archivo](https://dans.knaw.nl/en/file-formats/)  
  Guía del Instituto Holandés DANS con formatos recomendados para el archivo sostenible de datos digitales.

- [UK Data Service - Formatos recomendados](https://ukdataservice.ac.uk/learning-hub/research-data-management/format-your-data/recommended-formats/)  
  Tabla con orientación sobre formatos de archivo recomendados y aceptados por el UK Data Service para compartir, reutilizar y preservar datos.
  
---

## 4. Metadatos y Estándares

Los **metadatos** son descripciones estructuradas que permiten entender, descubrir y reutilizar los datos. Siguen estructuras normalizadas conocidas como **esquemas de metadatos** y, cuando se alinean con vocabularios compartidos, habilitan la interoperabilidad semántica.

#### Importancia de la Metadata

- Describen el contenido, contexto y estructura de los datos de manera detallada y legible por máquinas.
- Facilitan la búsqueda, comprensión, interoperabilidad y reutilización de los datos por parte de los usuarios y los sistemas informáticos.

### Estándares de Metadatos

#### Generales
- **Dublin Core**: Estándar general y ampliamente utilizado para describir una amplia variedad de recursos digitales y físicos. Proporciona un conjunto básico de elementos de metadatos para facilitar la interoperabilidad.
- **DataCite Metadata Schema**: Enfocado en la citación y el registro de datos de investigación, incluyendo identificadores persistentes como DOI. Facilita la identificación, acceso y reutilización de conjuntos de datos.
- **ISO 19115**: Estándar internacional para metadatos de información geoespacial. Define la estructura y contenido de los metadatos para describir datos geoespaciales y servicios relacionados.

#### Ciencias Sociales y Economía
- **DDI (Data Documentation Initiative)**: Estándar para metadatos en ciencias sociales, comportamiento y economía. Facilita la documentación, descubrimiento y compartición de datos en estos campos.
- **SDMX (Statistical Data and Metadata eXchange)**: Estándar para el intercambio de datos y metadatos estadísticos, utilizado por organizaciones estadísticas y bancos centrales.

#### Ciencias de la Salud
- **CDISC (Clinical Data Interchange Standards Consortium)**: Estándares para datos clínicos y de ensayos clínicos, promoviendo la interoperabilidad y eficiencia en la investigación clínica.
- **HL7 (Health Level Seven)**: Conjunto de estándares para el intercambio, integración y recuperación de información electrónica de salud, utilizado en sistemas hospitalarios y clínicos.

#### Ciencias de la Vida y Biología
- **Darwin Core (DwC)**: Estándar para datos de biodiversidad. Proporciona un marco para compartir información sobre especies y registros de organismos, facilitando el intercambio y agregación de datos biológicos.
- **MIAME (Minimum Information About a Microarray Experiment)**: Directrices para la descripción de experimentos de microarrays en genética y genómica, garantizando que los datos sean interpretables y reutilizables.
- **MINSEQE (Minimum Information about a high-throughput Nucleotide Sequencing Experiment)**: Estándar para describir experimentos de secuenciación de alto rendimiento, facilitando la comprensión y reproducción de resultados.
- **EML (Ecological Metadata Language)**: Estándar para metadatos en ecología y ciencias ambientales, promoviendo la gestión y reutilización de datos ecológicos.
- **SBML (Systems Biology Markup Language)**: Lenguaje para representar modelos en biología de sistemas.
- **BioPAX (Biological Pathway Exchange)**: Estándar para el intercambio de datos sobre vías biológicas.

#### Humanidades Digitales y Patrimonio Cultural
- **TEI (Text Encoding Initiative)**: Estándar para la representación de textos en formato digital, ampliamente utilizado en humanidades digitales para codificar y describir recursos textuales.
- **METS (Metadata Encoding and Transmission Standard)**: Esquema para la codificación y transmisión de metadatos de objetos digitales complejos, comúnmente utilizado en bibliotecas y archivos digitales.
- **PREMIS (Preservation Metadata)**: Estándar para metadatos de preservación digital, proporcionando información necesaria para gestionar y mantener objetos digitales a largo plazo.
- **MODS (Metadata Object Description Schema)**: Esquema para descripción bibliográfica, desarrollado por la Biblioteca del Congreso de EE.UU., utilizado en bibliotecas y repositorios digitales.
- **VRA Core**: Estándar para describir obras de arte y artefactos culturales, utilizado en museos, galerías y colecciones de arte.
- **LIDO (Lightweight Information Describing Objects)**: Estándar para la interoperabilidad de datos sobre objetos de museos y colecciones culturales, facilitando el intercambio de información entre instituciones.
- **EAD (Encoded Archival Description)**: Estándar para describir materiales de archivo y manuscritos, utilizado en archivos y bibliotecas para facilitar el acceso a colecciones especiales.
- **ONIX (ONline Information eXchange)**: Estándar para el intercambio de información sobre publicaciones, utilizado en la industria editorial para compartir metadatos sobre libros y otros medios.
- **CIDOC CRM (Conceptual Reference Model)**: Modelo para la interoperabilidad de información cultural y patrimonial.
- **IIIF (International Image Interoperability Framework)**: Estándares para compartir, visualizar y anotar imágenes de alta resolución.

#### Ciencias de la Tierra y Medio Ambiente
- **CF Conventions (Climate and Forecast)**: Estándares para datos climáticos y de pronósticos meteorológicos, utilizados con formatos como NetCDF.
- **INSPIRE Metadata Implementing Rules**: Especificaciones para metadatos en el contexto de la directiva INSPIRE de la Unión Europea, relacionadas con datos espaciales ambientales.
- **CSDGM (Content Standard for Digital Geospatial Metadata)**: Estándar desarrollado por el FGDC (Federal Geographic Data Committee) de EE.UU. para metadatos geoespaciales, promoviendo una documentación consistente de datos geoespaciales.

#### Ingeniería y Manufactura
- **STEP (Standard for the Exchange of Product model data)**: Estándar para el intercambio de datos de productos industriales y de ingeniería.

#### Educación
- **LOM (Learning Object Metadata)**: Estándar para describir objetos de aprendizaje y recursos educativos.

#### Servicios Web y Datos Abiertos
- **DCAT (Data Catalog Vocabulary)**: Vocabulario para describir catálogos de datos publicados en la web, facilitando la interoperabilidad entre portales de datos.
- **OAI-PMH (Open Archives Initiative Protocol for Metadata Harvesting)**: Protocolo que facilita la recolección de metadatos desde repositorios digitales, permitiendo la interoperabilidad y el descubrimiento de recursos.

### Uso de Vocabularios Controlados y Ontologías
- Emplear vocabularios y ontologías estandarizados como **Schema.org**, **FOAF**, **DCMI Terms**, que mejoran la interoperabilidad semántica y la comprensión común de los términos utilizados.
- Asegurar que estos vocabularios y ontologías sigan los principios **FAIR**.

### Elementos Clave de los Metadatos
- **Título**
- **Autores/Colaboradores**: Incluir identificadores persistentes como **ORCID** para autores y **ROR** para organizaciones.
- **Resumen/Descripción**
- **Palabras Clave**: Utilizar vocabularios controlados para facilitar la búsqueda y recuperación.
- **Fecha de Publicación**
- **Fecha de Creación y Modificación**
- **Licencia**: Especificar una licencia clara y estándar (ej. **CC BY**, **CC0**) para definir las condiciones de reutilización.
- **Identificador Persistente**: Asignar un **DOI** u otro identificador persistente al conjunto de datos.
- **Proveniencia**: Proporcionar información sobre el origen de los datos, métodos de recolección y cualquier transformación realizada.
- **Métodos**: Detalles sobre cómo se recopilaron, procesaron y analizaron los datos.
- **Estándares y Formatos Utilizados**: Especificar los estándares y formatos utilizados en los datos y metadatos.
- **Información de Contacto**: Datos de la persona responsable o custodio de los datos para soporte o consultas adicionales.

### **Estructura de metadatos procesables por máquinas**

### **Data Stewardship Wizard – maDMPs**
- **Descripción**: Extensión de la herramienta DSW que permite generar planes de gestión de datos legibles por máquinas (maDMPs), facilitando su integración con flujos institucionales, APIs y sistemas de monitoreo FAIR.
- **Enlace**: [https://ds-wizard.org/machine-actionability](https://ds-wizard.org/machine-actionability)

### **Schema.org**
- **Descripción**: Vocabulario ampliamente adoptado para describir objetos digitales (datasets, software, publicaciones) en formato legible por máquinas, compatible con JSON-LD y motores de búsqueda académicos.
- **Enlace**: [https://schema.org/](https://schema.org/)

### **CodeMeta**
- **Descripción**: Esquema de metadatos para describir software de investigación, interoperable con Schema.org y diseñado para facilitar la integración con sistemas abiertos. Utiliza archivos `codemeta.json`.
- **Enlace**: [https://codemeta.github.io/](https://codemeta.github.io/)

### **DCAT – Data Catalog Vocabulary**
- **Descripción**: Vocabulario del W3C para describir catálogos de datos abiertos y sus recursos asociados, usado por portales de datos científicos e institucionales.
- **Enlace**: [https://www.w3.org/TR/vocab-dcat-3/](https://www.w3.org/TR/vocab-dcat-3/)

### **FAIRsharing**
- **Descripción**: Repositorio curado de estándares, metadatos, políticas y repositorios que permite identificar estructuras interoperables por disciplina o tipo de producto digital.
- **Enlace**: [https://fairsharing.org/](https://fairsharing.org/)

📌 **Referencia útil:** 
- [FAIR Metadata Recommendations](https://doi.org/10.1371/journal.pcbi.1009041)



---

## 5. Licencias y Derechos de Uso

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

 [Software Licenses in Plain English](https://www.tldrlegal.com/)
 
📌 **Más sobre licencias:** 
- [Recopilación de licencias según tipo de objeto digital](https://doi.org/10.5281/zenodo.8222781)


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
- Incluir archivos de licencia (ejemplo: **LICENSE.txt**) en los repositorios de código.

##### **Implicaciones en Interoperabilidad y Reutilización**
- Licencias más abiertas y permisivas facilitan una mayor interoperabilidad y reutilización.
- Licencias más restrictivas pueden limitar la capacidad de terceros para reutilizar o integrar los datos y código en otros proyectos.

##### **Consultas Legales**
- Si hay dudas sobre qué licencia elegir, considerar consultar con un experto legal para garantizar cumplimiento y adecuación.

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


📌 **Herramienta para elegir licencias:** 
- [Choose a License](https://choosealicense.com/).

📌 **Lista de licencias y sus identificadores:** 
- [SPDX License List](https://spdx.org/licenses/)

---

## 6. Evaluación FAIR y Herramientas

Algunas herramientas útiles para evaluar la adopción FAIR incluyen:

### **FAIR-Aware**
- **Descripción**: FAIR-Aware es una plataforma educativa desarrollada por **DANS (Data Archiving and Networked Services)** que ayuda a investigadores y gestores de datos a comprender mejor los principios **FAIR** y cómo aplicarlos a sus datos. 
- Proporciona una autoevaluación guiada que sensibiliza sobre los aspectos clave de FAIR.  
- **Enlace**: [FAIR-Aware](https://fairaware.dans.knaw.nl/)

### **FAIR Evaluator**
- **Descripción**: Herramienta en línea que permite a los usuarios evaluar el cumplimiento de sus datos con los principios **FAIR** a través de una serie de preguntas y métricas. 
- Proporciona comentarios y recomendaciones para mejorar la **FAIRness** de los datos.
- **Enlace**: [FAIR Evaluator](https://fairsharing.org/FAIR-Evaluator)

### **How FAIR is**
- **Descripción**: Herramienta de línea de commando que permite analisar el cumplimiento del software con las recomendaciones de [fair-software.eu](https://fair-software.eu/). 
- Las recomendaciones de no estan directamente ligadas a los principios **FAIR4RS**, pero no les contradicen tienen el mismo objetivo.
- **Enlace**: [howFAIRis](https://github.com/fair-software/howfairis)

### **F-UJI**
- **Descripción**: Herramienta automatica para la evaluación de **FAIRness**.
- La evaluación de F-UJI assessment esta basada en 16 de las 17 metricas desarolladas en el projecto [FAIRsFAIR](https://www.fairsfair.eu/). 
- **Enlace**: [F-UJI](https://catalogue.fair-impact.eu/resources/f-uji)

### ** Auto-evaluacion de FAIR software **
- **Descripción**: Una lista interactive de verificación con preguntas sobre el **FAIRness** del software de investigación.
- Esta lista genera una insignia (badge) que los propietarios de proyectos pueden incluir en su README para comunicar el estado del proyecto a los visitantes.
- **Enlace**: [FAIR software check-list](https://fairsoftwarechecklist.net/v0.2/)

### **FAIRsharing**
- **Descripción**: Recurso curado que proporciona información sobre estándares, repositorios y políticas que apoyan la implementación de los principios **FAIR**.
- **Enlace**: [FAIRsharing](https://fairsharing.org/)

### **FAIR Data Maturity Model**
- **Descripción**: Modelo desarrollado por el **Grupo de Trabajo ISO/TC 276** para medir el grado de "FAIRness" de los datos. 
- Proporciona un conjunto de indicadores y métricas que permiten evaluar de manera sistemática el cumplimiento de los principios **FAIR**.
- **Enlace**: [FAIR Data Maturity Model](https://zenodo.org/records/3909563)

### **FAIR Cookbook**
- **Descripción**: Colección de recetas prácticas que guían a los usuarios a través de los pasos necesarios para implementar los principios **FAIR** en la gestión y publicación de datos.
- **Enlace**: [FAIR Cookbook](https://faircookbook.elixir-europe.org/)

### **FAIRification Process**
- **Descripción**: Guía detallada que describe el proceso de "FAIRificación" de los datos, incluyendo pasos prácticos y consideraciones técnicas.
- **Enlace**: [FAIRification Process](https://www.go-fair.org/fair-principles/fairification-process/)

### ***Otros Recursos Relevantes***

### **DMT Clearinghouse**
- **Descripción**: Repositorio curado de materiales educativos, herramientas y recursos sobre gestión de datos. Permite buscar guías, plantillas y presentaciones útiles para investigadores y data stewards.
- **Enlace**: [https://dmtclearinghouse.esipfed.org/search](https://dmtclearinghouse.esipfed.org/search)

### **Ethical Data Initiative**
- **Descripción**: Iniciativa global centrada en los aspectos éticos del uso, gestión y gobernanza de datos. Promueve principios de equidad, justicia de datos y soberanía digital.
- **Enlace**: [https://ethicaldatainitiative.org](https://ethicaldatainitiative.org)

### **The Turing Way**
- **Descripción**: Proyecto comunitario que ofrece una guía integral para la ciencia de datos reproducible, colaborativa y ética. Incluye capítulos sobre planes de gestión de datos y software, licencias, citación, liderazgo, diversidad y colaboración abierta. Todo el contenido está disponible bajo licencia CC BY e incluye ilustraciones reutilizables.
- **Enlace**: [https://the-turing-way.netlify.app/](https://the-turing-way.netlify.app/)


---

## 7. Tipos de Investigación y Requisitos FAIR

### 7.1 Investigación Observacional
##### **Requisitos:**
- **Documentar Instrumentos y Métodos**:  
  - Metadatos de contexto
  - Describir en detalle los instrumentos utilizados y los métodos de recopilación de datos.  
  - Usar estándares y protocolos reconocidos en el dominio (ej. **Darwin Core** para biodiversidad, **ISO 19115** para metadatos geoespaciales).
- **Registrar Coordenadas y Tiempo**:  
  - Proporcionar información precisa sobre la ubicación geográfica (coordenadas GPS) y marcas de tiempo, utilizando formatos estandarizados como **ISO 8601** para fechas y horas.
- **Preservar Metadatos Contextuales**:  
  - Incluir metadatos sobre condiciones ambientales, contexto del estudio y factores que puedan influir en los datos.
- **Consideraciones Éticas y Legales**:  
  - Obtener consentimiento informado cuando sea aplicable.  
  - Cumplir con las regulaciones de protección de datos.

### 7.2 Investigación Experimental
##### **Requisitos:**
- **Documentar Condiciones Experimentales**:
  - Proveniencia y estándares
  - Describir el diseño experimental, procedimientos y protocolos utilizados.  
  - Incluir información sobre materiales, reactivos y sujetos experimentales.
- **Registrar Calibraciones y Configuraciones**:  
  - Documentar calibraciones de equipos, configuraciones de instrumentos y parámetros relevantes.
- **Preservar Datos Brutos y Procesados**:  
  - Almacenar y compartir tanto datos en bruto como procesados, junto con información sobre métodos de procesamiento y análisis.
- **Cumplimiento de Estándares del Dominio**:  
  - Usar estándares como **MIAME** para microarrays, **MIBBI** para investigaciones biológicas y biomédicas.
- **Consideraciones Éticas**:  
  - Obtener aprobaciones éticas y cumplir con las regulaciones aplicables.

### 7.3 Investigación Computacional
##### **Requisitos:**
- **Documentar Código y Dependencias**:
  - Publicación de código y entorno   
  - Proporcionar acceso al código fuente, scripts y bibliotecas utilizadas, con comentarios y documentación adecuada.  
  - Usar sistemas de control de versiones como **Git**.
- **Preservar Entornos de Ejecución**:  
  - Compartir información sobre el entorno de ejecución (sistemas operativos, versiones de software, contenedores como **Docker** o **Singularity**).
  - Considerar el uso de contenedores o máquinas virtuales para facilitar la reproducibilidad.
- **Registrar Parámetros y Seeds**:  
  - Documentar todos los parámetros de entrada, configuraciones y seeds aleatorios utilizados en simulaciones o modelos.
- **Publicación y Citación del Código**:  
  - Asignar un **DOI** al código y usar repositorios como **GitHub**, **GitLab** o **Zenodo**.
- **Licencias de Código**:  
  - Aplicar licencias apropiadas como **Apache 2.0** o **GPL** para código y software.

### 7.4 Investigación Clínica y Social
##### **Requisitos:**
- **Cumplimiento con Regulaciones de Protección de Datos**:
  - Licencias, anonimización  
  - Cumplir con regulaciones como **GDPR** (Europa), **LGPD** (Brasil), **HIPAA** (EE.UU.), u otras aplicables.
- **Anonimización y Seudonimización**:  
  - Aplicar técnicas para proteger la identidad de los participantes.  
  - Evaluar riesgos de re-identificación y aplicar medidas adecuadas.
- **Consentimiento Informado**:  
  - Obtener consentimiento explícito para la recopilación, uso y compartición de datos.
- **Aprobaciones Éticas y Regulatorias**:  
  - Obtener aprobaciones de comités de ética y cumplir con requisitos institucionales y legales.
- **Acceso Restringido y Controlado**:  
  - Implementar mecanismos para controlar el acceso a datos sensibles.

---

## 8. Consideraciones éticas, lingüísticas y culturales

Los principios **FAIR** no consideran explícitamente los derechos de comunidades, por lo que es crucial complementarlos con los principios **CARE** (Colectivo, Autoridad, Responsabilidad, Ética), desarrollados por GIDA para guiar el uso justo y respetuoso de datos sobre pueblos indígenas.

📌 [Más información sobre CARE](https://www.gida-global.org/care)


### Accesibilidad lingüística

- La mayoría de las herramientas, guías y vocabularios están disponibles solo en inglés.
- Promover traducciones, glosarios en español y capacitación multilingüe es un paso esencial hacia la equidad en ciencia abierta.

### Contextos locales y epistemologías diversas

- La definición de metadatos, estándares y licencias debe considerar normas culturales, marcos legales nacionales y derechos colectivos.
- El principio de **reutilización responsable** implica no solo lo técnico, sino también lo ético y contextual.

📌 **Recurso inspirador**:
- [Ethical Data Initiative](https://ethicaldatainitiative.org) – reflexiones sobre justicia de datos, soberanía digital y derechos de comunidades.

> ⚠️ Se recomienda no aplicar criterios FAIR de forma mecánica o exclusivamente técnica, sino incorporar principios de **justicia epistémica**, accesibilidad cultural y pluralismo de saberes.

---

## 9. Anexos

### 9.1 Anexo A: Checklist de Evaluación FAIR

### **Findable (Encontrable)**

- **Identificadores Persistentes:**  
  - [ ] ¿Los datos tienen un identificador único y persistente (por ejemplo, DOI, Handle)?

- **Metadatos Ricos:**  
  - [ ] ¿Los metadatos proporcionan una descripción detallada del conjunto de datos e incluyen el identificador persistente de los datos descritos?

- **Indexación en Repositorios:**  
  - [ ] ¿Los datos y metadatos están almacenados en repositorios especializados o catálogos accesibles por usuarios y sistemas?

- **Estructura de Metadatos Estándar:**  
  - [ ] ¿Se utilizan estándares de metadatos reconocidos y vocabularios controlados (ej. Dublin Core, DataCite, Schema.org)?

- **Palabras Clave y Etiquetas:**  
  - [ ] ¿Se incluyen palabras clave relevantes utilizando vocabularios controlados para facilitar la búsqueda?

---

### **Accessible (Accesible)**

- **Protocolos de Acceso Estándar:**  
  - [ ] ¿Los datos son accesibles a través de protocolos abiertos, gratuitos y universalmente implementables (ej. HTTPS, APIs RESTful)?

- **Condiciones de Acceso Claras:**  
  - [ ] ¿Las condiciones y procedimientos para acceder a los datos están claramente especificados, incluyendo procesos de autenticación si son necesarios?

- **Autenticación y Autorización:**  
  - [ ] Si es necesario, ¿existen mecanismos de autenticación y autorización bien definidos, estandarizados y seguros?

- **Persistencia de Metadatos:**  
  - [ ] ¿Los metadatos siguen siendo accesibles sin restricciones, incluso si los datos ya no están disponibles?

---

### **Interoperable (Interoperable)**

- **Formatos de Datos Estándar:**  
  - [ ] ¿Se utilizan formatos de datos abiertos y ampliamente aceptados (ej. RDF, OWL, JSON-LD)?

- **Vocabularios Controlados y Ontologías:**  
  - [ ] ¿Se emplean vocabularios estandarizados y ontologías compartidas que siguen los principios FAIR?

- **Referencias a Otros Recursos:**  
  - [ ] ¿Los datos y metadatos incluyen referencias claras a otros recursos relacionados especificando la naturaleza de la relación?

- **Uso de Estándares de Codificación:**  
  - [ ] ¿Se aplican estándares de codificación consistentes (ej. UTF-8) y está la codificación documentada claramente?

---

### **Reusable (Reutilizable)**

- **Licencias Claras y Abiertas:**  
  - [ ] ¿Se aplican licencias abiertas y bien definidas (ej. CC0, CC BY)?

- **Información de Origen:**  
  - [ ] ¿Se proporciona información detallada sobre el origen e historial de los datos?

- **Descripción Detallada:**  
  - [ ] ¿Los metadatos incluyen suficiente contexto para comprender y reutilizar los datos?

- **Cumplimiento de Estándares de la Comunidad:**  
  - [ ] ¿Se siguen estándares y convenciones de la comunidad en el dominio de los datos?

- **Calidad y Validación de Datos:**  
  - [ ] ¿Se han realizado controles de calidad y están documentados los procedimientos de validación?
  
---

### 9.2 Anexo B: Ejemplo de Metadatos Estructurados

A continuación se muestra un ejemplo de metadatos estructurados según el estándar **Dublin Core** para un conjunto de datos hipotético.

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

### 9.3 Anexo C: Datos mínimos para un Plan de Gestión de Datos (DMP)

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

---

📌 Notas Finales
Un **DMP bien estructurado** es clave para asegurar la **transparencia, reproducibilidad e interoperabilidad** de los datos científicos. Se recomienda revisar periódicamente este plan para adaptarlo a nuevas necesidades o requisitos institucionales.

---

### 9.4 Anexo D: Datos mínimos para un Plan de Gestión de Software (SMP)

El **Plan de Gestión de Software (PGS)** describe cómo se desarrollará, documentará y compartirá el software durante un proyecto de investigación. Su objetivo es garantizar que el software sea **mantenido, utilizable y accesible a largo plazo**, apoyando la trazabilidad de su desarrollo y facilitando su reutilización, de acuerdo con los principios FAIR4RS (Findable, Accessible, Interoperable, Reusable for Research Software).

## Comparación entre FAIR y FAIR4RS

| Principio | FAIR (datos) | FAIR4RS (software) |
|-----------|--------------|--------------------|
| **Findable** | Los datos deben tener un identificador persistente y estar indexados en un repositorio. | El software debe tener un identificador, versión persistente y estar registrable (ej. en Zenodo, Software Heritage). |
| **Accessible** | Los metadatos y datos deben estar disponibles con protocolos abiertos. | El código fuente, documentación y ejecutables deben estar accesibles (repositorio abierto, instrucciones de instalación). |
| **Interoperable** | Uso de vocabularios controlados y formatos estándar. | Uso de lenguajes estándar, interoperabilidad entre módulos, y metadatos de ejecución. |
| **Reusable** | Licencias claras, documentación adecuada y proveniencia completa. | Licencia de software compatible, documentación, dependencias y entorno reproducible. |

📌 **Más información:**
- Martínez-Ortiz, C., Bakker, P., & Koning, H. (2022). *Practical guide to Software Management Plans*. Netherlands eScience Center. [https://doi.org/10.5281/zenodo.6245751](https://doi.org/10.5281/zenodo.6245751)

A continuación, se describen los elementos mínimos recomendados que debe contener un PGS:

### 1. Información general del software
- Nombre del software y del proyecto asociado
- Instituciones y responsables (desarrolladores, mantenedores)
- Periodo de desarrollo y/o mantenimiento
- Recursos necesarios (infraestructura, personal)

### 2. Propósito y alcance
- Objetivo científico del software
- Problema que resuelve
- Usuarios esperados y contexto de aplicación

### 3. Repositorio y control de versiones
- URL del repositorio (por ejemplo, GitHub, GitLab)
- Uso de control de versiones (por ejemplo, Git)
- Estrategia de *releases* y asignación de DOI (por ejemplo, Zenodo)
- Historial de cambios

### 4. Documentación
- Manuales de usuario
- Guías de instalación y despliegue
- Documentación para desarrolladores
- Herramientas de documentación (Markdown, ReadTheDocs, etc.)

### 5. Calidad del software
- Pruebas (unitarias, integración, regresión)
- Revisión de código (*code review*)
- Uso de herramientas de calidad (linters, CI/CD)
- Gestión de *issues* y errores

### 6. Licenciamiento y aspectos legales
- Licencia elegida (MIT, GPL, Apache, etc.)
- Consideraciones de copyright y atribución
- Restricciones legales o éticas (por ejemplo, uso dual, privacidad)

### 7. Publicación, citación y visibilidad
- Plataforma de publicación (Zenodo, Software Heritage, repositorio institucional)
- Especificación de citación (CITATION.cff, codemeta.json)
- Registro en catálogos o directorios de software científico

### 8. Preservación y sostenibilidad
- Responsable(s) del mantenimiento
- Plan de archivado a largo plazo
- Compatibilidad futura (contenedores, gestión de dependencias)
- Nivel de soporte tras el proyecto

### 9. Soporte y gobernanza
- Canales de contacto o soporte para usuarios
- Roles y responsabilidades del equipo
- Recursos estimados para sostenibilidad

---

📌 **Recursos y plantillas útiles**

### **Principios y lineamientos FAIR para software**

### **FAIR4RS Principles (RDA, FORCE11, ReSA)**
- **Descripción**: Principios FAIR adaptados específicamente para software de investigación, desarrollados por comunidades como RDA, FORCE11 y ReSA. Sirven como marco de referencia para asegurar la trazabilidad, accesibilidad y reutilización del software en contextos científicos.
- **Enlace**: [https://doi.org/10.15497/RDA00068](https://doi.org/10.15497/RDA00068)

### **SMP Checklist – Software Sustainability Institute**
- **Descripción**: Lista de verificación para elaborar planes de gestión de software sostenibles y de calidad. Incluye preguntas clave sobre documentación, licencias, preservación y gobernanza.
- **Enlace**: [https://software.ac.uk/resources/guides/software-management-plans](https://software.ac.uk/resources/guides/software-management-plans)

### **Plantilla de PGS – Wageningen University & Research**
- **Descripción**: Ejemplo práctico de plan de gestión de software (PGS), alineado con los principios FAIR y usado como referencia por instituciones europeas.
- **Enlace**: [https://zenodo.org/record/10696023](https://zenodo.org/record/10696023)

---

### **Herramientas para elaborar y gestionar PGS**

### **Data Stewardship Wizard (DSW)**
- **Descripción**: Herramienta interactiva para construir planes de gestión de datos y software, integrando vocabularios controlados y buenas prácticas FAIR desde etapas tempranas del proyecto.
- **Enlace**: [https://ds-wizard.org/](https://ds-wizard.org/)

### **Machine Actionable DMPs – DSW**
- **Descripción**: Extensión del DSW para generar DMPs legibles por máquinas (maDMPs), facilitando su integración en flujos automatizados de gestión de datos.
- **Enlace**: [https://ds-wizard.org/machine-actionability](https://ds-wizard.org/machine-actionability)

### **RDA Workshop on Machine Actionable DMPs**
- **Descripción**: Taller organizado por la RDA y DCC para explorar el desarrollo, adopción y uso práctico de planes de gestión automatizados.
- **Enlace**: [https://www.dcc.ac.uk/events/RDAcolocated_machine_actionable_DMPs](https://www.dcc.ac.uk/events/RDAcolocated_machine_actionable_DMPs)

### **DMPonline**
- **Descripción**: Plataforma ampliamente utilizada para elaborar DMPs y SMPs personalizados según el tipo de proyecto y requerimientos de financiadores.
- **Enlace**: [https://dmponline.dcc.ac.uk/](https://dmponline.dcc.ac.uk/)

### **RDMO – Research Data Management Organizer**
- **Descripción**: Herramienta flexible y modular para planificar la gestión de datos y software durante todo el ciclo de vida del proyecto.
- **Enlace**: [https://rdmorganiser.github.io/](https://rdmorganiser.github.io/)

---

### **Preservación, licencias y metadatos**

### **Software Heritage**
- **Descripción**: Archivo universal de software impulsado por INRIA, que permite preservar, rastrear y citar código fuente mediante identificadores persistentes (SWHID).
- **Enlace**: [https://www.softwareheritage.org/](https://www.softwareheritage.org/)

### **Choose a License – GitHub**
- **Descripción**: Asistente que facilita la elección de licencias de software, comparando permisos, restricciones y compatibilidades.
- **Enlace**: [https://choosealicense.com/](https://choosealicense.com/)

### **Codemeta**
- **Descripción**: Esquema estandarizado para describir software con metadatos interoperables, facilitando su descubrimiento, citación y reutilización en repositorios.
- **Enlace**: [https://codemeta.github.io/](https://codemeta.github.io/)

---

### **Herramientas para gestionar software científico**

### **Tutorial GloBI (en español)**
- **Descripción**: Guía paso a paso del proyecto Global Biotic Interactions (GloBI) sobre cómo documentar, versionar y publicar software científico usando GitHub y Zenodo. Incluye buenas prácticas para la asignación de DOIs y licencias.
- **Enlace**: [https://www.globalbioticinteractions.org/es/tutorial.html](https://www.globalbioticinteractions.org/es/tutorial.html)


---
