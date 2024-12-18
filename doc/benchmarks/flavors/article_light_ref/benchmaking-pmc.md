## Header metadata

Evaluation on 1943 random PDF files out of 1941 PDF (ratio 1.0).

#### Strict Matching (exact matches)

**Field-level results**

| label                       | precision | recall    | f1        | support |
|-----------------------------|-----------|-----------|-----------|---------|
| authors                     | 92.45     | 92.07     | 92.26     | 1941    |
| first_author                | 96.38     | 95.98     | 96.18     | 1941    |
| title                       | 84.27     | 83.27     | 83.77     | 1943    |
|                             |           |           |           |         |
| **all fields (micro avg.)** | **91.05** | **90.44** | **90.74** | 5825    |
| all fields (macro avg.)     | 91.03     | 90.44     | 90.73     | 5825    |

#### Soft Matching (ignoring punctuation, case and space characters mismatches)

**Field-level results**

| label                       | precision | recall    | f1        | support |
|-----------------------------|-----------|-----------|-----------|---------|
| authors                     | 94.36     | 93.97     | 94.17     | 1941    |
| first_author                | 96.74     | 96.34     | 96.54     | 1941    |
| title                       | 92.03     | 90.94     | 91.48     | 1943    |
|                             |           |           |           |         |
| **all fields (micro avg.)** | **94.38** | **93.75** | **94.07** | 5825    |
| all fields (macro avg.)     | 94.38     | 93.75     | 94.06     | 5825    |

#### Levenshtein Matching (Minimum Levenshtein distance at 0.8)

**Field-level results**

| label                       | precision | recall    | f1        | support |
|-----------------------------|-----------|-----------|-----------|---------|
| authors                     | 96.59     | 96.19     | 96.39     | 1941    |
| first_author                | 97.05     | 96.65     | 96.85     | 1941    |
| title                       | 98.18     | 97.01     | 97.59     | 1943    |
|                             |           |           |           |         |
| **all fields (micro avg.)** | **97.27** | **96.62** | **96.94** | 5825    |
| all fields (macro avg.)     | 97.27     | 96.62     | 96.94     | 5825    |

#### Ratcliff/Obershelp Matching (Minimum Ratcliff/Obershelp similarity at 0.95)

**Field-level results**

| label                       | precision | recall    | f1        | support |
|-----------------------------|-----------|-----------|-----------|---------|
| authors                     | 95.6      | 95.21     | 95.41     | 1941    |
| first_author                | 96.38     | 95.98     | 96.18     | 1941    |
| title                       | 96.2      | 95.06     | 95.63     | 1943    |
|                             |           |           |           |         |
| **all fields (micro avg.)** | **96.06** | **95.42** | **95.74** | 5825    |
| all fields (macro avg.)     | 96.06     | 95.42     | 95.74     | 5825    |

#### Instance-level results

```
Total expected instances: 	1943
Total correct instances: 	1507 (strict) 
Total correct instances: 	1672 (soft) 
Total correct instances: 	1820 (Levenshtein) 
Total correct instances: 	1764 (ObservedRatcliffObershelp) 

Instance-level recall:	77.56	(strict) 
Instance-level recall:	86.05	(soft) 
Instance-level recall:	93.67	(Levenshtein) 
Instance-level recall:	90.79	(RatcliffObershelp) 
```

## Citation metadata

Evaluation on 1943 random PDF files out of 1941 PDF (ratio 1.0).

#### Strict Matching (exact matches)

**Field-level results**

| label                       | precision | recall    | f1        | support |
|-----------------------------|-----------|-----------|-----------|---------|
| authors                     | 82.75     | 75.91     | 79.18     | 85778   |
| date                        | 93.93     | 83.72     | 88.53     | 87067   |
| first_author                | 89.45     | 82.02     | 85.57     | 85778   |
| inTitle                     | 72.53     | 71.31     | 71.91     | 81007   |
| issue                       | 87.61     | 87.48     | 87.54     | 16635   |
| page                        | 93.43     | 82.97     | 87.89     | 80501   |
| title                       | 79.19     | 74.82     | 76.94     | 80736   |
| volume                      | 95.14     | 89.25     | 92.1      | 80067   |
|                             |           |           |           |         |
| **all fields (micro avg.)** | **86.51** | **80.21** | **83.24** | 597569  |
| all fields (macro avg.)     | 86.75     | 80.93     | 83.71     | 597569  |

#### Soft Matching (ignoring punctuation, case and space characters mismatches)

**Field-level results**

| label                       | precision | recall    | f1        | support |
|-----------------------------|-----------|-----------|-----------|---------|
| authors                     | 83.22     | 76.34     | 79.63     | 85778   |
| date                        | 93.93     | 83.72     | 88.53     | 87067   |
| first_author                | 89.62     | 82.18     | 85.74     | 85778   |
| inTitle                     | 84.16     | 82.74     | 83.45     | 81007   |
| issue                       | 87.61     | 87.48     | 87.54     | 16635   |
| page                        | 93.43     | 82.97     | 87.89     | 80501   |
| title                       | 90.89     | 85.86     | 88.3      | 80736   |
| volume                      | 95.14     | 89.25     | 92.1      | 80067   |
|                             |           |           |           |         |
| **all fields (micro avg.)** | **89.88** | **83.34** | **86.49** | 597569  |
| all fields (macro avg.)     | 89.75     | 83.82     | 86.65     | 597569  |

#### Levenshtein Matching (Minimum Levenshtein distance at 0.8)

**Field-level results**

| label                       | precision | recall    | f1        | support |
|-----------------------------|-----------|-----------|-----------|---------|
| authors                     | 88.86     | 81.51     | 85.03     | 85778   |
| date                        | 93.93     | 83.72     | 88.53     | 87067   |
| first_author                | 89.81     | 82.35     | 85.92     | 85778   |
| inTitle                     | 85.4      | 83.96     | 84.68     | 81007   |
| issue                       | 87.61     | 87.48     | 87.54     | 16635   |
| page                        | 93.43     | 82.97     | 87.89     | 80501   |
| title                       | 93.21     | 88.06     | 90.56     | 80736   |
| volume                      | 95.14     | 89.25     | 92.1      | 80067   |
|                             |           |           |           |         |
| **all fields (micro avg.)** | **91.21** | **84.57** | **87.77** | 597569  |
| all fields (macro avg.)     | 90.92     | 84.91     | 87.78     | 597569  |

#### Ratcliff/Obershelp Matching (Minimum Ratcliff/Obershelp similarity at 0.95)

**Field-level results**

| label                       | precision | recall   | f1        | support |
|-----------------------------|-----------|----------|-----------|---------|
| authors                     | 85.68     | 78.59    | 81.98     | 85778   |
| date                        | 93.93     | 83.72    | 88.53     | 87067   |
| first_author                | 89.46     | 82.04    | 85.59     | 85778   |
| inTitle                     | 82.76     | 81.36    | 82.05     | 81007   |
| issue                       | 87.61     | 87.48    | 87.54     | 16635   |
| page                        | 93.43     | 82.97    | 87.89     | 80501   |
| title                       | 92.81     | 87.68    | 90.17     | 80736   |
| volume                      | 95.14     | 89.25    | 92.1      | 80067   |
|                             |           |          |           |         |
| **all fields (micro avg.)** | **90.27** | **83.7** | **86.86** | 597569  |
| all fields (macro avg.)     | 90.1      | 84.14    | 86.98     | 597569  |

#### Instance-level results

```
Total expected instances: 		90125
Total extracted instances: 		86410
Total correct instances: 		38449 (strict) 
Total correct instances: 		50473 (soft) 
Total correct instances: 		55286 (Levenshtein) 
Total correct instances: 		51882 (RatcliffObershelp) 

Instance-level precision:	44.5 (strict) 
Instance-level precision:	58.41 (soft) 
Instance-level precision:	63.98 (Levenshtein) 
Instance-level precision:	60.04 (RatcliffObershelp) 

Instance-level recall:	42.66	(strict) 
Instance-level recall:	56	(soft) 
Instance-level recall:	61.34	(Levenshtein) 
Instance-level recall:	57.57	(RatcliffObershelp) 

Instance-level f-score:	43.56 (strict) 
Instance-level f-score:	57.18 (soft) 
Instance-level f-score:	62.63 (Levenshtein) 
Instance-level f-score:	58.78 (RatcliffObershelp) 

Matching 1 :	67871

Matching 2 :	4150

Matching 3 :	1863

Matching 4 :	672

Total matches :	74556
```

#### Citation context resolution

```

Total expected references: 	 90125 - 46.38 references per article
Total predicted references: 	 86410 - 44.47 references per article

Total expected citation contexts: 	 139835 - 71.97 citation contexts per article
Total predicted citation contexts: 	 0 - 0 citation contexts per article

Total correct predicted citation contexts: 	 0 - 0 citation contexts per article
Total wrong predicted citation contexts: 	 0 (wrong callout matching, callout missing in NLM, or matching with a bib. ref. not aligned with a bib.ref. in NLM)

Precision citation contexts: 	 NaN
Recall citation contexts: 	 0
fscore citation contexts: 	 NaN
```

Evaluation metrics produced in 1474.976 seconds
