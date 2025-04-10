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

## Properties

### Objects Use

#### Rights Code
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Rights Code</td>
      <td>Codes specifying the usage rights and permissions for data objects</td>
      <td>String</td>
      <td>1</td>
      <td>CC BY</td>
    </tr>
  </tbody>
</table>

#### Embargo Period
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Embargo Period</td>
      <td>Period during which access to data is restricted</td>
      <td>String</td>
      <td>1</td>
      <td>12 months</td>
    </tr>
  </tbody>
</table>

### Project

#### Project ID
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Project ID</td>
      <td>Research Activity Identifier for tracking project activities</td>
      <td>String</td>
      <td>1</td>
      <td>10.12345/RAiD.123456</td>
    </tr>
  </tbody>
</table>

#### Grant ID
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Grant ID</td>
      <td>Identifier for the grant supporting the project</td>
      <td>String</td>
      <td>1</td>
      <td>10.13039/100000001</td>
    </tr>
  </tbody>
</table>

### Creator

#### Person ID
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ORCID ID</td>
      <td>Open Researcher and Contributor ID</td>
      <td>String</td>
      <td>1</td>
      <td>https://orcid.org/0000-0001-2345-6789</td>
    </tr>
  </tbody>
</table>

#### Person Name
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Family Name</td>
      <td>Surname according to cultural naming conventions</td>
      <td>String</td>
      <td>1</td>
      <td>Doe</td>
    </tr>
    <tr>
      <td>Given Name</td>
      <td>First name according to cultural naming conventions</td>
      <td>String</td>
      <td>1</td>
      <td>John</td>
    </tr>
  </tbody>
</table>

### Grant

#### Grant ID
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Grant ID</td>
      <td>Identifier for the grant supporting the project</td>
      <td>String</td>
      <td>1</td>
      <td>10.13039/100000001</td>
    </tr>
  </tbody>
</table>

#### Funding Amount
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Funding Amount</td>
      <td>Amount of funding awarded</td>
      <td>Number</td>
      <td>1</td>
      <td>1000000</td>
    </tr>
  </tbody>
</table>

#### Funding Period
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Funding Period</td>
      <td>Duration of the grant in years</td>
      <td>Number</td>
      <td>1</td>
      <td>3</td>
    </tr>
  </tbody>
</table>

#### Funder ID

##### Public Funders
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ROR ID</td>
      <td>Research Organization Registry identifier</td>
      <td>String</td>
      <td>1</td>
      <td>https://ror.org/1234567</td>
    </tr>
    <tr>
      <td>GRID ID</td>
      <td>Global Research Identifier Database ID</td>
      <td>String</td>
      <td>1</td>
      <td>https://grid.ac/institutes/grid.1234.5</td>
    </tr>
    <tr>
      <td>ISNI ID</td>
      <td>International Standard Name Identifier</td>
      <td>String</td>
      <td>1</td>
      <td>https://isni.org/isni/0000000123456789</td>
    </tr>
    <tr>
      <td>Wikidata ID</td>
      <td>Identifier for Wikidata entities</td>
      <td>String</td>
      <td>1</td>
      <td>https://www.wikidata.org/wiki/Q123456</td>
    </tr>
    <tr>
      <td>Crossref Funder ID</td>
      <td>Unique identifier assigned by Crossref</td>
      <td>String</td>
      <td>1</td>
      <td>https://doi.org/10.13039/501100000</td>
    </tr>
  </tbody>
</table>

##### Private Funders
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ROR ID</td>
      <td>Research Organization Registry identifier</td>
      <td>String</td>
      <td>1</td>
      <td>https://ror.org/1234567</td>
    </tr>
    <tr>
      <td>GRID ID</td>
      <td>Global Research Identifier Database ID</td>
      <td>String</td>
      <td>1</td>
      <td>https://grid.ac/institutes/grid.1234.5</td>
    </tr>
    <tr>
      <td>ISNI ID</td>
      <td>International Standard Name Identifier</td>
      <td>String</td>
      <td>1</td>
      <td>https://isni.org/isni/0000000123456789</td>
    </tr>
    <tr>
      <td>Wikidata ID</td>
      <td>Identifier for Wikidata entities</td>
      <td>String</td>
      <td>1</td>
      <td>https://www.wikidata.org/wiki/Q123456</td>
    </tr>
    <tr>
      <td>Crossref Funder ID</td>
      <td>Unique identifier assigned by Crossref</td>
      <td>String</td>
      <td>1</td>
      <td>https://doi.org/10.13039/501100000</td>
    </tr>
  </tbody>
</table>

### Objects Description

#### Report Structure
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Sample ID</td>
      <td>Detailed information on chemical samples</td>
      <td>String</td>
      <td>1</td>
      <td>Sample123</td>
    </tr>
  </tbody>
</table>

#### Metadata Representation
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Metadata Standard</td>
      <td>Standards for metadata interoperability in open science</td>
      <td>String</td>
      <td>1</td>
      <td>OpenAIRE</td>
    </tr>
  </tbody>
</table>

#### Localization Code
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>GeoNames ID</td>
      <td>Unique identifiers for geographical locations</td>
      <td>String</td>
      <td>1</td>
      <td>http://www.geonames.org/1234567</td>
    </tr>
  </tbody>
</table>

#### License Code
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>License Code</td>
      <td>Creative Commons licenses and other open data licenses</td>
      <td>String</td>
      <td>1</td>
      <td>CC BY 4.0</td>
    </tr>
  </tbody>
</table>

#### Object ID

##### Handle-based
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Handle</td>
      <td>System for assigning and managing persistent identifiers for digital objects</td>
      <td>String</td>
      <td>1</td>
      <td>hdl:12345/6789</td>
    </tr>
    <tr>
      <td>DOI</td>
      <td>Digital Object Identifier for uniquely identifying content</td>
      <td>String</td>
      <td>1</td>
      <td>10.1000/182</td>
    </tr>
  </tbody>
</table>

##### Non Handle-based
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Data Type</th>
      <th>Cardinality</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ARK</td>
      <td>Archival Resource Key for long-term access to information objects</td>
      <td>String</td>
      <td>1</td>
      <td>ark:/12345/xv12345</td>
    </tr>
    <tr>
      <td>URN</td>
      <td>Uniform Resource Name for persistent, location-independent resource identifiers</td>
      <td>String</td>
      <td>1</td>
      <td>urn:nbn:de:0001-0002</td>
    </tr>
    <tr>
      <td>PURL</td>
      <td>Persistent Uniform Resource Locator for redirecting to the current URL of a resource</td>
      <td>String</td>
      <td>1</td>
      <td>http://purl.org/12345</td>
    </tr>
  </tbody>
</table>


