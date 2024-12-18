# Benchmarking PLOS

## General

This is the end-to-end benchmarking result for GROBID version **0.8.1** against the `PLOS` test set, see the [End-to-end evaluation](End-to-end-evaluation.md) page for explanations and for reproducing this evaluation. 

The following end-to-end results are using:

- **BidLSTM_ChainCRF_FEATURES** as sequence labeling for the header model

- **BidLSTM_ChainCRF_FEATURES** as sequence labeling for the reference-segmenter model

- **BidLSTM-CRF-FEATURES** as sequence labeling for the citation model

- **BidLSTM_CRF_FEATURES** as sequence labeling for the affiliation-address model

- **CRF Wapiti** as sequence labelling engine for all other models.  

Header extractions are consolidated by default with [biblio-glutton](https://github.com/kermitt2/biblio-glutton) service (the results with CrossRef REST API as consolidation service should be similar but much slower). 

Other versions of these benchmarks with variants and **Deep Learning models** (e.g. newer master snapshots) are available [here](https://github.com/kermitt2/grobid/tree/master/grobid-trainer/doc). Note that Deep Learning models might provide higher accuracy, but at the cost of slower runtime and more expensive CPU/GPU resources. 

Evaluation on 1000 PDF preprints out of 1000 (no failure).

Runtime for processing 1000 PDF: **999** seconds, (0.99 seconds per PDF) on Ubuntu 22.04, 16 CPU (32 threads), 128GB RAM and with a GeForce GTX 1080 Ti GPU.

Note: with CRF only models runtime is 304s (0.30 seconds per PDF) with 4 CPU, 8 threads. 


## Header metadata 

Evaluation on 1000 random PDF files out of 998 PDF (ratio 1.0).

#### Strict Matching (exact matches)

**Field-level results**

| label            |  precision |   recall  |     f1     | support |
|---               |---         |---        |---         |---      |
| abstract | 13.58 | 13.65 | 13.61 | 960 |
| authors | 98.87 | 98.97 | 98.92 | 969 |
| first_author | 99.18 | 99.28 | 99.23 | 969 |
| keywords | 0 | 0 | 0 | 0 |
| title | 95.75 | 94.6 | 95.17 | 1000 |
|                  |            |           |            |         |
| **all fields (micro avg.)** | **77.01** | **76.91** | **76.96** | 3898 |
| all fields (macro avg.) | 76.84 | 76.62 | 76.73 | 3898 |



#### Soft Matching (ignoring punctuation, case and space characters mismatches)

**Field-level results**

| label            |  precision |   recall  |     f1     | support |
|---               |---         |---        |---         |---      |
| abstract | 50.57 | 50.83 | 50.7 | 960 |
| authors | 98.87 | 98.97 | 98.92 | 969 |
| first_author | 99.18 | 99.28 | 99.23 | 969 |
| keywords | 0 | 0 | 0 | 0 |
| title | 99.39 | 98.2 | 98.79 | 1000 |
|                  |            |           |            |         |
| **all fields (micro avg.)** | **87.11** | **86.99** | **87.05** | 3898 |
| all fields (macro avg.) | 87 | 86.82 | 86.91 | 3898 |



#### Levenshtein Matching (Minimum Levenshtein distance at 0.8)

**Field-level results**

| label            |  precision |   recall  |     f1     | support |
|---               |---         |---        |---         |---      |
| abstract | 76.68 | 77.08 | 76.88 | 960 |
| authors | 99.28 | 99.38 | 99.33 | 969 |
| first_author | 99.28 | 99.38 | 99.33 | 969 |
| keywords | 0 | 0 | 0 | 0 |
| title | 99.7 | 98.5 | 99.09 | 1000 |
|                  |            |           |            |         |
| **all fields (micro avg.)** | **93.78** | **93.66** | **93.72** | 3898 |
| all fields (macro avg.) | 93.73 | 93.59 | 93.66 | 3898 |



#### Ratcliff/Obershelp Matching (Minimum Ratcliff/Obershelp similarity at 0.95)

**Field-level results**

| label            |  precision |   recall  |     f1     | support |
|---               |---         |---        |---         |---      |
| abstract | 66.94 | 67.29 | 67.12 | 960 |
| authors | 99.18 | 99.28 | 99.23 | 969 |
| first_author | 99.18 | 99.28 | 99.23 | 969 |
| keywords | 0 | 0 | 0 | 0 |
| title | 99.49 | 98.3 | 98.89 | 1000 |
|                  |            |           |            |         |
| **all fields (micro avg.)** | **91.27** | **91.15** | **91.21** | 3898 |
| all fields (macro avg.) | 91.2 | 91.04 | 91.12 | 3898 |


#### Instance-level results

```
Total expected instances: 	1000
Total correct instances: 	139 (strict) 
Total correct instances: 	487 (soft) 
Total correct instances: 	726 (Levenshtein) 
Total correct instances: 	642 (ObservedRatcliffObershelp) 

Instance-level recall:	13.9	(strict) 
Instance-level recall:	48.7	(soft) 
Instance-level recall:	72.6	(Levenshtein) 
Instance-level recall:	64.2	(RatcliffObershelp) 
```


## Citation metadata 

Evaluation on 1000 random PDF files out of 998 PDF (ratio 1.0).

#### Strict Matching (exact matches)

**Field-level results**

| label            |  precision |   recall  |     f1     | support |
|---               |---         |---        |---         |---      |
| authors | 81.17 | 78.43 | 79.78 | 44770 |
| date | 84.61 | 81.24 | 82.89 | 45457 |
| first_author | 91.47 | 88.34 | 89.88 | 44770 |
| inTitle | 81.67 | 83.58 | 82.61 | 42795 |
| issue | 93.62 | 92.68 | 93.15 | 18983 |
| page | 93.7 | 77.57 | 84.87 | 40844 |
| title | 59.97 | 60.47 | 60.22 | 43101 |
| volume | 95.89 | 96.11 | 96 | 40458 |
|                  |            |           |            |         |
| **all fields (micro avg.)** | **84.23** | **81.45** | **82.81** | 321178 |
| all fields (macro avg.) | 85.26 | 82.3 | 83.67 | 321178 |



#### Soft Matching (ignoring punctuation, case and space characters mismatches)

**Field-level results**

| label            |  precision |   recall  |     f1     | support |
|---               |---         |---        |---         |---      |
| authors | 81.49 | 78.73 | 80.09 | 44770 |
| date | 84.61 | 81.24 | 82.89 | 45457 |
| first_author | 91.69 | 88.55 | 90.09 | 44770 |
| inTitle | 85.51 | 87.5 | 86.49 | 42795 |
| issue | 93.62 | 92.68 | 93.15 | 18983 |
| page | 93.7 | 77.57 | 84.87 | 40844 |
| title | 91.95 | 92.74 | 92.34 | 43101 |
| volume | 95.89 | 96.11 | 96 | 40458 |
|                  |            |           |            |         |
| **all fields (micro avg.)** | **89.32** | **86.37** | **87.82** | 321178 |
| all fields (macro avg.) | 89.81 | 86.89 | 88.24 | 321178 |



#### Levenshtein Matching (Minimum Levenshtein distance at 0.8)

**Field-level results**

| label            |  precision |   recall  |     f1     | support |
|---               |---         |---        |---         |---      |
| authors | 90.64 | 87.57 | 89.08 | 44770 |
| date | 84.61 | 81.24 | 82.89 | 45457 |
| first_author | 92.23 | 89.08 | 90.62 | 44770 |
| inTitle | 86.45 | 88.47 | 87.45 | 42795 |
| issue | 93.62 | 92.68 | 93.15 | 18983 |
| page | 93.7 | 77.57 | 84.87 | 40844 |
| title | 94.56 | 95.37 | 94.96 | 43101 |
| volume | 95.89 | 96.11 | 96 | 40458 |
|                  |            |           |            |         |
| **all fields (micro avg.)** | **91.17** | **88.16** | **89.64** | 321178 |
| all fields (macro avg.) | 91.46 | 88.51 | 89.88 | 321178 |



#### Ratcliff/Obershelp Matching (Minimum Ratcliff/Obershelp similarity at 0.95)

**Field-level results**

| label            |  precision |   recall  |     f1     | support |
|---               |---         |---        |---         |---      |
| authors | 84.94 | 82.06 | 83.48 | 44770 |
| date | 84.61 | 81.24 | 82.89 | 45457 |
| first_author | 91.47 | 88.34 | 89.88 | 44770 |
| inTitle | 85.16 | 87.15 | 86.14 | 42795 |
| issue | 93.62 | 92.68 | 93.15 | 18983 |
| page | 93.7 | 77.57 | 84.87 | 40844 |
| title | 93.95 | 94.74 | 94.34 | 43101 |
| volume | 95.89 | 96.11 | 96 | 40458 |
|                  |            |           |            |         |
| **all fields (micro avg.)** | **90** | **87.03** | **88.49** | 321178 |
| all fields (macro avg.) | 90.42 | 87.49 | 88.84 | 321178 |


#### Instance-level results

```
Total expected instances: 		48449
Total extracted instances: 		48250
Total correct instances: 		13496 (strict) 
Total correct instances: 		22269 (soft) 
Total correct instances: 		24916 (Levenshtein) 
Total correct instances: 		23272 (RatcliffObershelp) 

Instance-level precision:	27.97 (strict) 
Instance-level precision:	46.15 (soft) 
Instance-level precision:	51.64 (Levenshtein) 
Instance-level precision:	48.23 (RatcliffObershelp) 

Instance-level recall:	27.86	(strict) 
Instance-level recall:	45.96	(soft) 
Instance-level recall:	51.43	(Levenshtein) 
Instance-level recall:	48.03	(RatcliffObershelp) 

Instance-level f-score:	27.91 (strict) 
Instance-level f-score:	46.06 (soft) 
Instance-level f-score:	51.53 (Levenshtein) 
Instance-level f-score:	48.13 (RatcliffObershelp) 

Matching 1 :	35369

Matching 2 :	1260

Matching 3 :	3266

Matching 4 :	1800

Total matches :	41695
```


#### Citation context resolution
```

Total expected references: 	 48449 - 48.45 references per article
Total predicted references: 	 48250 - 48.25 references per article

Total expected citation contexts: 	 69755 - 69.75 citation contexts per article
Total predicted citation contexts: 	 73696 - 73.7 citation contexts per article

Total correct predicted citation contexts: 	 56772 - 56.77 citation contexts per article
Total wrong predicted citation contexts: 	 16924 (wrong callout matching, callout missing in NLM, or matching with a bib. ref. not aligned with a bib.ref. in NLM)

Precision citation contexts: 	 77.04
Recall citation contexts: 	 81.39
fscore citation contexts: 	 79.15
```


## Fulltext structures 

Fulltext structure contents are complicated to capture from JATS NLM files. They are often normalized and different from the actual PDF content and are can be inconsistent from one document to another. The scores of the following metrics are thus not very meaningful in absolute term, in particular for the strict matching (textual content of the srtructure can be very long). As relative values for comparing different models, they seem however useful.


Evaluation on 1000 random PDF files out of 998 PDF (ratio 1.0).

#### Strict Matching (exact matches)

**Field-level results**

| label            |  precision |   recall  |     f1     | support |
|---               |---         |---        |---         |---      |
| availability_stmt | 54.06 | 52.12 | 53.07 | 779 |
| figure_title | 2.11 | 0.92 | 1.28 | 8943 |
| funding_stmt | 5.27 | 28.14 | 8.88 | 1507 |
| reference_citation | 86.69 | 94.65 | 90.49 | 69741 |
| reference_figure | 72.06 | 54.06 | 61.77 | 11010 |
| reference_table | 84.28 | 92.07 | 88 | 5159 |
| section_title | 77.18 | 65.8 | 71.03 | 17540 |
| table_title | 1.13 | 0.59 | 0.77 | 6092 |
|                  |            |           |            |         |
| **all fields (micro avg.)** | **73.79** | **73.86** | **73.82** | 120771 |
| all fields (macro avg.) | 47.85 | 48.54 | 46.91 | 120771 |



#### Soft Matching (ignoring punctuation, case and space characters mismatches)

**Field-level results**

| label            |  precision |   recall  |     f1     | support |
|---               |---         |---        |---         |---      |
| availability_stmt | 79.36 | 76.51 | 77.91 | 779 |
| figure_title | 81.17 | 35.33 | 49.24 | 8943 |
| funding_stmt | 6.89 | 36.76 | 11.6 | 1507 |
| reference_citation | 86.7 | 94.66 | 90.51 | 69741 |
| reference_figure | 72.52 | 54.41 | 62.17 | 11010 |
| reference_table | 84.46 | 92.27 | 88.19 | 5159 |
| section_title | 78.17 | 66.65 | 71.95 | 17540 |
| table_title | 15.97 | 8.39 | 11 | 6092 |
|                  |            |           |            |         |
| **all fields (micro avg.)** | **77.16** | **77.24** | **77.2** | 120771 |
| all fields (macro avg.) | 63.16 | 58.12 | 57.82 | 120771 |


**Document-level ratio results**

| label            |  precision |   recall  |     f1     | support |
|---               |---         |---        |---         |---      |
| availability_stmt | 99.47 | 96.41 | 97.91 | 779 |
|                  |            |           |            |         |
| **all fields (micro avg.)** | **99.47** | **96.41** | **97.91** | 779 |
| all fields (macro avg.) | 99.47 | 96.41 | 97.91 | 779 |

Evaluation metrics produced in 396.908 seconds

