# SCATE
[SCATE (Smart Computer-Aided Translation Environment)](https://www.arts.kuleuven.be/ling/ccl/projects/scate) Corpus of Machine Translation Errors

This data repository contains an English-Dutch corpus of machine translations manually annotated with translation errors using the SCATE error taxonomy (Tezcan et al. 2017) . The English source texts were selected from the Dutch Parallel Corpus (Macken et al. 2011); the target texts were generated by three different MT systems.  

Data set | MT system | MT output obtained on | No. sentence pairs
--- | --- | --- | ---
SMT | Google Translate | 2014 | 2963
NMT | Google Translate | 2017 | 2963
RBMT | Systran<sup>1</sup> | 2014 | 698

![The SCATE MT error taxonomy](https://github.com/ardate/SCATE/blob/master/images/scate_taxonomy.png)

The annotations are stored in a tab-delimited format based on brat rapid annotation tool - [standoff format](http://brat.nlplab.org/standoff.html) and consists of three types of entries:
1. Error annotations:
   - ID (indicated with "T")
   - Main error category
   - Start offset of the text span
   - End offset of the text span
   - Annotated text
2. Sub-category of a given error annotation (if applicable):
   - ID (indicated with "A")
   - Parent error category
   - Parent error annotation ID 
   - Error category (sub-category)
3. Links between error annotations (if applicable):
   - ID (indicated with "R")
   - Link name
   - Linked error annotation ID (from)
   - Linked error annotation ID (to)

The files contain the following additional information besides the brat annotation information (as described above and in brat documentation):
* START-SEG: start of segment pair (source-target), with the ID of the segment pair
* START-OFFSET-SOURCE: start offset for the source sentence
* SRC: source sentence
* START-OFFSET-TARGET: start offset for the target sentence
* TRG: target sentence
* END-OFFSET: end offset for the target sentence
* END-SEG: end of segment pair

## Example entry
```
<START-SEG 6>
<START-OFFSET-SOURCE>962
<SRC>The mill in Fos-sur-Mer is the only exception.
<START-OFFSET-TARGET>1009
<TRG>De molen in Fos-sur-Mer is de enige uitzondering.
<END-OFFSET>1059
T22	Mistranslation_WordSense 966 970	mill
T43	Mistranslation_WordSense 1012 1017	molen
A25	Mistranslation_WordSense_subcat T22 Cont
A27	Mistranslation_WordSense_subcat T43 Cont
R9	MisTra_Sense Arg1:T22 Arg2:T43	
<END-SEG 6>
```



The data set is free to use for research purposes. Please cite the following paper if you use it in your research:
* Tezcan, A., Hoste, V., & Macken, L. (2017). SCATE taxonomy and corpus of machine translation errors . In G. C. Pastor & I. Durán-Muñoz (Eds.), Trends in E-tools and resources for translators and interpreters (Vol. 45, pp. 219–244). Brill | Rodopi.

Note 1: This version of the data set has been checked further for consistency of error annotations throughout the data-set and therefore contains additional error annotations than the version used in Tezcan et al. (2017) and Tezcan (2018).

Note 2: The NMT data-set has been annotated with an additional error category "Accuracy > Mistranslation > SemanticallyUnrelated". A subset of this NMT data-set with the additional error category has been analysed in Van Brussel et al. (2018).


<sup>1</sup> <sub><sup>Systran Enterprise Edition, version 7.5. All domains, dictionaries, translation choice les
and translation models were disabled prior to obtaining the MT output.</sup></sub>

## References 
* Tezcan, A., Hoste, V., & Macken, L. (2017). SCATE taxonomy and corpus of machine translation errors . In G. C. Pastor & I. Durán-Muñoz (Eds.), Trends in E-tools and resources for translators and interpreters (Vol. 45, pp. 219–244). Brill | Rodopi.
* Tezcan, A. (2018). Informative quality estimation of machine translation output. PhD Thesis.
* Van Brussel, L., Tezcan, A., & Macken, L. (2018). A fine-grained error analysis of NMT, PBMT and RBMT output for English-to-Dutch. In N. Calzolari, K. Choukri, C. Cieri, T. Declerck, S. Goggi, K. Hasida, H. Isahara, et al. (Eds.), Proceedings of the Eleventh International Conference on Language Resources and Evaluation (pp. 3799–3804). Presented at the Eleventh International Conference on Language Resources and Evaluation, Miyazaki, Japan: European Language Resources Association (ELRA).
* Paulussen, H., Macken, L., Vandeweghe, W., & Desmet, P. (2013). Dutch parallel corpus: a balanced parallel corpus for Dutch-English and Dutch-French. In P. Spyns & J. Odijk (Eds.), Essential speech and language technology for Dutch : results by the STEVIN-programme (pp. 185–199). Berlin, Germany: Springer.
Vancouver