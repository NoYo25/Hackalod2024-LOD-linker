# HackaLOD 2024 - LOD-Linker
* This repository contains scripts that are developed to link People records extracted from three LOD sources and how we linked them using Knowledge Graph Embeddings (KGE)
* This is our contribution for [HackaLOD 2024](https://netwerkdigitaalerfgoed.nl/hackalod/)
* Team:
  *   Nora Abdelmageed - LOD Expert at Nieuwe Instituut
  *   Lois Hutubessy - Program Manager at Nieuwe Instituut
  *   Rianne Piening - Application Manager at RKD
  *   Kelly James - Collectiebeheerder at Nieuwe Instituut

## Data Sources and Criteria 
We retrieved people records from three LOD sources using SPARQL queries. However, you are not limited to SPARQL, you can extract CSV files from your favorite application, e.g., collection management system.
The following are the data sources where we explain the fields and filter functions applied for each.

**Sources**
1. Nieuwe Instituut (NI)
2. Wikidata
3. RKD
   
**Fields**:
* Names (including all alternative names)
* birth dates, birthplaces
* OPTIONAL(death dates, death places)
* occupations

**Filters**
1. **Nieuwe Instituut (NI)**
* retrieved labels for all places and occupations are English

2. **Wikidata**
* Country of birth is Netherlands
* Occupation: architect, photographer, designer that correspond to wd:Q42973 wd:Q33231 wd:Q5322166
* Retrieved labels for all places and occupations are English

3. **RKD**
* Retrieved labels for all places and occupations are English
* death dates and places are mandatory.



