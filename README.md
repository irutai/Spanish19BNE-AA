# Spanish19BNE-AA
A dataset for large-scale AA derived from the digitized collections of the National Library of Spain (Biblioteca Nacional de España, BNE). It comprises OCR-based textual representations of works written in Spanish and published during 19-20th centuries: total of 425 authors; 6,432 works used for training and 1,609 for test after an 80-20 split.

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


## License
This project is licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0).

### Attribution Requirement
If you use, modify, or distribute this work, you must give appropriate credit by citing the following paper:

, 2026.
DOI:  https://doi.org/xxx

In addition, you must indicate if changes were made and include a link to this repository.
