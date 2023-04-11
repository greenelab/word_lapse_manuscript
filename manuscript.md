---
title: Changing word meanings in biomedical literature reveal pandemics and new technologies
keywords:
- pubtator central
- preprints
- natural language-processing
- machine learning
- time series
- change point detection
lang: en-US
date-meta: '2023-04-11'
author-meta:
- David N. Nicholson
- Faisal Alquaddoomi
- Vincent Rubinetti
- Casey S. Greene
header-includes: |
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta property="og:type" content="article" />
  <meta name="dc.title" content="Changing word meanings in biomedical literature reveal pandemics and new technologies" />
  <meta name="citation_title" content="Changing word meanings in biomedical literature reveal pandemics and new technologies" />
  <meta property="og:title" content="Changing word meanings in biomedical literature reveal pandemics and new technologies" />
  <meta property="twitter:title" content="Changing word meanings in biomedical literature reveal pandemics and new technologies" />
  <meta name="dc.date" content="2023-04-11" />
  <meta name="citation_publication_date" content="2023-04-11" />
  <meta property="article:published_time" content="2023-04-11" />
  <meta name="dc.modified" content="2023-04-11T17:49:56+00:00" />
  <meta property="article:modified_time" content="2023-04-11T17:49:56+00:00" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="David N. Nicholson" />
  <meta name="citation_author_institution" content="Genomics and Computational Biology Program, University of Pennsylvania, Philadelpia, PA, USA" />
  <meta name="citation_author_orcid" content="0000-0003-0002-5761" />
  <meta name="twitter:creator" content="@dnicholson329" />
  <meta name="citation_author" content="Faisal Alquaddoomi" />
  <meta name="citation_author_institution" content="Department of Biomedical Informatics, University of Colorado School of Medicine, Aurora, CO, USA" />
  <meta name="citation_author_institution" content="Center for Health Artificial Intelligence (CHAI), University of Colorado School of Medicine, Aurora, CO, USA" />
  <meta name="citation_author_orcid" content="0000-0003-4297-8747" />
  <meta name="citation_author" content="Vincent Rubinetti" />
  <meta name="citation_author_institution" content="Department of Biomedical Informatics, University of Colorado School of Medicine, Aurora, CO, USA" />
  <meta name="citation_author_institution" content="Center for Health Artificial Intelligence (CHAI), University of Colorado School of Medicine, Aurora, CO, USA" />
  <meta name="citation_author" content="Casey S. Greene" />
  <meta name="citation_author_institution" content="Department of Biomedical Informatics, University of Colorado School of Medicine, Aurora, CO, USA" />
  <meta name="citation_author_institution" content="Center for Health Artificial Intelligence (CHAI), University of Colorado School of Medicine, Aurora, CO, USA" />
  <meta name="citation_author_orcid" content="0000-0001-8713-9213" />
  <meta name="twitter:creator" content="@greenescientist" />
  <link rel="canonical" href="https://greenelab.github.io/word_lapse_manuscript/" />
  <meta property="og:url" content="https://greenelab.github.io/word_lapse_manuscript/" />
  <meta property="twitter:url" content="https://greenelab.github.io/word_lapse_manuscript/" />
  <meta name="citation_fulltext_html_url" content="https://greenelab.github.io/word_lapse_manuscript/" />
  <meta name="citation_pdf_url" content="https://greenelab.github.io/word_lapse_manuscript/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://greenelab.github.io/word_lapse_manuscript/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://greenelab.github.io/word_lapse_manuscript/v/96d2b98fd59ebcef7499a0a8f0826617389588ce/" />
  <meta name="manubot_html_url_versioned" content="https://greenelab.github.io/word_lapse_manuscript/v/96d2b98fd59ebcef7499a0a8f0826617389588ce/" />
  <meta name="manubot_pdf_url_versioned" content="https://greenelab.github.io/word_lapse_manuscript/v/96d2b98fd59ebcef7499a0a8f0826617389588ce/manuscript.pdf" />
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
([permalink](https://greenelab.github.io/word_lapse_manuscript/v/96d2b98fd59ebcef7499a0a8f0826617389588ce/))
was automatically generated
from [greenelab/word_lapse_manuscript@96d2b98](https://github.com/greenelab/word_lapse_manuscript/tree/96d2b98fd59ebcef7499a0a8f0826617389588ce)
on April 11, 2023.
</em></small>



## Authors



+ **David N. Nicholson**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0003-0002-5761](https://orcid.org/0000-0003-0002-5761)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [danich1](https://github.com/danich1)
    · ![Twitter icon](images/twitter.svg){.inline_icon width=16 height=16}
    [dnicholson329](https://twitter.com/dnicholson329)
    <br>
  <small>
     Genomics and Computational Biology Program, University of Pennsylvania, Philadelpia, PA, USA
     · Funded by The Gordon and Betty Moore Foundation, GBMF4552; The National Human Genome Research Institute, R01 HG010067
  </small>

+ **Faisal Alquaddoomi**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0003-4297-8747](https://orcid.org/0000-0003-4297-8747)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [falquaddoomi](https://github.com/falquaddoomi)
    <br>
  <small>
     Department of Biomedical Informatics, University of Colorado School of Medicine, Aurora, CO, USA; Center for Health Artificial Intelligence (CHAI), University of Colorado School of Medicine, Aurora, CO, USA
     · Funded by The Gordon and Betty Moore Foundation, GBMF4552; The National Human Genome Research Institute, R01 HG010067
  </small>

+ **Vincent Rubinetti**
  <br>
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [vincerubinetti](https://github.com/vincerubinetti)
    <br>
  <small>
     Department of Biomedical Informatics, University of Colorado School of Medicine, Aurora, CO, USA; Center for Health Artificial Intelligence (CHAI), University of Colorado School of Medicine, Aurora, CO, USA
     · Funded by The Gordon and Betty Moore Foundation, GBMF4552; The National Human Genome Research Institute, R01 HG010067
  </small>

+ **Casey S. Greene**
  ^[✉](#correspondence)^<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0001-8713-9213](https://orcid.org/0000-0001-8713-9213)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [cgreene](https://github.com/cgreene)
    · ![Twitter icon](images/twitter.svg){.inline_icon width=16 height=16}
    [greenescientist](https://twitter.com/greenescientist)
    <br>
  <small>
     Department of Biomedical Informatics, University of Colorado School of Medicine, Aurora, CO, USA; Center for Health Artificial Intelligence (CHAI), University of Colorado School of Medicine, Aurora, CO, USA
     · Funded by The Gordon and Betty Moore Foundation, GBMF4552; The National Human Genome Research Institute, R01 HG010067
  </small>


::: {#correspondence}
✉ — Correspondence possible via [GitHub Issues](https://github.com/greenelab/word_lapse_manuscript/issues)
or email to
Casey S. Greene \<casey.s.greene@cuanschutz.edu\>.


:::


## Abstract {.page_break_before}

While we often think of words as having a fixed meaning that we use to describe a changing world, words are also dynamic and changing.
Scientific research can also be remarkably fast-moving, with new concepts or approaches rapidly gaining mind share.
We examined scientific writing, both preprint and pre-publication peer-reviewed text, to identify terms that have changed and examine their use.
One particular challenge that we faced was that the shift from closed to open access publishing meant that the size of available corpora changed by over an order of magnitude in the last two decades.
We developed an approach to evaluate semantic shift by accounting for both intra- and inter-year variability using multiple integrated models.
This analysis revealed thousands of change points in both corpora, including for terms such as 'cas9', 'pandemic', and 'sars'.
We found that the consistent change-points between pre-publication peer-reviewed and preprinted text are largely related to the COVID-19 pandemic.
We also created a web app for exploration that allows users to investigate individual terms (https://greenelab.github.io/word-lapse/).
To our knowledge, our research is the first to examine semantic shift in biomedical preprints and pre-publication peer-reviewed text, and provides a foundation for future work to understand how terms acquire new meanings and how peer review affects this process.

**Keywords**: Linguistic shift, pandemic, software, novelty


# Introduction

The meaning of words is constantly evolving.
For instance, the word "nice" used to mean foolish or innocent in the 15th-17th centuries, before it underwent a shift to its modern meaning of "pleasant or delightful" [@doi:10.1093/acrefore/9780199384655.013.323].
This change can be attributed to writers using new metaphors or substituting words with similar meanings, a process known as metonymy [@doi:10.1093/acrefore/9780199384655.013.323].
By studying these shifts, we can gain a more nuanced understanding of how language adapts to describe our world.

Scientific fields of inquiry are constantly evolving as researchers develop and test new hypotheses and applications.
For example, in the interval studied the CRISPR-Cas9 system has been repurposed as a tool for genome editing.
Microbes use this system as a defense against viruses, and scientists have adapted it for genome editing [@doi:10.1126/science.1225829], resulting in changes in the use of the term.
Written communication is an important part of science [@doi:10.1021/ci00050a001], both through published papers [@doi:10.1073/pnas.98.2.381] and preprints [@doi:10.1101/833400; @doi:10.1126/science.aay2933].
By using computational linguistics to analyze scientific manuscripts, we can identify longitudinal trends in scientific research.

The task of detecting changes in the meaning of words is known as semantic shift detection.
This process involves capturing word usage patterns, such as frequency and structure, over a set period of time [@arxiv:1806.03537].
Once captured, the final step is generating a time series to show potential shift events, commonly called changepoints [@arxiv:1806.03537; @arxiv:0710.3742; @gustafsson].
By using this approach, researchers have identified many changepoints within publicly available English corpora [@doi:10.1145/2736277.2741627; @doi:10.1109/JCDL.2014.6970173; @doi:10.1145/2064448.2064475; @doi:10.18653/v1/N18-1044; @doi:10.1017/S1351324918000220].
These discoveries included semantic changes like the meaning of awful shifting from majestic to horrible [@arxiv:1605.09096].
In addition to individual discoveries, scientists have identified global patterns that semantic shifts follow [@arxiv:1605.09096; @xu2015computational].
For instance, words with similar meanings, i.e., synonyms, tend to change over time and undergo similar changes [@xu2015computational].
Other patterns include that words change meaning inversely proportional to their frequency, and words with multiple meanings have higher rates of change [@arxiv:1605.09096].
Most of these discoveries have been made in regular English text.
However, researchers have also attempted to investigate whether these patterns are also found in biomedical literature [@doi:10.1016/j.ijmedinf.2017.11.006].
The only strong evidence they found is that words that change meaning do so inversely proportional to their usage frequency [@doi:10.18653/v1/W19-5037].
Despite conflicting evidence, it is clear that biomedical words and concepts change over time.

Recent studies have investigated semantic shifts in various non-biomedical corpora, such as newspapers [@doi:10.18653/v1/W17-2705; @arxiv:1711.05603; @doi:10.1017/S0003055417000570], books [@arxiv:1605.09096], Reddit [@doi:10.1016/j.jbi.2021.103824], and Twitter [@arxiv:1411.3315].
Other research has focused on semantic shifts in topics related to information retrieval [@doi:10.1007/s11192-018-2843-2], and the COVID-19 pandemic has been studied multiple times [@doi:10.1142/9789811232701_0011;@arxiv:2102.07836; @doi:10.2196/22635].
Additionally, researchers have examined how term usage related to drugs and diseases changes over time [@doi:10.18653/v1/W19-5037].
However, with the dramatic increase in open-access biomedical literature over the last two decades, there is an opportunity to analyze semantic shifts in biomedicine on a whole-literature scale.
This paper takes a deeper dive into this area by exploring semantic shifts in published and preprint works using natural language-processing and machine learning techniques.

We sought to identify semantic shifts in the rapidly growing body of open-access texts, published papers, and preprints.
To do this, we used a novel approach that integrates multiple models to account for the instability of machine learning models trained across various years.
This approach allowed us to identify changepoints for each token and to examine key cases.
We have made our research products, including changepoints and machine learning models, freely available as open licensed tools for the community.
In addition, we have created a web server that allows users to analyze tokens of interest and to observe the most similar terms within a year and temporal trends.


# Methods

## Biomedical Corpora Examined

### Pubtator Central

Pubtator Central is an open-access resource containing annotated abstracts and full-texts with entity recognition systems for biomedical concepts [@doi:10.1093/nar/gkz389].
The systens used were TaggerOne [@doi:10.1093/bioinformatics/btw343] to tag diseases, chemicals, and cell line entities, GNormPlus [@doi:10.1155/2015/918710] to tag genes, SR4GN [@doi:10.1371/journal.pone.0038460] to tag species, and tmVar [@doi:10.1093/bioinformatics/btx541] to tag genetic mutations.
We initially downloaded this resource on December 07th, 2021 and processed over 30 million documents.
This resource contains documents from the pre-1800s to 2021; however, due to the low sample size in the early years, we only used documents published from 2000 to 2021.
The resource was subsequently updated with documents from 2021.
We also downloaded a later version on March 09th, 2022 and merged both versions using each document's doc_id field to produce the corpus used in this analysis.
We divided documents by publication year and then preprocessed each using spacy's en_core_web_sm model [@spacy2].
We replaced each tagged word or phrase with its corresponding entity type and entity ID for every sentence that contained an annotation.
Then, we used spacy to break sentences into individual tokens and normalized each token to its root form via lemmatization.
After preprocessing, we used every sentence to train multiple Natural Language Processing (NLP) models designed to represent words based on their context.

### Biomedical Preprints

We downloaded a snapshot of BioRxiv [@doi:10.1101/833400] and MedRxiv [@doi:10.1126/science.aay2933] on March 4th, 2022, using their respective Amazon S3 buckets [@https://www.biorxiv.org/tdm; @https://www.medrxiv.org/tdm].
This snapshot contained 172,868 BioRxiv and 37,517 MedRxiv preprints.
We filtered each preprint to its most recent version to prevent duplication bias and sorted them into their respective posted year.
Unlike Pubtator Central, these filtered preprints did not contain any annotations.
Therefore, we used TaggerOne [@doi:10.1093/bioinformatics/btw343] to tag chemical and disease entities, and GNormplus [@doi:10.1155/2015/918710] to tag gene and species entities for our preprint set.
We then used spacy to preprocess every preprint as described in the Pubtator Central section.

## Constructing Word Embeddings for Semantic Change Detection

![
A. The first step of our data pipeline is where PMCOA papers and BioRxiv/MedRxiv preprints are binned by their respective posting year.
Following the binning process, we train ten word2vec models for each year's manuscripts.
B. Upon training each individual word2vec model, we align every model onto an anchor model.
C. We capture token differences using an intra-year and inter-year approach.
Each arrow indicates comparing all tokens from one model with their respective selves in a different model.
D. The last step combines the above calculations into a single metric to allow for a time series to be constructed.
Once constructed, we use a statistical technique to autodetect the presence of a changepoint.
](images/methods-pipeline/word-lapse-pipeline.png){#fig:pipeline_overview width="100%}

We used the Word2vec model [@arxiv:1301.3781] to construct word vectors for each year.
This model is a natural language processing model designed to represent words based on their respective neighbors  as dense vectors.
The skipgram model generates these vectors by having a shallow neural network predict a word's neighbors given the word, while the CBOW model predicts the word given its neighbors.
We used the CBOW model to construct word vectors for each year.
Despite the power of these word2vec models, these models are known to differ due to randomization within a year and year-to-year variability across years [@arxiv:1804.09692; @doi:10.1007/978-3-030-03991-2_73; @doi:10.1162/tacl_a_00008; @doi:10.18653/v1/S18-2019].
To control for run-to-run variability, we examined both intra-year and inter-year relationships.
We trained ten different CBOW models for each year using the following parameters: vector size of 300, 10 epochs, minimum frequency cutoff of 5, and a window size of 16 for abstracts (Figure {@fig:pipeline_overview}A).
Every model has its own unique vector space following training, making it difficult to compare two models without a correction step.
We then used orthogonal Procrustes [@doi:10.1007/BF02289451] to align all trained CBOW models for the Pubtator Central dataset to the first model trained in 2021, and all CBOW models for the BioRxiv/MedRxiv dataset to the first model trained in 2021 (Figure {@fig:pipeline_overview}B).
To visualize the aligned models, we used UMAP [@arxiv:1802.03426] with the cosine distance metric, a random_state of 100, 25 for n_neighbors, a minimum distance of 0.99, and 50 n_epochs.


## Detecting semantic changes across time

Once the word2vec models were aligned, the next step was to detect semantic change.
Semantic change events were detected through time series analysis [@doi:10.1145/2736277.2741627].
We constructed a time series sequence for each token by calculating its distance within a given year (intra-year) and across each year (inter-year) (Figure {@fig:pipeline_overview}C).
We used the model pairs constructed from the same year to calculate an intra-year distance, which was the cosine distance between each token and its corresponding counterpart.
The cosine distance is a metric bounded between 0 and 2, where a score of 0 indicates that two vectors are the same, and a score of 2 indicates that the two vectors are different.
For the inter-year distance, we used the Cartesian product of every model between two years and calculated the distance between tokens in the same way as the the intra-year distance.
We then combined both metrics by taking the ratio of the average inter-year distance over the average intra-year distance.
This approach penalizes tokens with high intra-year instability and rewards more stable tokens.
Additionally, it has been shown that including token frequency improves results compared to using distance alone [@doi:10.1007/s00799-019-00271-6].
We calculated token frequency as the ratio of token frequency in the more recent year over the frequency of the previous year.
Finally, we combined the frequency with the distance ratios to make the final metric (Figure {@fig:pipeline_overview}D).

Following time series construction, we performed change point detection, which uses statistical techniques to detect abnormalities within a given time series (Figure {@fig:pipeline_overview}D).
We used the CUSUM algorithm [@gustafsson], which uses a rolling sum of the differences between two timepoints and checks whether the sum is greater than a threshold.
A change point is considered to have occurred if the sum exceeds a threshold.
We used the 99th percentile on every generated timepoint as the threshold, and ran the CUSUM algorithm with a drift of 0 and default settings for all other parameters.


# Results

## Models can be aligned and compared within and between years

We examined how the usage of tokens in biomedical text changes over time using machine learning models.
We trained the models to predict the actual token given a portion of its surrounding tokens, and each token was represented as a vector in a coordinate space constructed by the models.

However, training these models is stochastic, resulting in arbitrary coordinate spaces.
Each model has its own unique coordinate space (Figure {@fig:word2vec_alignment}A), and each word is represented within that space (Figure {@fig:word2vec_alignment}B).
Model alignment is essential in allowing word2vec models to be compared [@doi:10.48550/arXiv.1605.09096; @doi:10.1038/s41597-021-01047-x].
Alignment projects every model onto a shared coordinate space (Figure {@fig:word2vec_alignment}C), enabling direct token comparison.
To enable comparison of the models, we aligned them onto a shared coordinate space.
We randomly selected 100 tokens to confirm that alignment worked as expected.
We found that tokens in the global space were more similar to themselves within the year than between years, while identical tokens in unaligned models were completely distinct (Figure {@fig:word2vec_alignment}D).
Local distances were unaffected by alignment, as token-neighbor distances remained unchanged (Figure {@fig:word2vec_alignment}D).

![
A. Without alignment, each word2vec model has its own coordinate space.
This is a UMAP visualization of 5000 randomly sampled tokens from 5 distinct Word2Vec models trained on the text published in 2010.
Each data point represents a token, and the color represents the respective Word2Vec model.
B. We greyed out all tokens except for the token 'probiotics' to highlight that each token appears in its own respective cluster without alignment.
C. After the alignment step, the token 'probiotics' is closer in vector space signifying that tokens can be easily compared.
D. In the global coordinate space, token distances appear to be vastly different when alignment is not applied.
After alignment, token distances become closer; tokens maintain similar distances with their neighbors regardless of alignment.
This boxplot shows the average distance of 100 randomly sampled tokens shared in every year from 2000 to 2021.
The x-axis shows the various groups being compared (tokens against themselves via intra-year and inter-year distances and tokens against their corresponding neighbors.
The y-axis shows the average distance for every year.
](https://raw.githubusercontent.com/danich1/biovectors/48913404aa889a381213ed44bd52e5927c66c51a/figure_generation/output/Figure_1.png){#fig:word2vec_alignment width="100%"}


The landscape of biomedical publishing has changed rapidly during the period of our dataset.
The texts for our analysis were open-access manuscripts available through PubMed Central.
The growth in the amount of available text and the uneven adoption of open-access publishing during the interval studied was expected to induce changes in the underlying machine learning models, making comparisons more difficult.
We found that the number of tokens available for model building, i.e., those in PMC OA, increased dramatically during this time (Figure {@fig:novel_distance_validation}A).
This was expected to create a pattern where models trained in earlier years were more variable than those from later years simply due to the limited sample size in early years.
To correct for this change in the underlying models, we developed a statistic that compared tokens' intra- and inter-year variabilities.

![
A. The number of tokens our models have trained on increases over time.
This line plot shows the number of unique tokens our various machine-learning models see.
The x-axis depicts the year, and the y-axis shows the token count.
B. Earlier years compared to 2010 have greater distances than later years.
This confidence interval plot shows the collective distances obtained by sampling 100 tokens present from every year using a single model approach.
The x-axis shows a given year, and the y-axis shows the distance metric.
C. Later years have a lower intra-distance variability compared to the earlier years.
This confidence interval plot shows the collective distances obtained by sampling 100 tokens present from every year using our multi-model approach.
The x-axis shows a given year, and the y-axis shows the distance metric.
](https://raw.githubusercontent.com/danich1/biovectors/48913404aa889a381213ed44bd52e5927c66c51a/figure_generation/output/Figure_2.png){#fig:novel_distance_validation width="100%"}

We expected most tokens to undergo minor changes from year to year, while substantial changes likely suggested model drift instead of true linguistic change.
We measured the extent to which tokens differed from themselves using the standard single-model approach and our integrated statistic.
We filtered the token list to only contain tokens present in every year and compared their distance to the midpoint year, 2010, using the single-model and integrated-models strategies.
The single-model approach showed that distances were larger in the earliest years than in later years (Figure {@fig:novel_distance_validation}B).
The integrated model approach did not display the same pattern (Figure {@fig:novel_distance_validation}C).
This suggests that training on smaller corpora leads to high variation and that an integrated model strategy is needed [@doi:10.1162/tacl_a_00008].
Therefore, we used the integrated-model strategy for the remainder of this work.

## Terms exhibit detectable changes in usage

![
A. The number of change points increases over time in PMCOA.
The x-axis shows the various time periods, while the y-axis depicts the number of detected changepoints.
B. Regarding preprints, the greatest number of change points was during 2018-2019.
The x-axis shows the various time periods, while the y-axis depicts the number of detected change points.
C. The token 'cas9' was detected to have a changepoint between 2012 and 2013.
The x-axis shows the time period since the first appearance of the token, and the y-axis shows the change metric.
D. 'sars' has two detected changepoints within the PMCOA corpus.
The x-axis shows the time period since the first appearance of the token, and the y-axis shows the change metric.
](https://raw.githubusercontent.com/danich1/biovectors/48913404aa889a381213ed44bd52e5927c66c51a/figure_generation/output/Figure_3.png){#fig:preprint_published_changepoints width="100%"}

We next sought to identify tokens that changed during the 2000-2021 interval for the text from PubMed Central's Open Access Corpus (PMCOA) and the 2015-2022 interval for our preprint corpus.
We applied the CUSUM algorithm with integrated-model distance to correct for systematic differences in the underlying corpora.
We found 41281 terms with a detected changepoint from PMCOA and 2266 terms from preprints (Figures {@fig:preprint_published_changepoints}A and {@fig:preprint_published_changepoints}B).
Most of our detected changepoints (38019 for PMCOA and 2260 for preprints) only had a single event.

We detected a changepoint in PMCOA for 'cas9' from 2012 to 2013 (Figure {@fig:preprint_published_changepoints}C).
Before the changepoint, its closest neighbors were related to genetic elements (e.g., 'cas'1-3).
After the changepoint, its closest neighbors became terms related to targeting, sgRNA, gRNA, and other genome editing strategies, such as 'talen' and 'zfns' (Table {@tbl:cas9_neighbor_table}).
We detected change points for 'SARS' from 2002 to 2003 and 2019 to 2020 (Figure {@fig:preprint_published_changepoints}D), consistent with the emergences of SARS-CoV [@doi:10.1046/j.1440-1843.2003.00517.x] and SARS-CoV-2 [@doi:10.1016/j.ijantimicag.2020.105924; @doi:10.1038/s41564-020-0695-z] as observed human pathogens.
Before each changepoint, the closest neighbors for 'SARS' were difficult to synthesize and summarize.
After changepoints, the neighbors for 'SARS' were consistent with the acronym for Severe Acute Respiratory Syndrome (Tables {@tbl:sars_neighbor_table_one} and {@tbl:sars_neighbor_table_two}).

We detected 200 tokens with at least one changepoint in each corpus.
Only 25 of the 200 terms were detected to have simultaneous changes between the preprint and PMCOA corpora.
We examined the overlap of detected change points between preprints and published articles.
Many of these 25 were related to the COVID-19 pandemic (Supplementary Table {@tbl:published_preprint_change_table}).
The complete set of detected change points is available for further analysis (see Data Availability and Software).


|2012    |2013        |
|--------|------------|
|cas2    |sgrna       |
|crispr1 |talen       |
|cas3    |spcas9      |
|cas1    |zfns        |
|cas10   |grna        |
|crispr3 |zfn         |
|tracrrna|dcas9       |
|crispr  |nickase     |
|csn1    |pcocas9     |
|crispr4 |crispr      |
|cas7    |sgrnas      |
|cas6e   |meganuclease|
|cas4    |tracrrna    |
|cse1    |crispri     |
|cas6    |crrna       |

Table: The fifteen most similar neighbors to the token 'cas9' for the years 2012 and 2013. {#tbl:cas9_neighbor_table}

2002                     |2003                                                                  |
|-------------------------|----------------------------------------------------------------------|
|qsar                     |species_227859                                                        |
|herbicidal               |mesh_c000657245                                                       |
|antiplasmodial           |severe acute respiratory syndrome-related coronavirus (species_694009)|
|arylpiperazine           |unidentified human coronavirus (species_694448)                       |
|a]pyridine               |SARS1 (gene_6301)                                                     |
|leishmanicidal           |ebola virus sp. (species_205488)                                      |
|naphthyridine            |pandemic                                                              |
|indolo[2,1               |coronavirus infections (mesh_d018352)                                 |
|b]quinazoline-6,12       |coronavirus                                                           |
|nematocidal              |ebola virus (species_1570291)                                         |
|f]isoxazolo[2,3          |severe acute respiratory syndrome (mesh_d045169)                      |
|5-(4                     |paramyxovirus                                                         |
|cholinephosphotransferase|viruse                                                                |
|oxovanadium(iv           |drosten                                                               |
|catecholase              |virologist                                                            |
Table: The fifteen most similar neighbors to the token 'sars' for the years 2002 and 2003. {#tbl:sars_neighbor_table_one}

|2019                     |2020                                                                  |
|-------------------------|----------------------------------------------------------------------|
|g.o.                     |sar                                                                   |
|nsp13                    |mers                                                                  |
|40/367                   |cov                                                                   |
|lissodendoryx            |sars-1                                                                |
|lutken                   |severe acute respiratory syndrome-related coronavirus (species_694009)|
|sarr                     |coronaviruse                                                          |
|sar                      |middle east respiratory syndrome-related coronavirus (species_1335626)|
|ophiura ophiura (species_72673)|cov.                                                                  |
|verrill                  |coronavirus infections (mesh_d018352)                                 |
|hirondelle               |mers-                                                                 |
|kobelt                   |covs                                                                  |
|azorean                  |severe acute respiratory syndrome coronavirus 2 (species_2697049)     |
|rusby                    |severe acute respiratory syndrome (mesh_d045169)                      |
|d'orbigny                |sarscov                                                               |
|psychropotes longicauda (species_55639)|sarscov-2                                                             |
Table: The fifteen most similar neighbors to the token 'sars' for the years 2019 and 2020. {#tbl:sars_neighbor_table_two}


## The word-lapse application is an online resource for the manual examination of biomedical tokens

![
A. The trajectory visualization of the token 'pandemic' through time.
It starts at the first mention of the token and progresses through each subsequent year.
Every data point shows the top five neighbors for the respective token.
B. The usage frequency of the token 'pandemic' through time.
The x-axis shows the year, and the y-axis shows the frequency for each token.
C. A word cloud visualization for the top 25 neighbors for the token 'pandemic' each year.
This visualization highlights each neighbor from a particular year and allows for the comparison between two years.
Tokens in purple are shared within both years, while tokens in red or blue are unique to their respective year.
](images/Figure_4.png){#fig:website_walkthrough width="100%"}

Our online application allows users to explore how token meanings change over time.
Users can input tokens as text strings, MeSH IDs, Entrez Gene IDs, or Taxonomy IDs.
For example, users might elect to explore the term 'pandemic', for which we detected a changepoint between 2019 and 2020.
The application also shows users the token's nearest neighbors through time (Figure {@fig:website_walkthrough}A).
When using 'pandemic' as an example, users can observe that 'epidemic' remains similar through time, but taxid:114727 (the H1N1 subtype of influenza) only entered the nearest neighbors with the swine flu pandemic in 2009 and MeSH:C000657245 (COVID-19) appeared in 2020.
Additionally, users can view a frequency chart displaying the token's usage each year (Figure {@fig:website_walkthrough}B), which can be displayed as a raw count or adjusted by the total size of the corpus.
Previously detected changepoints are indicated on this chart.
The final visualization shows the union of the nearest 25 neighbors from each year, ordered by the number of years it was present (Figure {@fig:website_walkthrough}C).
This visualization includes a comparison function.
All functionalities are supported across PMCOA and preprint corpora, and users can toggle between them.


# Discussion

Language is rapidly evolving, and the usage of words changes over time, with words assimilating new meanings or associations [@doi:10.1093/acrefore/9780199384655.013.323].
Some efforts have been made to study semantic change using biomedical text [@doi:10.1142/9789811232701_0011;@arxiv:2102.07836; @doi:10.2196/22635]; however, no such work has examined the changes evident in both pre-publication peer-reviewed and preprinted biomedical text.

We examined semantic changes in two open-access biomedical corpora, PubMed (PMCOA) and bioRxiv/MedRxiv, over a two-decade period from 2000 to 2022.
We developed a novel statistic that incorporated multiple Word2Vec models to examine semantic change over time.
We used orthogonal procrustes to align each model, and we found that the word vectors were closer together after alignment (Figure {@fig:word2vec_alignment}).
However, the best approach to align these models still remains to be determined [@doi:10.1007/978-3-030-32233-5_58].
As has been reported in previous studies [@doi:10.1162/tacl_a_00008; @doi:10.48550/arXiv.1804.09692], we found that without a correction step for the variability within and across years, it is difficult to compare stable and unstable models.
Our correction approach revealed that the average distances in the earlier years had less variability when using multiple models than when using a single model (Figure {@fig:novel_distance_validation}).

After correcting for year variability, our analysis revealed more than 41,000 change points, including tokens such as 'cas9', 'pandemic', and 'sars' (Figure {@fig:preprint_published_changepoints}).
Many of these change points overlapped between PMCOA and preprints, and were related to COVID-19 (Table {@tbl:published_preprint_change_table}).
This indicates that the COVID-19 pandemic has had a sufficiently strong impact on the biomedical literature to cause rapid semantic change across both publishing paradigms [@doi:10.1371/journal.pbio.3000959; @doi:10.1371/journal.pone.0240123].
To further investigate these change points, we have developed a web application that allows users to manually examine individual tokens.
However, approaches that can automatically validate these change points remain an essential area for future research.


# Conclusion

We uncovered changes in the meanings of words used in biomedical literature using a new approach that took variations between and within years into account.
Our approach identified 41,000 changepoints, including well-known terms such as 'cas9', 'pandemic' and 'sars'.
We created a web application that allows users to investigate these individual changepoints.
As a next step, it would be interesting to see if it is possible to detect the consistency and time-lag of semantic changes between preprints and published peer-reviewed texts.
This discovery could potentially be used to predict future changes within published texts.
Additionally, including other preprint databases may help to uncover consistencies across a wider range of disciplines, or within-field analyses may show the initial stages of semantic changes that will eventually spread throughout biomedicine.
Overall, this research is a starting point for understanding semantic changes in biomedical literature, and we are looking forward to seeing how this area develops over time.


# Availability of Data and Materials

An online version of this manuscript is available under a Creative Commons Attribution License at [https://greenelab.github.io/word_lapse_manuscript/](https://greenelab.github.io/word_lapse_manuscript/).
The source for the research portions of this project is licensed under the BSD-2-Clause Plus Patent at [https://github.com/greenelab/biovectors](https://github.com/greenelab/biovectors).
Our Word Lapse website can be found at [https://greenelab.github.io/word-lapse](https://greenelab.github.io/word-lapse), and the code for the website is available under a BSD-3 Clause at [https://github.com/greenelab/word-lapse](https://github.com/greenelab/word-lapse).
Full-text access for the bioRxiv repository is available at [https://www.biorxiv.org/tdm](https://www.biorxiv.org/tdm).
Full-text access for the medRxiv repository is available at [https://www.medrxiv.org/tdm](https://www.medrxiv.org/tdm).
Access to Pubtator Central's Open Access subset is available on NCBI's FTP server at [https://ftp.ncbi.nlm.nih.gov/pub/lu/PubTatorCentral/](https://ftp.ncbi.nlm.nih.gov/pub/lu/PubTatorCentral/).




# Funding Declaration

This work was supported by the Gordon and Betty Moore Foundation under award GBMF4552 and the National Institutes of Health's National Human Genome Research Institute under award R01 HG010067 to CSG.
The funders had no role in the study design, data collection, and analysis, decision to publish, or preparation of the manuscript.

# Acknowledgements

We used manubot-ai-editor [@doi:10.1101/2023.01.21.525030] to suggest revisions for this manuscript.
The version before any AI-based assistance is available at [this permanent link](https://greenelab.github.io/word_lapse_manuscript/v/e13e82b6d54d095a940a6238d60bc9cb38dc42d1/).


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>

## Supplemental Tables

|Token      |Changepoint|
|-----------|-----------|
|lockdown   |2019-2020  |
|2021       |2020-2021  |
|distancing |2019-2020  |
|2019       |2018-2019  |
|ace2       |2019-2020  |
|pandemic   |2019-2020  |
|2020       |2019-2020  |
|coronavirus|2019-2020  |
|bcl2a1     |2018-2019  |
|peak3      |2020-2021  |
|3.6.2      |2019-2020  |
|quarantine |2019-2020  |
|cobl       |2020-2021  |
|injectrode |2020-2021  |
|nrc3       |2020-2021  |
|4.0.5      |2020-2021  |
|TMPRSS2 (gene_7113)  |2019-2020  |
|n262       |2019-2020  |
|bin1       |2017-2018  |
|n3c        |2020-2021  |
|tip1       |2020-2021  |
|omicron    |2020-2021  |
|pangolin   |2019-2020  |
|adrn       |2020-2021  |
|seir       |2019-2020  |

Table: The intersection of changepoints found between published papers and preprints. {#tbl:published_preprint_change_table tag="S1"}


# Response to Reviewers

## Reviewer 1

>In this paper, the authors presented a method to examine the semantic shift in biomedical preprints and pre-publication by machine learning method. This work is very impressive and could have a great impact on the domain. However, the following questions should be addressed before publication.

>Q1: In this work, the author applied word2vec model to train the word embeddings. The main issue is that word2vec has a limited capability to capture contextual information. I would suggest the authors  try other more advanced language model, like BERT to train embeddings.

**At the time of this work, we found that Word2Vec was easier to interpret than BERT.
Given that true changepoints are unknown and the lack of a consensus gold standard, we decided to move forward with Word2Vec to benefit from the model's interpretability.
However, we agree that using BERT or related language models is an important area for future work.**

>Q2: How does the method take care of the new word issue? basically, if there’s a word created in this domain for only a few years and there are very few publications talking about it, then how the performance of this method would be?

**In the most technical sense, a new word could be detected as having a changepoint for any potential string of subsequent years in which the word appeared in both corpora.
However, we think that most new words are unlikely to be detected as they settle into initial use because most new words will occur relatively few times in the literature.
This would lead to high intra-year variability, reducing the likelihood of a discovered changepoint (this is the intent of our correction for intra-year variability between models).
The case where a new word would have detectable changepoints would be limited to those where the use is sufficiently common that its positioning can be estimated reliably and where its positioning changes between subsequent years. **


>Q3: When detecting semantic changes, the cosine distance was used for comparing similarities between words. This method seems too easy and not that robust. Are there any other good ways for detecting?

**New ways of detecting semantic change remain open for investigation.
However, most work that detects semantic changes uses cosine similarity (1-cosine distance).
We added the intra- and inter-year comparisons in part to improve the robustness of this metric, which is widely used within the field.
Due to this work being the first within biomedical literature, we adapted the commonly used metric, but we agree with the reviewer that future work should explore additional metrics.**

## Reviewer 2

>This paper develops a method to evaluate semantic shifts by calculating annual and interannual changes using multiple integrated models. This method achieves good results, but there are some shortcomings in the paper. There are some suggestions for revision.
>1.      The motivation is not clear. Please specify the importance of this paper.

**We have updated our introduction to make our motivation for this work more clear.
While we attempted to briefly paste the changes here, the introduction has changed so significantly that we recommend examining the new version.**

>2.      Please highlight the contributions of this paper.

**We have updated our introduction to make our contributions for this work more clear.
As above, the introduction has changed so substantially that it was less efficient to convey this by pasting specific paragraphs here than it is to refer to the new introduction itself.**

>3.      Most of references are out of date. Please discuss more recently published solutions, especially the solutions published in 2022.

**We have updated our introduction to include more recent publications that pertain to this work.**

>4.      In the method part, the authors’ description is not easy to understand. Have the authors considered using drawings to explain the method?

**We agree with the reviewer that this was a significant opportunity for improvement. 
We have updated our methods section to include a graphical depiction of our data pipeline, which is now Figure 1.**

>5.      When detecting semantic changes across time, the authors mention the use of Cartesian products in calculating interannual changes. What are the advantages of using Cartesian products for the task of this paper?

**The main advantage here is that the cartesian product lets us directly compute the inter-year distances.
Since we compute all possible combinations of model pairings, our sample size is sufficiently large enough to obtain reliable inter-year distance estimates for the years studied (noting that we removed pre-2000 literature due to the limited size of PubMed in these years).**


>6.      There is something unclear about Figure 1. There are five black dots in the second picture of Figure 1. What is the specific meaning of these five black dots? Please explain it to the author.

**We added a new figure (now referred to as Figure 1) to our manuscript that shows our entire data processing pipeline, and this step here refers to part B in our new figure.
To allow for direct comparison between word vectors, we need to have word2vec models aligned (part B in our new figure 1).
The black dots in the figure mentioned by the reviewer are the individual word vectors obtained from their corresponding word2vec model.
We greyed out all tokens except for the word vector: 'probiotics' to provide an individual example of what occurs when word2vec models aren't aligned.**

>7.      Figure 2 has some ambiguities. The authors use single model and multiple model to carry out experiments, and the experimental results are different. Other than using different models, what could be the reason for the difference?

**One reason for the differences is that our correction metric allows for different scales of differences.
Since we are taking a ratio of the inter-year distances over the intra-year distances, we encounter values that are greater than 0.
Ultimately, the point for figure 2 is to show that the confidence intervals are a lot smaller when variability is accounted for than not.**

>8.      For the proposed method, has the author considered applying it to the same type of task and achieving similar results as in this paper? Please explain it to the readers.

**We have thought of using this approach outside of biomedical literature.
However, we determined that this direction would be outside our paper's scope.
We mention this point as a future direction within our manuscript.**

>9.      More discussions of technical details should be given.

**We have updated our manuscript to provide additional discussion of the underlying technical details.**

## Reviewer 3

>•       The introduction is not clear and very less literature is used. Follow this instruction: The introduction should briefly place the study in a broad context and highlight why it is important. It should define the purpose of the work and its significance, including specific hypotheses being tested. The current state of the research field should be reviewed carefully, and key publications cited. Please highlight controversial and diverging hypotheses when necessary. Finally, briefly mention the main aim of the work and highlight the main conclusions. Keep the introduction comprehensible to scientists working outside the topic of the paper.
>•       In the introduction, what key theoretical perspectives and empirical findings in the main literature have already informed the problem formulation? What major, unaddressed puzzle, controversy, or paradox does this research address?

**We have updated our introduction to include more recent publications and discussion in relation to this work.**

>•       Authors should further clarify and elaborate novelty in their contribution.

**We have updated our introduction to make our contributions for this work more clear.
We attempted to provide a concise example of changes, but the changes were so extensive that it is more effective to simply point the reviewer to the new introduction.**

>•       What are the limitations of the present work?

**One limitation of this work is that changepoint validation can be challenging.
Due to this being the first time this work has been performed, there isn't an available widely-agreed upon gold standard set.
Our solution to circumvent this problem is that we provide a website that allows users to investigate our changepoint list further.**

## Reviewer 4

>This is a well-written manuscript to examine semantic shift in open access biomedical preprints and pre-publication peer-reviewed text. The methods are novel and  are clearly described. The results are clearly presented. It is a pleasure and very easy for audience to follow the paper. It adds to scientific value of the relative research field. I suggest acceptance.

**We appreciate the positive feedback from the reviewer.**

## Reviewer 5

>Dear authors,
>It is a pleasure to review your manuscript.

**We appreciate the positive feedback from the reviewer.**

>My suggestion:
>1. Thoroughly revise the manuscript.

**We have thoroughly revised our manuscript based on the feedback that was given by the other reviewers and based on an additional proof-read of our work.**

>2. Visit the Submission Guidelines and place your manuscript according to the journal's guidelines.
>Preparing main manuscript text
>Preparing illustrations and figures
>Preparing tables
>Preparing additional files

**We have examined the journal guidelines and updated formatting.**

>3. The figures must be well displayed, the text of the figures must be legible.

**We updated our figures to meet the journal's requirements.**

>4. The introduction has few quotes, it is very short.

**We have extended our introduction to include a more thorough discussion on previous work and highlight our contributions/motivation.
We now highlight related work both within and outside biomedicine.**

>5. The methodology is not well detailed, there is no figure that represents the pipeline.

**We have updated our methods section to include a graphical depiction of our data pipeline.**

## Reviewer 6

>Reviewer Comments
>Manuscript Number: Not Mentioned
>The topic is exciting and shows how the words are changing over time. However, the authors must consider the following comments to improve the manuscript's quality.
>
>1.      The authors can use a graphical representation of the proposed work.

**We have updated our methods section to include a graphical depiction of our data pipeline.**

>2.      The authors must explain how the methodology is unique.

**Our work is the first example where year variability has been accounted for within a word2vec model. 
The revised figure helps to demonstrate this approach, which previously was somewhat buried in the technical details of the methods section.**

>3.      The resolution of the Figures can be improved for better visibility.

**We updated our figures to meet the journal's requirements.**

>4.      The authors should discuss the computational complexity of the methods.

**As with work focused on training machine learning models, it is difficult to estimate this precisely.
Because we add inter- and intra-year variability, we note that the distance calculations scale with the square of the number of models used per year and the number of years examined (if all combinations are calculated, as they are for our manuscript to examine stability over time); however, more efficiency could be gained in subsequent work by only examining subsequent year pairs now that the statistic has been evaluated.**

>5.      Provide a separate discussion section that explains the complete details of the evaluation of the word meanings.

**We updated our discussion per the given feedback.
The changes are extensive enough that we refer the reviewer to our new Discussion section.**


>6.      Briefly details the reasons to consider few-year pairs such as (2002-2003), (2012-2013) and (2019-2020).

**These year pairs in particular, are the time points where a semantic change has occurred.
Within our paper, we mention the tokens associated with these time points.
For example, 2012-2013 is associated with the 'cas9' token, which signifies cas9 obtaining an association with genome editing.**

>7.      Verify the caption (title) for Table 3. (maybe 'The fifteen most similar neighbors to the token 'sars' for the years 2019 and 2020)

**We have updated our caption for this table.**
```diff
-Table: The fifteen most similar neighbors to the token 'sars' for the years 2002 and 2003. 
+Table: The fifteen most similar neighbors to the token 'sars' for the years 2019 and 2020. 
```

>8.      The authors should remove the citations from the Conclusion section.

**We have removed the citation from our conclusion section.
We also condensed the section with updates to the Discussion section. The conclusions section now reads:
> We uncovered semantic changes within biomedical literature using a novel approach that accounts for inter- and intra-year variability.
> Our approach found 41,000 changepoints that include well-known examples such as 'cas9', 'pandemic', and 'sars'.
> We constructed a web application that allows users to manually examine these individual changepoints.
> As an extension to this project, future work may be able to determine the consistency and time-lag of semantic change between preprint and pre-publication peer-reviewed text - potentially predicting future change in pre-publication peer-reviewed text.
> Furthermore, including other preprint repositories may reveal consistencies across a broader swath of fields, or within-field analyses may reveal the earliest starting points of semantic changes that ultimately sweep through biomedicine.
> Overall, this work is one starting point regarding semantic change within biomedical literature, and we are excited to see how this landscape will change as time progresses.**


>9.      Grammatical and spelling mistakes must be corrected.

**We have revised our manuscript overall to correct for errors and grammar mistakes.**

