# Spanish19BNE-AA: structure of the data in the repository

Spanish19BNE-AA is a dataset for large-scale AA derived from the digitized collections of the National Library of Spain (Biblioteca Nacional de España, BNE). It comprises OCR-based textual representations of works written in Spanish and published during 19-20th centuries: total of 425 authors; 6,432 works used for training and 1,609 for test after an 80-20 split.

#### + Spanish19BNE-AA_raw.zip

This file contains the OCR-extracted raw text of the documents in the AA collection, separatedly in 2 folders for the train data (80%) and for the test (20%).

Regarding the dataset, each of the two folders for train and test is organized into **425 directories**, each one representing an author in the **Spanish19BNE-AA** collection.  
Inside each author directory, you will find the `.txt` files corresponding to each **manifestation** of that author included in the collection.

Each text file follows this naming convention:

`publication_code_publication_year_author_name_birth_year-death_year.txt`

#### Example

```
SinDuplicados_Test20:
SinDuplicados_Train80:
|__ ...
|__ Zorrilla_José_1817-1893:
      |__ ...
      |__ bimo0001594704_1839_Zorrilla_José_1817-1893.txt
      |__ bimo0001594627_1910_Zorrilla_José_1817-1893.txt
      |__ ...
|__ ...
```

#### + OCRvsCurated_16_test_texts

In this folder, as an additional study, to investigate if quality of the textual source affects AA performance, a controlled comparison between OCR-derived texts and manually curated digital editions is developed, with same training process but a separate evaluation using two alternative versions of the same test documents.

To do a comparative evaluation, a subset of 16 literary works from the original OCR-based test collection is chosen (in OCRvsCurated_16_test_texts/test_selected_OCR, with same structure as before). The works are compared with the corresponding manually curated digital version (in OCRvsCurated_16_test_texts/test_selected_curated) obtained from Project Gutenberg (original txts are in folder OCRvsCurated_16_test_texts/test_selected_curated_originally_from_gutenberg, but they has been adapted --and also de OCR-based texts-- to trim a percentage of the works at the beginning and at the end).


# Spanish19BNE-AA: provenance, public-domain status, and reuse rights

## Source and verification

Spanish19BNE-AA contains OCR text transcriptions originally supplied by the Biblioteca Nacional de España (BNE), together with corpus metadata. It does **not** redistribute digitized images or PDF files. The research team curated the source collection for authorship attribution through single-author selection, OCR-quality filtering, and removal of substantial textual overlap.

All 8,041 corpus documents (6,432 train; 1,609 test) were matched by exact BNE identifier to entries in the BNE's official *Biblioteca Digital. Documentos en dominio público* dataset, including an OCR reference. This establishes documentary correspondence with the BNE's public-domain classification, but is not an independent legal certification of every contribution present in an edition.

## BNE licensing and reuse conditions

The BNE's official legal notice distinguishes among kinds of source material:

- **Underlying literary works:** inclusion in the BNE public-domain collection is documentary evidence of their public-domain classification. The original works are not relicensed by Spanish19BNE-AA.
- **BNE bibliographic metadata:** the BNE states that its catalogue metadata are available under **CC0 1.0 Universal**, including commercial reuse.
- **BNE digitized images:** the BNE identifies its openly available images of public-domain works as **CC BY 4.0 or equivalent**, unless otherwise specified. **Images are not included in Spanish19BNE-AA.** This image-specific licensing statement should not automatically be treated as an item-level license on OCR transcriptions.
- **BNE-provided OCR files:** these are the source texts used by Spanish19BNE-AA. The BNE communicated directly to the corpus authors that the OCR materials concerned may be reused without copyright restrictions. This corpus therefore acknowledges the BNE as the OCR source and refers users to the BNE's applicable public-reuse conditions. The public notices consulted do not clearly establish a single, separate CC license for every individual OCR file; we do not assign one by inference.

The BNE's general public-sector information reuse terms allow commercial and non-commercial reuse of information subject to those terms, including copying, distribution and adaptation. Among other requirements, they call for acknowledgement of the BNE as source, preservation of existing applicable rights/reuse metadata, and avoidance of any suggestion that the BNE endorses the derivative resource. See the sources below for scope and current conditions.

Suggested source acknowledgement: **"Origen de los datos: Biblioteca Nacional de España"** ("Data source: Biblioteca Nacional de España").

## License for original corpus contributions

To the extent that the corpus developers hold copyright or applicable database rights in the **original selection, structure, organization, annotations, documentation, or other eligible contributions** to Spanish19BNE-AA, those rights are licensed under **Creative Commons Attribution 4.0 International (CC BY 4.0)**: https://creativecommons.org/licenses/by/4.0/ . This choice does not confer any rights over, or impose new restrictions upon, public-domain literary works or third-party BNE materials. Attribution to the original research dataset should be provided when reusing eligible licensed contributions.
 
## Item-level provenance manifest

`Spanish19BNE-AA_provenance_rights.csv` contains one row per corpus document, with its BNE identifier, author/bibliographic details, source digital-resource and OCR references, original BNE `Condiciones de uso` value, and verification outcome. `bne_source_file` and `bne_source_record_number` support auditing against the source CSV exports.

In the matched BNE records, `Condiciones de uso` was empty for 7,681 documents and contained `//` for 360. These source values are retained *as supplied* and are **not** interpreted as an individual CC license, a denial of reuse permission, or a modification of the BNE's published collection-level policy.

The exported BNE URL fields end in ` **` in the source data. The raw values are preserved in the manifest; remove that suffix when opening the URLs. Links have not been individually tested for current availability. Exact identifier matching does not establish byte-for-byte identity between historical OCR downloads and files currently linked by the BNE.

## Official sources

1. BNE, *Aviso legal* — licensing of public-domain images, CC0 metadata and public-sector information reuse conditions: https://www.bne.es/es/aviso-legal
2. BNE, *Uso de las reproducciones* — conditions for reproductions (particularly images): https://www.bne.es/es/servicios/reproduccion-documentos/uso-reproducciones
3. BNE, *Biblioteca Digital. Documentos en dominio público* — official source dataset: https://datosabiertos.bne.es/catalogo/dataset/biblioteca-digital-documentos-en-dominio-publico
4. Creative Commons, *CC BY 4.0*: https://creativecommons.org/licenses/by/4.0/

Checked against the BNE legal notice on 23 October 2026. The BNE's direct communication concerning the OCR texts is reported by the corpus authors and should be retained with the project's internal documentation, including its date and scope where available.

## Attribution Requirement
If you use, modify, or distribute this work, you must give appropriate credit by citing the following paper:

, 2026.
DOI:  https://doi.org/xxx

In addition, you must indicate if changes were made and include a link to this repository.
