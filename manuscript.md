---
title: Detecting semantic shifts in biomedical literature through an intra-year and inter-year approach
keywords:
- pubtator-central
- preprints
- natural-language-processing
- machine-learning
- time-series
- changepoint-detection
lang: en-US
date-meta: '2022-05-31'
author-meta:
- David Nicholson
- Faisal Alquaddoomi
- Vincent Rubinetti
- Casey S. Greene
header-includes: |-
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta name="dc.title" content="Detecting semantic shifts in biomedical literature through an intra-year and inter-year approach" />
  <meta name="citation_title" content="Detecting semantic shifts in biomedical literature through an intra-year and inter-year approach" />
  <meta property="og:title" content="Detecting semantic shifts in biomedical literature through an intra-year and inter-year approach" />
  <meta property="twitter:title" content="Detecting semantic shifts in biomedical literature through an intra-year and inter-year approach" />
  <meta name="dc.date" content="2022-05-31" />
  <meta name="citation_publication_date" content="2022-05-31" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="David Nicholson" />
  <meta name="citation_author_institution" content="Genomics and Computational Biology" />
  <meta name="citation_author_orcid" content="0000-0003-0002-5761" />
  <meta name="twitter:creator" content="@dnicholson329" />
  <meta name="citation_author" content="Faisal Alquaddoomi" />
  <meta name="citation_author_institution" content="Center for Health Artificial Intellegence (CHAI)" />
  <meta name="citation_author_orcid" content="XXXX-XXXX-XXXX-XXXX" />
  <meta name="citation_author" content="Vincent Rubinetti" />
  <meta name="citation_author_institution" content="Center for Health Artificial Intellegence (CHAI)" />
  <meta name="citation_author_orcid" content="XXXX-XXXX-XXXX-XXXX" />
  <meta name="citation_author" content="Casey S. Greene" />
  <meta name="citation_author_institution" content="Department of Something, University of Whatever" />
  <meta name="citation_author_institution" content="Department of Whatever, University of Something" />
  <meta name="citation_author_orcid" content="XXXX-XXXX-XXXX-XXXX" />
  <link rel="canonical" href="https://greenelab.github.io/word_lapse_manuscript/" />
  <meta property="og:url" content="https://greenelab.github.io/word_lapse_manuscript/" />
  <meta property="twitter:url" content="https://greenelab.github.io/word_lapse_manuscript/" />
  <meta name="citation_fulltext_html_url" content="https://greenelab.github.io/word_lapse_manuscript/" />
  <meta name="citation_pdf_url" content="https://greenelab.github.io/word_lapse_manuscript/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://greenelab.github.io/word_lapse_manuscript/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://greenelab.github.io/word_lapse_manuscript/v/9b53e4620c0ed1a6b42495a9cf2111d6bc10217f/" />
  <meta name="manubot_html_url_versioned" content="https://greenelab.github.io/word_lapse_manuscript/v/9b53e4620c0ed1a6b42495a9cf2111d6bc10217f/" />
  <meta name="manubot_pdf_url_versioned" content="https://greenelab.github.io/word_lapse_manuscript/v/9b53e4620c0ed1a6b42495a9cf2111d6bc10217f/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...






<small><em>
This manuscript
([permalink](https://greenelab.github.io/word_lapse_manuscript/v/9b53e4620c0ed1a6b42495a9cf2111d6bc10217f/))
was automatically generated
from [greenelab/word_lapse_manuscript@9b53e46](https://github.com/greenelab/word_lapse_manuscript/tree/9b53e4620c0ed1a6b42495a9cf2111d6bc10217f)
on May 31, 2022.
</em></small>

## Authors



+ **David Nicholson**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0003-0002-5761](https://orcid.org/0000-0003-0002-5761)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [danich1](https://github.com/danich1)
    · ![Twitter icon](images/twitter.svg){.inline_icon width=16 height=16}
    [dnicholson329](https://twitter.com/dnicholson329)<br>
  <small>
     Genomics and Computational Biology
     · Funded by Grant XXXXXXXX
  </small>

+ **Faisal Alquaddoomi**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [janeroe](https://github.com/janeroe)<br>
  <small>
     Center for Health Artificial Intellegence (CHAI)
  </small>

+ **Vincent Rubinetti**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [janeroe](https://github.com/janeroe)<br>
  <small>
     Center for Health Artificial Intellegence (CHAI)
  </small>

+ **Casey S. Greene**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [cgreene](https://github.com/cgreene)<br>
  <small>
     Department of Something, University of Whatever; Department of Whatever, University of Something
  </small>



## Abstract {.page_break_before}




# Introduction

Language is constantly evolving, and the meaning that we ascribe to words changes over time. 
For example, the word "nice" was used to mean foolish or innocent back in the 15th-17th century; then, it underwent a positive shift to its current meaning of "pleasant or delightful"[@doi:10.1093/acrefore/9780199384655.013.323]. 
These shifts occur for many reasons.
For example, writers may use new metaphors or substitute words for others with similar meanings in a process known as metonymy [@doi:10.1093/acrefore/9780199384655.013.323]. 
Studying these shifts can provide a nuanced understanding of how language adapts to describe our world.

Scientific fields of inquiry also change, sometimes rapidly, as researchers devise and test new hypotheses and applications.
For example, the repurposing of the CRISPR-Cas9 system to a pervasive tool for genome editing has altered how we discuss molecular entities.
Microbes use this as an immune system to defend against viruses.
Scientists repurposed this system for genome editing [@doi:10.1126/science.1225829], leading to changes in the use of the term.
Science is a field with substantial written communication [@doi:10.1021/ci00050a001], both via published papers [@doi:10.1073/pnas.98.2.381] and preprints [@doi:10.1101/833400; @doi:10.1126/science.aay2933].
Examining scientific manuscripts with computational linguistics can reveal longitudinal trends in scientific research.

Studying changes in the use of word meanings is called semantic shift detection.
Approaches for semantic shift detection examine time series datasets that capture word usage patterns, both with respect to frequency and structure.
Typically, these time series are generated for individual words by training a unique model on text binned by a selected time period [@arxiv:1605.09096; @arxiv:1606.0282; @doi:10.18653/v1/N18-1044].
<!--Following time series generation, the next step is to align models to enable comparison [@arxiv:1411.3315].
A common technique for alignment is Orthogonal Procrustes [@doi:10.1007/BF02289451], but other ways to perform alignment have been used [@arxiv:1702.08359; @arxiv:1703.00607].-->
Methods are then applied to identify "changepoints" where a word's meaning has changed [@arxiv:0710.3742,@gustafsson].

Semantic shifts have been examined in many sources. 
Analysis has included newspapers [@doi:10.18653/v1/W17-2705; @arxiv:1711.05603;@doi:10.1017/S0003055417000570], books [@arxiv:1605.09096], reddit [@arxiv:1606.0282], and Twitter [@arxiv:1411.3315].
Researchers have examined topics in information retrieval [@doi:10.1007/s11192-018-2843-2], and in biomedicine COVID-19 has been examined multiple times [@doi:10.1142/9789811232701_0011,@arxiv:2102.07836].
The amount of open access biomedical literature has dramatically increased in the last two decades, laying the groundwork for the large-scale analysis of semantic shifts in biomedicine.

We examine these semantic shifts in this rapidly growing body of open access text.
We include both published papers and preprints in our analysis.
We found that novel strategies integrating multiple models for each year sidestepped the challenge of instability in the machine learning models and allowed us to estimate intra- and inter-year variability.
We identify semantic changepoints for each token.
We examine key cases and provide the full set of research products, including changepoints and machine learning models, as openly licensed tools for the community.
We also created a webserver that allows users to analyze tokens of interest on the fly, examining both the most similar terms within a year and temporal trends.




# Methods

## Biomedical Corpora Examined

### Pubtator Central

Pubtator Central is an open-access resource containing annotated abstracts and full-text annotated with entity recognition systems for biomedical concepts [@doi:10.1093/nar/gkz389].
The methods used are TaggerOne [@doi:10.1093/bioinformatics/btw343] to tag diseases, chemicals, and cell line entities, GNormPlus [@doi:10.1155/2015/918710] to tag 
genes, SR4GN [@doi:10.1371/journal.pone.0038460] to tag species, and tmVar [@doi:10.1093/bioinformatics/btx541] to tag genetic mutations.
We initially downloaded this resource on December 07th, 2021, and processed over 30 million documents.
This resource contains documents that date back to the pre-1800s to the year 2021; however, due to the low sample size in early years, we only used documents published from 2000 to 2021.
The resource was subsequently updated with documents from 2021. 
We also downloaded a later version on March 09th, 2022, and merged both versions using each document's doc_id field to produce the corpus used in this analysis.
We divided documents by publication year and then preprocessed each using spacy's en_core_web_sm model [@spacy2].
We replaced each tagged word or phrase with its corresponding entity type and entity id for every sentence that contained an annotation.
Then, we used spacy to break sentences into individual tokens and normalized each token to its root form via lemmatization.
After preprocessing, we used every sentence to train multiple natural language models designed to represent words based on their context.

### Biomedical Preprints

BioRxiv [@doi:10.1101/833400] and MedRxiv [@doi:10.1126/science.aay2933] are repositories that contain preprints for the life science community.
MedRxiv mainly focuses on preprints that mention patient research, while bioRxiv focuses on general biology.
We downloaded a snapshot of both resources on March 4th, 2022, using their respective Amazon S3 bucket [@https://www.biorxiv.org/tdm; @https://www.medrxiv.org/tdm].
This snapshot contained 172,868 BioRxiv preprints and 37,517 MedRxiv preprints.
These resources allow authors to post multiple versions of a single preprint.
To prevent duplication bias, we filtered every preprint to its most recent version and sorted each preprint into its respective posted year.
Unlike Pubtator Central, these filtered preprints do not contain any annotations.
Therefore, we used TaggerOne [@doi:10.1093/bioinformatics/btw343] to tag every chemical and disease entity and GNormplus [@doi:10.1155/2015/918710] to tag every gene and species entity for our preprint set.
Once tagged, we used spacy to preprocess every preprint as described in our Pubtator Central section.

## Constructing Word Embeddings for Semantic Change Detection

Word2vec [@arxiv:1301.3781] is a natural language processing model designed to model words based on their respective neighbors in the form of dense vectors.
This suite of models comes in two forms, a skipgram model and a continuous bags of words (CBOW) model.
The skipgram model generates these vectors by having a shallow neural network predict a word's neighbors given the word, while the CBOW model predicts the word given its neighbors.
We used the CBOW model to construct word vectors for each year.
Despite the power of these word2vec models, these models are known to differ both due to randomization within year and year-to-year variability across years [@arxiv:1804.09692; @doi:10.1007/978-3-030-03991-2_73; @doi:10.1162/tacl_a_00008; @doi:10.18653/v1/S18-2019].
To control for run-to-run variability, we examined both intra-year and inter-year relationships.
Each year, we trained ten different CBOW models using the following parameters: vector size of 300, 10 epochs, minimum frequency cutoff of 5, and a window size of 16 for abstracts.
Every model has its own unique vector space following training, making it difficult to compare two models without a correction step.
We used orthogonal Procrustes [@doi:10.1007/BF02289451] to align models.
We aligned all trained CBOW models for the Pubtator Central dataset to the first model trained in 2021.
Likewise, we aligned all CBOW models for the BioRxiv/MedRxiv dataset to the first model trained in 2021.
We used UMAP [@arxiv:1802.03426] to visually examine the aligned models.
We trained this model using the following parameters: cosine distance metric, random_state of 100, 25 for n_neighbors, a minimum distance of 0.99, and 50 n_epochs.

## Detecting semantic changes across time

Once word2vec models are aligned, the next step is to detect semantic change.  
Semantic change events are often detected through time series analysis  [@doi:10.1145/2736277.2741627].
We constructed a time series sequence for every token by calculating its distance within a given year (intra-year) and across each year (inter-year).
We used the model pairs constructed from the same year to calculate an intra-year distance.
Then, we calculated the cosine distance between each token and its corresponding counterpart for every generated pair. 
Cosine distance is a metric bounded between zero and two, where a score of zero means two vectors are the same, and a score of two means both vectors are different.
For the inter-year distance, we used the Cartesian product of every model between two years and calculated the distance between tokens in the same way as the intra-year distance.
Following both calculations, we combined both metrics by taking the ratio of the average inter-year distance over the average intra-year distance.
Through this approach, tokens with high intra-year instability will be penalized and vice-verse for more stable tokens.
Along with token distance calculations, it has been shown that including token frequency improves results compared to using distance alone [@doi:10.1007/s00799-019-00271-6].
We calculated token frequency as the ratio of token frequency in the more recent year over the frequency of the previous year. 
Then, we combined both the frequency and distance ratios to make the final metric.

Following time series construction, we performed change point detection, which is a process that uses statistical techniques to detect abnormalities within a given time series.
We used the CUSUM algorithm [@gustafsson] to detect these abnormalities.
This algorithm uses a rolling sum of the differences between two timepoints and checks whether the sum is greater than a threshold.
A changepoint is considered to have occurred if the sum is greater than a threshold.
We used the 99th percentile on every generated timepoint as the threshold.
Then, we ran the CUSUM algorithm using a drift of 0 and default settings for all other parameters.



# Results
<div style="color:red">
One potential results panel: comparing results with abstract and full text (since you say above full text is not so often used).
</div>

1. Figure 1 - Visual to show that alignment works along intra year variation (Procrustes Validation)
  1. Umap panel for an individual year to show models are separated
  <div style="color:red">
  I would start with the simplest possible way that you can show things, and only bring in more complexity like UMAP when necessary. I'm guessing that you would be able to show this with just PCA or similar, unless I'm not thinking correctly.
  </div>
  2. Umap panel to show the same year after models have been aligned
  3. Umap panel to show across years (inter-year varation)
  	  1. might not have this as a figure given the aligned umap results, but we shall see 
2. Figure 2 - CUSUM validation
	<div style="color:red">
	I think you might want another figure here that shows how you can use the variability in distance to address the challenges of variable training set size / model uncertainty. Let's see how things shake out as you're writing.
	</div>
  1. Table of found timepoint changes using this algorithm
  2. Highlight pandemic as positive control
  3. Nearest Neighbors upset plot ^^
  4. Might look into lung cancer or other form of cancer results
4. Figure 3 - Website walkthrough for the work done here
  1. Website screenshots
  <div style="color:red">
  The figures that make up the website might be nice to show/explain individually - not as screenshots but as actual figures (remember the PLOS situation where using a screenshot was an issue we had to work through).
  </div>
  2. Basically a walkthrough of the website and how a user can operate the web resource (similar to preprint similarity search)



# Discussion and Conclusion

1. We provided a website resource to allow users to see toekn association changes
2. Word2vec is unstable and we implemented an approach to account for that variation
3. Constructs groundwork for future research into token changes
4. Will implement biorxiv and other preprint resources as a next step.


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
