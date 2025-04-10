# Research Object Traceability Framework (draft-scheme)

## Overview

This repository contains a mind map of digital artefact traceability. The mind map covers various aspects of managing, identifying, and transferring digital objects in research.

## Contributors

This guide was developed with the support of various individuals and organizations committed to promoting the FAIR principles. Additional collaborators are welcome to contribute improvements, updates, and further examples.

- Ricardo Hartley Belmar @ricnadamas [ORCID:0000-0001-5058-9309](https://orcid.org/my-orcid?orcid=0000-0001-5058-9309)

**This document is available under the CC BY 4.0 license** and may be updated with new contributions.

## Detailed Sections

### Objects Use

- **Rights Code**
  - Codes specifying the usage rights and permissions for data objects.
- **Embargo Period**
  - Period during which access to data is restricted.
- **Raw Data**
  - Unprocessed primary data collected from research activities.
- **Processed Data**
  - Data that has been cleaned, transformed, or analyzed.
- **Results**
  - Final outcomes and conclusions derived from the data.

### Project

- **Project ID**
  - [RAiD](https://raid.org/): Research Activity Identifier for tracking project activities.
- **Grant ID**
  - [Grant ID](https://www.crossref.org/categories/grants/): Identifier for the grant supporting the project.
- **Without Funds ID**
  - Identifier for projects not associated with a specific grant.
- **Data Source**
  - Description of data sources used in the project.
- **Data Management Plan**
  - Name: Title of the data management plan.
  - DMP ID: Identifier for the data management plan.
- **Software Management Plan**
  - Name: Title of the software management plan.
  - DMP ID: Identifier for the software management plan.
- **Data Transference Agreement**
  - Agreements for transferring data between entities.
- **Material Transference Agreement**
  - Agreements for transferring physical materials between entities.

### Creator

- **Person ID**
  - ORCID ID: Open Researcher and Contributor ID for unique identification.
  - ISNI ID: International Standard Name Identifier.
  - VIAF ID: Virtual International Authority File identifier.
  - Wikidata ID: Identifier for Wikidata entities.
  - ResearchID (private): Identifier for researchers in the Web of Science.
  - Scopus Author ID (private): Identifier for authors in the Scopus database.
- **Person Name**
  - Family Name (culture): Surname according to cultural naming conventions.
  - Given Name (culture): First name according to cultural naming conventions.
- **Affiliation(s) ID**
  - ROR ID: Research Organization Registry identifier.
  - GRID ID: Global Research Identifier Database ID.
  - ISNI ID: International Standard Name Identifier.
  - Wikidata ID: Identifier for Wikidata entities.
  - Crossref Funder ID: Unique identifier assigned by Crossref.
- **Actual Affiliation**
  - From ORCID ID: Affiliation data from ORCID profile.
  - ROR ID: Research Organization Registry identifier.
  - GRID ID: Global Research Identifier Database ID.
  - ISNI ID: International Standard Name Identifier.
  - Wikidata ID: Identifier for Wikidata entities.
  - Crossref Funder ID: Unique identifier assigned by Crossref.
- **Author Order Code**
  - Disciplinary Context: Contextual information about author order in specific disciplines.
  - Alphabet Order Context: Author order based on alphabetical listing.
- **CRediT Role Code**
  - Contributor Roles Taxonomy (CRediT): Standardized taxonomy for contributor roles.
  - APC Payment: Information on Article Processing Charge payments.
  - Information on the gender of the creator.
- **Career**
  - ORCID ID: Career information linked to ORCID profile.
  - Data on the creator's collaborations and network.
- **Collaboration Data**

### Grant

- **Grant ID**
  - [Grant ID](https://www.crossref.org/categories/grants/)
- **Funding Amount**
  - $(units): Amount of funding awarded.
- **Funding Period**
  - Period (years): Duration of the grant in years.
- **Funder ID**
  - **Public Funders**
    - ROR ID: Research Organization Registry identifier.
    - GRID ID: Global Research Identifier Database ID.
    - ISNI ID: International Standard Name Identifier.
    - Wikidata ID: Identifier for Wikidata entities.
    - Crossref Funder ID: Unique identifier assigned by Crossref.
  - **Private Funders**
    - ROR ID: Research Organization Registry identifier.
    - GRID ID: Global Research Identifier Database ID.
    - ISNI ID: International Standard Name Identifier.
    - Wikidata ID: Identifier for Wikidata entities.
    - Crossref Funder ID: Unique identifier assigned by Crossref.

### Objects Description

- **Report Structure**
  - Sample-based chemistry: Detailed information on chemical samples, including Sample ID and associated metadata.
  - Comma Separated Value (CSV) files: Structured data files for tabular data representation.
  - File-level metadata Reporting Formats: Standards and formats for reporting metadata at the file level.
- **Metadata Representation**
  - OpenAIRE: Standards for metadata interoperability in open science.
  - Datacite: Persistent identifiers for research data and related materials.
  - DublinCore: Standard for cross-domain information resource description.
  - DarwinCore: Standard for sharing biodiversity data.
- **Localization Code**
  - GeoNames ID: Unique identifiers for geographical locations.
- **License Code**
  - Creative Commons licenses, and other open data licenses.
- **Object ID**
  - **Handle-based**
    - Handle: System for assigning and managing persistent identifiers for digital objects.
    - DOI: Digital Object Identifier for uniquely identifying content.
  - **Non Handle-based**
    - ARK: Archival Resource Key for long-term access to information objects.
    - URN: Uniform Resource Name for persistent, location-independent resource identifiers.
    - PURL: Persistent Uniform Resource Locator for redirecting to the current URL of a resource.
  - Summary of the object descriptions, metadata standards, and identification codes.

### Resume
- Summary of key points and considerations for digital artifact traceability.

## Table of Contents

- [Objects Use](#objects-use)
  - [Rights Code](#rights-code)
  - [Embargo Period](#embargo-period)
- [Project](#project)
  - [Project ID](#project-id)
  - [Grant ID (Project)](#grant-id-project)
- [Creator](#creator)
  - [ORCID ID](#orcid-id)
  - [Person Name](#person-name)
- [Grant](#grant)
  - [Grant ID (Funding)](#grant-id-funding)
  - [Funding Amount](#funding-amount)
  - [Funding Period](#funding-period)
  - [Public Funders](#public-funders)
  - [Private Funders](#private-funders)
- [Objects Description](#objects-description)
  - [Report Structure](#report-structure)
  - [Metadata Representation](#metadata-representation)
  - [Localization Code](#localization-code)
  - [License Code](#license-code)
- [Object ID](#object-id)
  - [Handle-based Object ID](#handle-based-object-id)
  - [Non Handle-based Object ID](#non-handle-based-object-id)

## Properties

### Objects Use

#### Rights Code

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| Rights Code | Codes specifying the usage rights and permissions for data objects | String | 1 | CC BY |

#### Embargo Period

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| Embargo Period | Period during which access to data is restricted | String | 1 | 12 months |

### Project

#### Project ID

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| Project ID | Research Activity Identifier for tracking project activities | String | 1 | 10.12345/RAiD.123456 |

#### Grant ID (Project)

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| Grant ID | Identifier for the grant supporting the project | String | 1 | 10.13039/100000001 |

### Creator

#### Author ID

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| ORCID ID | Open Researcher and Contributor ID | String | 1 | https://orcid.org/0000-0001-2345-6789 |

#### Person Name

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| Family Name | Surname according to cultural naming conventions | String | 1 | Doe |
| Given Name | First name according to cultural naming conventions | String | 1 | John |

### Grant

#### Grant ID (Funding)

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| Grant ID | Identifier for the grant supporting the project | String | 1 | 10.13039/100000001 |

#### Funding Amount

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| Funding Amount | Amount of funding awarded | Number | 1 | 1000000 |

#### Funding Period

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| Funding Period | Duration of the grant in years | Number | 1 | 3 |

### Funder ID

#### Public Funders

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| ROR ID | Research Organization Registry identifier | String | 1 | https://ror.org/1234567 |
| GRID ID | Global Research Identifier Database ID | String | 1 | https://grid.ac/institutes/grid.1234.5 |
| ISNI ID | International Standard Name Identifier | String | 1 | https://isni.org/isni/0000000123456789 |
| Wikidata ID | Identifier for Wikidata entities | String | 1 | https://www.wikidata.org/wiki/Q123456 |
| Crossref Funder ID | Unique identifier assigned by Crossref | String | 1 | https://doi.org/10.13039/501100000 |

#### Private Funders

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| ROR ID | Research Organization Registry identifier | String | 1 | https://ror.org/1234567 |
| GRID ID | Global Research Identifier Database ID | String | 1 | https://grid.ac/institutes/grid.1234.5 |
| ISNI ID | International Standard Name Identifier | String | 1 | https://isni.org/isni/0000000123456789 |
| Wikidata ID | Identifier for Wikidata entities | String | 1 | https://www.wikidata.org/wiki/Q123456 |
| Crossref Funder ID | Unique identifier assigned by Crossref | String | 1 | https://doi.org/10.13039/501100000 |

### Objects Description

#### Report Structure

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| Sample ID | Detailed information on chemical samples | String | 1 | Sample123 |

#### Metadata Representation

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| Metadata Standard | Standards for metadata interoperability in open science | String | 1 | OpenAIRE |

#### Localization Code

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| GeoNames ID | Unique identifiers for geographical locations | String | 1 | http://www.geonames.org/1234567 |

#### License Code

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| License Code | Creative Commons licenses and other open data licenses | String | 1 | CC BY 4.0 |

### Object ID

#### Handle-based Object ID

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| Handle | System for assigning and managing persistent identifiers for digital objects | String | 1 | hdl:12345/6789 |
| DOI | Digital Object Identifier for uniquely identifying content | String | 1 | 10.1000/182 |

#### Non Handle-based Object ID

| Name | Description | Data Type | Cardinality | Example Value |
| --- | --- | --- | --- | --- |
| ARK | Archival Resource Key for long-term access to information objects | String | 1 | ark:/12345/xv12345 |
| URN | Uniform Resource Name for persistent, location-independent resource identifiers | String | 1 | urn:nbn:de:0001-0002 |
| PURL | Persistent Uniform Resource Locator for redirecting to the current URL of a resource | String | 1 | http://purl.org/12345 |
