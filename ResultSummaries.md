# Results (running updates)

The writing samples are incomplete but let's just try it.

## September 16 2018

END OF DAY SUMMARY: Ignore the 8:39pm analysis because the 9-feature set is heavily dependent on word counts per document, which is flawed for our conditions. The best one might be the 9:23pm one so far but the highest match is only 0.18 using the SMO (sequential minimal optimization) classifier. I think a good match would have been 0.25? Might have to email the creators to check that. Anyway, I definitely have to finish RL and then we'll only have 4 author sets left to populate!

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

Features: WritePrints (limited), Word Bigrams

Result summary:

    Results:
    ========
    doc \ author   | _Unknown_      | BC             | JD             | JS             | MM             | RL             | RP             | RZ             | SM             | SP             | modern-good-writing |
    -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    ASAOE.txt      | 0.000000       | 0.054545       | 0.163636       | 0.145455       | 0.127273       | 0.109091       | 0.090909       | 0.036364       | 0.018182       | 0.181818 +     | 0.072727       |

### 9:23

This one is based on word frequencies and not bigrams. And the WritePrint unlimited feature set. And it took a really long time.

Features: WritePrints, Words

Result summary:

    Results:
    ========
    doc \ author   | _Unknown_      | BC             | JD             | JS             | MM             | RL             | RP             | RZ             | SM             | SP             | modern-good-writing |
    -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    ASAOE.txt      | 0.000000       | 0.054545       | 0.145455       | 0.109091       | 0.127273       | 0.181818 +     | 0.090909       | 0.036364       | 0.018182       | 0.163636       | 0.072727       |

### 9:51pm

Okay I only just figured out that the feature set uses ALL the listed things.

Feature Set: `WritePrints (Limited)`

    Results:
    ========
    doc \ author   | _Unknown_      | BC             | JD             | JS             | MM             | RL             | RP             | RZ             | SM             | SP             | modern-good-writing |
    -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    ASAOE.txt      | 0.000000       | 0.054545       | 0.163636       | 0.145455       | 0.109091       | 0.127273       | 0.090909       | 0.036364       | 0.018182       | 0.181818 +     | 0.072727       |

