# Results (running updates)

The writing samples are incomplete but let's just try it.

## September 17 2018 **HAPPY CONSTITUTION DAY AND WEEK!**

Added `drexel_1` and `enron_demo` authors as outgroups to the problem set.

- Feature set: WritePrints (Limited)
- Classifier(s): SMO

    Results:
    ========
    doc \ author   | _Unknown_      | BC             | JD             | JS             | MM             | RL             | RP             | RZ             | SM             | SP             | a              | allen-p        | arnold-j       | b              | bass-e         | beck-s         | c              | campbell-l     | cash-m         | cm             | d              | dasovich-j     | davis-d        | delainey-d     | dickson-s      | dorland-c      | e              | f              | farmer-d       | fossum-d       | g              | gay-r          | germany-c      | giron-d        | grigsby-m      | guzman-m       | h              | haedicke-m     | hain-m         | horton-s       | hyvl-d         | jones-t        | k              | kaminski-v     | kean-s         | kuykendall-t   | lavorato-j     | lenhart-m      | lokay-m        | love-p         | m              | mann-k         | mcconnell-m    | mclaughlin-e   | mims-thurston-p | modern-good-writing | neal-s         | nemec-g        | p              | pereira-s      | perlingiere-d  | rogers-b       | ruscitti-k     | s              | sager-e        | sanders-r      | scott-s        | shackleton-s   | shankman-j     | smith-m        | symes-k        | taylor-m       | tholt-j        | weldon-c       |
    --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    ASAOE.txt      | 0.000000       | 0.001111       | 0.017771       | 0.017401       | 0.019252       | 0.005553       | 0.002962       | 0.000740       | 0.000370       | 0.021103       | 0.024806       | 0.008145       | 0.017401       | 0.022954       | 0.005924       | 0.018882       | 0.019252       | 0.021844       | 0.011107       | 0.015550       | 0.025176       | 0.021474       | 0.011107       | 0.014439       | 0.007034       | 0.013328       | 0.026657       | 0.025546       | 0.004813       | 0.018141       | 0.027027 +     | 0.017771       | 0.007775       | 0.007405       | 0.008886       | 0.010367       | 0.023695       | 0.013328       | 0.020363       | 0.015180       | 0.021103       | 0.016660       | 0.025916       | 0.008515       | 0.022584       | 0.003702       | 0.011107       | 0.004073       | 0.004073       | 0.010367       | 0.026287       | 0.020363       | 0.015180       | 0.002592       | 0.012218       | 0.001481       | 0.006664       | 0.014809       | 0.024435       | 0.005183       | 0.002221       | 0.009256       | 0.011477       | 0.023695       | 0.006294       | 0.017031       | 0.019993       | 0.001851       | 0.013328       | 0.012218       | 0.003702       | 0.023695       | 0.016290       | 0.009996       |

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

