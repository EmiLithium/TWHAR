# ReadMe for JStylo

The following is extracted and slightly distilled from the [PSAL website](https://psal.cs.drexel.edu/index.php/JStylo-Anonymouth).

## What is JSAN?

JSAN is a writing style analysis and anonymization framework. It consists of two parts:

1. JStylo - authorship attribution framework
1. Anonymouth - authorship evasion (anonymization) framework

JStylo is used as an underlying feature extraction and authorship attribution engine for Anonymouth, which uses the extracted stylometric features and classification results obtained through JStylo and suggests users changes to anonymize their writing style.

Details about JSAN: [Use Fewer Instances of the Letter "i": Toward Writing Style Anonymization.](https://www.cs.drexel.edu/~sa499/papers/anonymouth.pdf) Andrew McDonald, Sadia Afroz, Aylin Caliskan, Ariel Stolerman and Rachel Greenstadt. Privacy Enhancing Technologies Symposium (PETS 2012)

## Tutorial

JSAN tutorial: [Presented at 28c3](http://events.ccc.de/congress/2011/Fahrplan/attachments/2019_28C3-authorship.pdf) [video](http://www.youtube.com/watch?v=-b0Ta9h62_E)

## Download

Downloads:

* JStylo - Authorship attribution analysis tool:
	* JStylo v1.2
	* Includes JStylo and the Extended-Brennan-Greenstadt Adversarial Stylometry Corpus, the Brennan-Greenstadt Adversarial Stylometry Corpus and the Enron subcorpus detailed below.
* Corpora - includes corpora and problem set XML files suitable for JStylo, for the following:
	* The Extended-Brennan-Greenstadt Adversarial Stylometry Corpus (45 Authors, 6500 words per author minimum)
	* The Brennan-Greenstadt Adversarial Stylometry Corpus (12 Authors, 5000 words per author minimum)
	* A subcorpus of the [Enron email dataset](http://www.cs.cmu.edu/~enron/) (50 authors, 6500 words per author minimum)

If you use JStylo and/or Anonymouth in your research, please cite:

*Andrew McDonald, Sadia Afroz, Aylin Caliskan, Ariel Stolerman and Rachel Greenstadt. Use Fewer Instances of the Letter "i": Toward Writing Style Anonymization. PETS 2012.*

If you use the corpus in your research, please cite:

*Michael Brennan and Rachel Greenstadt. Practical Attacks Against Authorship Recognition Techniques in Proceedings of the Twenty-First Conference on Innovative Applications of Artificial Intelligence (IAAI), Pasadena, California, July 2009.*
