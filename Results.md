# Results (running updates)

The writing samples are incomplete but let's just try it.

## September 16 2018

Number of authors in training set: 10

### 8:39pm 

Analysis parameters:
- Features: 9 feature-set, Complexity
- Classifiers: SMO

Result summary:

    Results:
    ========
    doc \ author   | _Unknown_      | BC             | JD             | JS             | MM             | RL             | RP             | RZ             | SM             | SP             | modern-good-writing |
    -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    ASAOE.txt      | 0.000000       | 0.054545       | 0.163636       | 0.181818 +     | 0.145455       | 0.090909       | 0.109091       | 0.036364       | 0.018182       | 0.127273       | 0.072727       |

Discussion: This isn't great. This was based on complexity, which is "Ratio of unique words to total number of words in the document." Obviously total number of words in documents is a terrible factor in our case.

### 8:52pm 

Features: WritePrints, Word Bigrams

Result summary:

    Results:
    ========
    doc \ author   | _Unknown_      | BC             | JD             | JS             | MM             | RL             | RP             | RZ             | SM             | SP             | modern-good-writing |
    -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    ASAOE.txt      | 0.000000       | 0.054545       | 0.163636       | 0.145455       | 0.127273       | 0.109091       | 0.090909       | 0.036364       | 0.018182       | 0.181818 +     | 0.072727       |

