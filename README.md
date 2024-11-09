# HackaLOD 2024 - LOD-Linker
* This repository contains scripts that are developed to link People records extracted from three LOD sources and how we linked them using Knowledge Graph Embeddings (KGE)
* This is our contribution for [HackaLOD 2024](https://netwerkdigitaalerfgoed.nl/hackalod/)
* Team:
  *   Nora Abdelmageed - LOD Expert at Nieuwe Instituut
  *   Lois Hutubessy - Program Manager at Nieuwe Instituut
  *   Rianne Piening - Application Manager at RKD
  *   Kelly James - Collectiebeheerder at Nieuwe Instituut

## Data Sources and Criteria 
We retrieved people records from three LOD sources using SPARQL queries. However, you are not limited to SPARQL; you can extract CSV files from your favorite application, e.g., a collection management system.
The following are the data sources where we explain the fields and filter functions applied for each.
You can find our [Queries](https://github.com/NoYo25/Hackalod2024-LOD-linker/tree/main/Queries) and retrieved [Data](https://github.com/NoYo25/Hackalod2024-LOD-linker/tree/main/Data) in this repository as well. 

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
* Occupation: architect, photographer, designer that corresponds to wd:Q42973 wd:Q33231 wd:Q5322166
* Retrieved labels for all places and occupations are English

3. **RKD**
* Retrieved labels for all places and occupations are English
* death dates and places are mandatory.

## Methodology 
* LOD-Linker relies on Knowledge Graph Embeddings (KGE), TransH model.
* The implementation uses the [pykeen](https://github.com/pykeen/pykeen) library for KGE.
* We conducted 4 experiments to test. All are found in the [Code](https://github.com/NoYo25/Hackalod2024-LOD-linker/tree/main/Code) folder in this repository:
1. **Language & Data Points**
   * All retrieved labels should be in the same language?
   * Can we match English with Dutch
2. **Embedding Size**
   * Is a small dimension sufficient, or are large embeddings required?
3. **Data Cleaning**
   * Should we normalize all names? Could you get rid of all punctuation and make sure letter case?
   * Can we keep the original format of the names (remember it is one of the downsides of baselines)
4. **Data Balance**
   * Each source should contribute nearly the same amount of record 
   * One source could be dominant (biases?)





