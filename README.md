# SCATE
[SCATE (Smart Computer-Aided Translation Environment)](https://www.arts.kuleuven.be/ling/ccl/projects/scate) Corpus of Machine Translation Errors

This data repository contains source-target sentence pairs, for which the target sentences are obtained from different machine translation (MT) systems, and manual error annotations made using the SCATE error taxonomy.


Data set | MT system | MT output obtained on | No. sentence pairs
--- | --- | --- | ---
SMT | Google Translate | 2014 | 2963
NMT | Google Translate | 2017 | 2963
RBMT | Systran<sup>1</sup> | 2014 | 698

![The SCATE MT error taxonomy](https://github.com/ardate/SCATE/blob/master/images/scate_taxonomy.png)

The data format is based on brat rapid annotation tool - [standoff format](http://brat.nlplab.org/standoff.html). The txt files contain the same brat annotation structure (as described in brat documentation) and the following additional information:
* START-SEG: start of segment pair (source-target), with the ID of the segment pair
* START-OFFSET-SOURCE: start offset for the source sentence
* SRC: source sentence
* START-OFFSET-TARGET: start offset for the target sentence
* TRG: target sentence
* END-OFFSET: end offset for the target sentence
* END-SEG: end of segment pair


Please refer to the following studies for the details of the SCATE error taxonomy and annotation guidelines and consider citing them if you use this data set in your research:
* Tezcan, A., Hoste, V., & Macken, L. (2017). SCATE taxonomy and corpus of machine translation errors . In G. C. Pastor & I. Durán-Muñoz (Eds.), Trends in E-tools and resources for translators and interpreters (Vol. 45, pp. 219–244). Brill | Rodopi.
* Tezcan, A. (2018). Informative quality estimation of machine translation output. PhD Thesis.
* Van Brussel, L., Tezcan, A., & Macken, L. (2018). A fine-grained error analysis of NMT, PBMT and RBMT output for English-to-Dutch. In N. Calzolari, K. Choukri, C. Cieri, T. Declerck, S. Goggi, K. Hasida, H. Isahara, et al. (Eds.), Proceedings of the Eleventh International Conference on Language Resources and Evaluation (pp. 3799–3804). Presented at the Eleventh International Conference on Language Resources and Evaluation, Miyazaki, Japan: European Language Resources Association (ELRA).

Note 1: This version of the data set has been checked further for consistency of error annotations throughout the data-set and therefore contains additional error annotations than the version used in the above-mentioned studies.

Note 2: The NMT data-set has been annotated with an additional error category "Accuracy > Mistranslation > SemanticallyUnrelated". A subset of this NMT data-set with the additional error category has been analysed in Van Brussel et al. (2018).


<sup>1</sup> <sub><sup>Systran Enterprise Edition, version 7.5. All domains, dictionaries, translation choice les
and translation models were disabled prior to obtaining the MT output.</sup></sub>