# FAIR: Guía de Referencia

## Índice
1. [Introducción](#ntroduccion)
2. [Principios FAIR](#principios-fair)
   - [Findable (Encontrable)](#findable-encontrable)
   - [Accessible (Accesible)](#accessible-accesible)
   - [Interoperable](#interoperable)
   - [Reusable (Reutilizable)](#reusable-reutilizable)
3. [Formatos de Datos y Recomendaciones](#formatos-de-datos-y-recomendaciones)
4. [Metadatos y Estándares](#metadatos-y-estandares)
5. [Licencias y Derechos de Uso](#licencias-y-derechos-de-uso)
6. [Evaluación FAIR y Herramientas](#evaluacion-fair-y-herramientas)
7. [Tipos de Investigación y Requisitos FAIR](#tipos-de-investigacion-y-requisitos-fair)
   - [Investigación Observacional](#investigacion-observacional)
   - [Investigación Experimental](#investigacion-experimental)
   - [Investigación Computacional](#investigacion-computacional)
8. [Colaboradores](#colaboradores)
9. [Anexos](#anexos)
   - [Anexo A: Checklist de Evaluación FAIR](#anexo-a-checklist-de-evaluacion-fair)
   - [Anexo B: Ejemplo de Metadatos Estructurados](#anexo-b-ejemplo-de-metadatos-estructurados)
   - [Anexo C: Datos mínimos para un Plan de Gestión de Datos](#anexo-c-datos-minimos-para-un-plan-de-gestion-de-datos)

**Este documento está disponible bajo la licencia CC BY 4.0** y puede ser actualizado con nuevas colaboraciones.

## Colaboradores

Esta guía ha sido elaborada con el apoyo de diversas personas y organizaciones comprometidas con la promoción de los principios FAIR. Se invita a otros colaboradores a contribuir con mejoras, actualizaciones y ejemplos adicionales.

**Colaboradores:**
- Ricardo Hartley Belmar @ricnadamas [ORCID:0000-0001-5058-9309](https://orcid.org/my-orcid?orcid=0000-0001-5058-9309)
- Isabel Abedrapo @yolaisa [ORCID:0000-0001-9990-0436](https://orcid.org/0000-0001-9990-0436)

---

## Introduccion

Esta guía proporciona un marco práctico para la implementación de los principios **FAIR** en la gestión de datos de investigación y otras áreas que requieren estructuración y accesibilidad de la información. No está dirigida únicamente a investigadores, sino también a bibliotecarios, gestores de datos, responsables de políticas científicas, desarrolladores de infraestructuras y cualquier persona interesada en la gestión eficiente de datos digitales.

Los principios FAIR buscan garantizar que los datos sean **Encontrables (Findable), Accesibles (Accessible), Interoperables (Interoperable) y Reutilizables (Reusable)**. Implementar estos principios permite mejorar la visibilidad y el impacto de los datos, optimizar la inversión en su generación y promover la colaboración científica y tecnológica.

Además de describir los principios FAIR, esta guía proporciona información sobre:
- **Estándares de metadatos** recomendados.
- **Formatos de datos** y su interoperabilidad.
- **Licencias y derechos de uso** para facilitar la reutilización.
- **Herramientas y metodologías** para evaluar la adopción de FAIR.
- **Ejemplos y recursos prácticos** para la implementación en diferentes contextos.

Para facilitar su aplicación, se incluyen listas de verificación y directrices para distintos tipos de proyectos.

---

## Principios FAIR 

📌 **Más información:**

[Principios FAIR (material para taller). Autores Meyers, N., Escapil-Inchauspé, P., Egaña Aranguren, M., & Hartley Belmar, Ricardo](https://doi.org/10.6075/J0TM7BG5)

[Traducción del Documento guía para el Plan de Gestión de Datos FAIR en Organizaciones e Instituciones. Autores Kirkpatrick, C. R., Cragin, M. H., & Meyers, N. (2024) (Translators Hartley Belmar, Ricardo; Meyers, Natalie)](https://doi.org/10.6075/J0ZC836W)

### Findable (Encontrable)
Objetivo: Asegurar que los datos y metadatos puedan ser descubiertos fácilmente.

**Requisitos clave:**
- Uso de **identificadores persistentes (PID)** como DOI o Handle.
- Almacenamiento de metadatos los identificadores persistentes.
- Metadatos ricos que describan los datos de manera clara y estructurada.
- Indexación en **repositorios especializados** como Zenodo, DataCite o re3data.

📌 **Más información:** [FAIR Data Principles - GO FAIR](https://www.go-fair.org/fair-principles/)

### Accessible (Accesible)
Objetivo: Garantizar el acceso a datos y metadatos de manera clara y transparente.

**Requisitos clave:**
- Uso de protocolos de comunicación abiertos y seguros (**HTTPS, APIs RESTful**).
- Implementación de mecanismos de autenticación y autorización cuando sea necesario.
- **Disponibilidad de metadatos**, incluso si los datos tienen restricciones.
- Metadatos descriptivos que permitan comprender los datos y la accesibilidad para personas con discapacidades.

📌 **Más información:** [FAIR Data - OpenAIRE](https://www.openaire.eu/fair-data)

### Interoperable
Objetivo: Facilitar la integración de datos con otros sistemas y garantizar su reutilización automatizada.

**Requisitos clave:**
- Uso de **formatos estándar** como JSON, RDF, XML.
- Uso de **vocabularios controlados y ontologías** (ej. COAR, Schema.org).
- Inclusión de referencias a otros datos con relaciones bien definidas en los metadatos.

📌 **Ejemplo práctico:** [FAIRsharing.org](https://fairsharing.org/)

### Reusable (Reutilizable)
Objetivo: Permitir la reutilización de los datos en distintos contextos.

**Requisitos clave:**
- Asignación de **licencias claras** (ej. CC BY, CC0).
- Metadatos detallados con información metodológica y de procedencia.
- Cumplimiento de estándares y buenas prácticas de la comunidad (ej. diccionario de datos, cuaderno de código).

📌 **Guía complementaria:** [Ten Simple Rules for FAIR Data](https://doi.org/10.1371/journal.pcbi.1007854)

---

## Formatos de Datos y Recomendaciones

| Tipo de Datos | Formato Recomendado |
|--------------|-------------------|
| Datos Tabulares | CSV, TSV (UTF-8) |
| Datos Jerárquicos | JSON, XML |
| Datos Geoespaciales | GeoJSON, GML |
| Datos Biológicos | FASTA, NetCDF |
| Imágenes Científicas | TIFF, DICOM |

---

## Metadatos y Estándares

Algunos estándares de metadatos recomendados incluyen:

- **[Dublin Core](https://www.dublincore.org/):** General y ampliamente adoptado.
- **[DataCite Metadata Schema](https://schema.datacite.org/):** Para la citación de datos de investigación.
- **[ISO 19115](https://www.iso.org/standard/26020.html):** Metadatos geoespaciales.
- **[Darwin Core](https://dwc.tdwg.org/):** Biodiversidad.

📌 **Referencia útil:** [FAIR Metadata Recommendations](https://doi.org/10.1371/journal.pcbi.1009041)

---

## Licencias y Derechos de Uso

Las licencias abiertas permiten la reutilización de datos:

| Tipo de Licencia | Aplicación |
|-----------------|------------|
| **CC0** | Dominio público, sin restricciones. |
| **CC BY** | Uso permitido con atribución. |
| **ODbL** | Para bases de datos, con condiciones de atribución y compartición. |

📌 **Herramienta para elegir licencias:** [Choose a License](https://choosealicense.com/)

---

## Evaluación FAIR y Herramientas

Algunas herramientas útiles para evaluar la adopción FAIR incluyen:

- **[FAIR-Aware](https://fairaware.dans.knaw.nl/)** – Evaluación de principios FAIR.
- **[FAIR Evaluator](https://fairsharing.org/FAIR-Evaluator)** – Evaluación automática de datasets.
- **[FAIR Data Maturity Model](https://zenodo.org/record/3909563)** – Modelo de medición de FAIR.

---

## Tipos de Investigación y Requisitos FAIR

### Investigación Observacional
- Documentación detallada de instrumentos y métodos.
- Geolocalización y timestamps en formatos estándar.

### Investigación Experimental
- Registro de configuraciones y calibraciones de equipos.
- Publicación de datos brutos y procesados.

### Investigación Computacional
- Uso de control de versiones (Git).
- Publicación de código y dependencias en repositorios abiertos.

📌 **Ejemplo:** [FAIR for Research Software](https://fair4rs.org/)

---

# Anexos

## Anexo A: Checklist de Evaluación FAIR

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

## Anexo B: Ejemplo de Metadatos Estructurados

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

## Anexo C: Datos mínimos para un Plan de Gestión de Datos (DMP)

Un **Plan de Gestión de Datos (DMP)** es un documento esencial que describe cómo se generarán, documentarán, almacenarán, compartirán y preservarán los datos de investigación. A continuación, se presentan los elementos mínimos que debe contener un DMP.

---

### 1. Información del Proyecto
   - [ ] **Título del proyecto:** Nombre oficial del estudio o iniciativa.
   - [ ] **Investigadores responsables:** Nombres y afiliaciones de los principales responsables del proyecto.
   - [ ] **Fuentes de financiamiento:** Instituciones, agencias o programas que financian el proyecto.

---

### 2. Descripción de los Datos
   - [ ] **Tipos de datos:** ¿Qué tipo de datos se generarán o recopilarán? (Ej.: encuestas, imágenes, datos tabulares, secuencias genómicas, etc.)
   - [ ] **Formatos de datos:** Formatos recomendados para garantizar la interoperabilidad y accesibilidad a largo plazo (Ej.: CSV, JSON, XML, NetCDF, FITS).
   - [ ] **Volumen estimado de datos:** Aproximación del tamaño de los datos generados (Ej.: 100 GB, 1 TB, etc.).
   - [ ] **Metodología de recolección:** ¿Cómo se generarán los datos? (Ej.: sensores, simulaciones, encuestas, bases de datos existentes).

---

### 3. Documentación y Metadatos
   - [ ] **Estándares de metadatos:** Especificar qué estándares se utilizarán para describir los datos (Ej.: Dublin Core, DataCite, ISO 19115).
   - [ ] **Herramientas de documentación:** Métodos y plataformas usadas para generar documentación (Ej.: README.txt, Data Dictionaries, esquemas JSON-LD).
   - [ ] **Vocabularios controlados y ontologías:** Identificar si se utilizarán vocabularios estandarizados (Ej.: FOAF, Schema.org, Darwin Core).

---

### 4. Almacenamiento y Seguridad
   - [ ] **Ubicación de los datos durante el proyecto:** ¿Dónde se almacenarán los datos en curso? (Ej.: servidores locales, nube, repositorios de universidades).
   - [ ] **Estrategia de respaldo:** Métodos de respaldo y periodicidad (Ej.: copias diarias/semanales en almacenamiento redundante).
   - [ ] **Medidas de seguridad:** ¿Qué protocolos se implementarán para garantizar la seguridad de los datos? (Ej.: encriptación, acceso restringido).

---

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

## 📌 Notas Finales
Un **DMP bien estructurado** es clave para asegurar la **transparencia, reproducibilidad e interoperabilidad** de los datos científicos. Se recomienda revisar periódicamente este plan para adaptarlo a nuevas necesidades o requisitos institucionales.

