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
date-meta: '2023-04-05'
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
  <meta name="dc.date" content="2023-04-05" />
  <meta name="citation_publication_date" content="2023-04-05" />
  <meta property="article:published_time" content="2023-04-05" />
  <meta name="dc.modified" content="2023-04-05T14:32:05+00:00" />
  <meta property="article:modified_time" content="2023-04-05T14:32:05+00:00" />
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
  <link rel="alternate" type="text/html" href="https://greenelab.github.io/word_lapse_manuscript/v/46067118a85d60e14386fbca676d10d511d5fb4c/" />
  <meta name="manubot_html_url_versioned" content="https://greenelab.github.io/word_lapse_manuscript/v/46067118a85d60e14386fbca676d10d511d5fb4c/" />
  <meta name="manubot_pdf_url_versioned" content="https://greenelab.github.io/word_lapse_manuscript/v/46067118a85d60e14386fbca676d10d511d5fb4c/manuscript.pdf" />
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
([permalink](https://greenelab.github.io/word_lapse_manuscript/v/46067118a85d60e14386fbca676d10d511d5fb4c/))
was automatically generated
from [greenelab/word_lapse_manuscript@4606711](https://github.com/greenelab/word_lapse_manuscript/tree/46067118a85d60e14386fbca676d10d511d5fb4c)
on April 5, 2023.
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
Using this strategy and examining year-by-year changes revealed thousands of change points in both corpora.
We found change points for tokens including 'cas9', 'pandemic', and 'sars' among many others.
The consistent change-points between pre-publication peer-reviewed and preprinted text were largely related to the COVID-19 pandemic.
We developed a web app for exploration (https://greenelab.github.io/word-lapse/) that enables users to investigate individual terms.
To our knowledge, this analysis is the first to examine semantic shift in biomedical preprints and pre-publication peer-reviewed text, and it lays the foundation for future work to examine how terms acquire new meaning and the extent to which that process is encouraged or discouraged by peer review.

**Keywords**: Linguistic shift, pandemic, software, novelty


# Introduction

Language constantly evolves, and the meaning we ascribe to words changes over time.
The word "nice" was used to mean foolish or innocent back in the 15th-17th century; then, it underwent a positive shift to its current meaning of "pleasant or delightful"[@doi:10.1093/acrefore/9780199384655.013.323].
These shifts occur for many reasons.
For example, writers may use new metaphors or substitute words for others with similar meanings in a process known as metonymy [@doi:10.1093/acrefore/9780199384655.013.323].
Studying these shifts can provide a nuanced understanding of how language adapts to describe our world.

Scientific fields of inquiry also change, sometimes rapidly, as researchers devise and test new hypotheses and applications.
For example, repurposing the CRISPR-Cas9 system to a pervasive tool for genome editing has altered how we discuss molecular entities.
Microbes use this as an immune system to defend against viruses.
Scientists repurposed this system for genome editing [@doi:10.1126/science.1225829], leading to changes in the use of the term.
Science is a field with substantial written communication [@doi:10.1021/ci00050a001], both via published papers [@doi:10.1073/pnas.98.2.381] and preprints [@doi:10.1101/833400; @doi:10.1126/science.aay2933].
Examining scientific manuscripts with computational linguistics can reveal longitudinal trends in scientific research.

The task of examining if words change their meanings is called semantic shift detection.
This process involves capturing word usage patterns such as frequency and structure over a set period of time [@arxiv:1806.03537].
Once these patterns have been captured, the last step is generating a time series showing possible shift events, commonly called changepoints [@arxiv:1806.03537;@arxiv:0710.3742,@gustafsson].
Scientists have used this approach to discover many changepoints within publically available English corpora [@doi:10.1145/2736277.2741627; @doi:10.1109/JCDL.2014.6970173; @doi:10.1145/2064448.2064475; @doi:10.18653/v1/N18-1044; @doi:10.1017/S1351324918000220].
These discoveries included semantic changes like the meaning of awful shifting from majestic to horrible [@arxiv:1605.09096].
Along with individual discoveries, scientists have identified global patterns that semantic shifts can follow [@arxiv:1605.09096; @xu2015computational].
One pattern discovered is that words with similar meanings, i.e., synonyms, tend to change over time and undergo similar changes [@xu2015computational].
The other patterns are that words undergo semantic shifts inversely proportional to their frequency, and words with multiple meanings will have higher rates of change [@arxiv:1605.09096].
The majority of these discoveries have been within regular English text.
There has been an effort to investigate if any of these patterns are upheld within biomedical literature [@doi:10.1016/j.ijmedinf.2017.11.006].
The researchers only found strong evidence of words that change meaning inversely scales to their usage frequency [@doi:10.18653/v1/W19-5037].
Despite the conflicting evidence for these change patterns, biomedical words and concepts change over time.

Most recent work to detect semantic shifts has been outside of biomedical corpora.
Common mediums include newspapers [@doi:10.18653/v1/W17-2705; @arxiv:1711.05603; @doi:10.1017/S0003055417000570], books [@arxiv:1605.09096], reddit [@doi:10.1016/j.jbi.2021.103824], and Twitter [@arxiv:1411.3315].
Researchers have examined topics in information retrieval [@doi:10.1007/s11192-018-2843-2], and in biomedicine COVID-19 has been examined multiple times [@doi:10.1142/9789811232701_0011;@arxiv:2102.07836; @doi:10.2196/22635].
Also, researchers have examined how drugs and disease pairs changed in their usage over time [@doi:10.18653/v1/W19-5037].
Despite these discoveries, the amount of open-access biomedical literature has dramatically increased in the last two decades, laying the groundwork for the large-scale analysis of semantic shifts in biomedicine.
There remains a gap in uncovering semantic change on a global scale within published and preprint works
and this work takes a deeper dive.

To fill this gap, we sought to uncover instances of semantic shifts within the rapidly growing body of open-access texts, published papers, and preprints.
We took a novel approach that integrates multiple models to account for the challenge of instability in the machine learning models trained across various years.
Using this approach, we identified semantic changepoints for each token and examine key changepoint cases.
We provided the full set of research products, including changepoints and machine learning models, as openly licensed tools for the community.
Lastly, we created a web server that allows users to analyze tokens of interest on the fly with respect to the most similar terms within a year and temporal trends.


# Methods

## Biomedical Corpora Examined

### Pubtator Central

Pubtator Central is an open-access resource containing annotated abstracts and full-text annotated with entity recognition systems for biomedical concepts [@doi:10.1093/nar/gkz389].
The methods used are TaggerOne [@doi:10.1093/bioinformatics/btw343] to tag diseases, chemicals, and cell line entities, GNormPlus [@doi:10.1155/2015/918710] to tag 
genes, SR4GN [@doi:10.1371/journal.pone.0038460] to tag species, and tmVar [@doi:10.1093/bioinformatics/btx541] to tag genetic mutations.
We initially downloaded this resource on December 07th, 2021, and processed over 30 million documents.
This resource contains documents from the pre-1800s to 2021; however, due to the low sample size in the early years, we only used documents published from 2000 to 2021.
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
We filtered every preprint to its most recent version to prevent duplication bias and sorted each preprint into its respective posted year.
Unlike Pubtator Central, these filtered preprints do not contain any annotations.
Therefore, we used TaggerOne [@doi:10.1093/bioinformatics/btw343] to tag every chemical and disease entity and GNormplus [@doi:10.1155/2015/918710] to tag every gene and species entity for our preprint set.
Once tagged, we used spacy to preprocess every preprint as described in our Pubtator Central section.

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

Word2vec [@arxiv:1301.3781] is a natural language processing model designed to model words based on their respective neighbors in the form of dense vectors.
This suite of models comes in two forms, a skipgram model and a continuous bags of words (CBOW) model.
The skipgram model generates these vectors by having a shallow neural network predict a word's neighbors given the word, while the CBOW model predicts the word given its neighbors.
We used the CBOW model to construct word vectors for each year.
Despite the power of these word2vec models, these models are known to differ due to randomization within a year and year-to-year variability across years [@arxiv:1804.09692; @doi:10.1007/978-3-030-03991-2_73; @doi:10.1162/tacl_a_00008; @doi:10.18653/v1/S18-2019].
To control for run-to-run variability, we examined both intra-year and inter-year relationships.
Each year, we trained ten different CBOW models using the following parameters: vector size of 300, 10 epochs, minimum frequency cutoff of 5, and a window size of 16 for abstracts (Figure {@fig:pipeline_overview}A).
Every model has its own unique vector space following training, making it difficult to compare two models without a correction step.
We used orthogonal Procrustes [@doi:10.1007/BF02289451] to align models (Figure {@fig:pipeline_overview}B).
We aligned all trained CBOW models for the Pubtator Central dataset to the first model trained in 2021.
Likewise, we aligned all CBOW models for the BioRxiv/MedRxiv dataset to the first model trained in 2021.
We used UMAP [@arxiv:1802.03426] to visually examine the aligned models.
We trained this model using the following parameters: cosine distance metric, random_state of 100, 25 for n_neighbors, a minimum distance of 0.99, and 50 n_epochs.

## Detecting semantic changes across time

Once word2vec models are aligned, the next step is to detect semantic change.  
Semantic change events are often detected through time series analysis  [@doi:10.1145/2736277.2741627].
We constructed a time series sequence for every token by calculating its distance within a given year (intra-year) and across each year (inter-year) (Figure {@fig:pipeline_overview}C).
We used the model pairs constructed from the same year to calculate an intra-year distance.
Then, we calculated the cosine distance between each token and its corresponding counterpart for every generated pair. 
Cosine distance is a metric bounded between zero and two, where a score of zero means two vectors are the same, and a score of two means both vectors are different.
For the inter-year distance, we used the Cartesian product of every model between two years and calculated the distance between tokens in the same way as the intra-year distance.
Following both calculations, we combined both metrics by taking the ratio of the average inter-year distance over the average intra-year distance.
This approach will penalize tokens with high intra-year instability and vice-versa for more stable tokens.
Along with token distance calculations, it has been shown that including token frequency improves results compared to using distance alone [@doi:10.1007/s00799-019-00271-6].
We calculated token frequency as the ratio of token frequency in the more recent year over the frequency of the previous year. 
Then, we combined the frequency with distance ratios to make the final metric (Figure {@fig:pipeline_overview}D).

Following time series construction, we performed changepoint detection, which is a process that uses statistical techniques to detect abnormalities within a given time series (Figure {@fig:pipeline_overview}D).
We used the CUSUM algorithm [@gustafsson] to detect these abnormalities.
This algorithm uses a rolling sum of the differences between two timepoints and checks whether the sum is greater than a threshold.
A changepoint is considered to have occurred if the sum exceeds a threshold.
We used the 99th percentile on every generated timepoint as the threshold.
Then, we ran the CUSUM algorithm using a drift of 0 and default settings for all other parameters.



# Results

## Models can be aligned and compared within and between years

We examined how the usage of tokens in biomedical text changes over time.
Our evaluation was derived from machine learning models designed to predict the actual token given a portion of its surrounding tokens.
Each token was represented as a vector in a coordinate space constructed by these models.
However, training these models is stochastic, which results in arbitrary coordinate spaces.
Model alignment is essential in allowing word2vec models to be compared [@doi:10.48550/arXiv.1605.09096; @doi:10.1038/s41597-021-01047-x].
Before alignment, each model has its own unique coordinate space (Figure {@fig:word2vec_alignment}A), and each word is represented within that space (Figure {@fig:word2vec_alignment}B).
Alignment projects every model onto a shared coordinate space (Figure {@fig:word2vec_alignment}C), enabling direct token comparison.
We randomly selected 100 tokens to confirm that alignment worked as expected.
In aligned models, tokens in the global space were more similar to themselves within the year than between years, while identical tokens in unaligned models were completely distinct (Figure {@fig:word2vec_alignment}D).
Local distances were unaffected by alignment (Figure {@fig:word2vec_alignment}D), as token-neighbor distances were unaffected by the alignment procedure.

![
A. Without alignment, each word2vec model has its own coordinate space.
This is a UMAP visualization of 5000 randomly sampled tokens from 5 distinct Word2Vec models trained on the text published in 2010.
Each data point represents a token, and the color represents the respective Word2Vec model.
B. We greyed out all tokens except for the token 'probiotics' to highlight that each token appears in its own respective cluster without alignment.
C. After the alignment step, the token 'probiotic' is closer in vector space signifying that tokens can be easily compared.
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
We aimed to correct for this change in the underlying models by developing a statistic that, instead of using pairwise comparisons of token distances between individual models, integrated multiple models for each year by comparing tokens' intra- and inter-year variabilities.
We defined the statistic as the ratio of the average distance between two years over the sum of the average distance within each year respectively.

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
We found that distances tended to be markedly larger in the earliest years, where we expected models to be least stable, using the traditional approach (Figure {@fig:novel_distance_validation}B).
The integrated model approach did not display the same pattern in the earliest years (Figure {@fig:novel_distance_validation}C).
Both trends reinforce that training on smaller corpora will lead to high variation and that an integrated model strategy is needed [@doi:10.1162/tacl_a_00008].
Based on these results, we used the integrated-model strategy to calculate inter-year token distances for the remainder of this work.

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
We performed change point detection using the CUSUM algorithm with distances calculated with the integrated-model approach to correct for systematic differences in the underlying corpora.
We found 41281 terms with a detected change point from PMCOA and 2266 terms from preprints (Figures {@fig:preprint_published_changepoints}A and {@fig:preprint_published_changepoints}B), and the vast majority (38019 for PMCOA and 2260 for preprints) had just a single change-point.

We explored individual change points.
We detected one in PMCOA for 'cas9' from 2012 to 2013 (Figure {@fig:preprint_published_changepoints}C).
Before the change point, its closest neighbors were related genetic elements (e.g., 'cas'1-3).
After the change point, its closest neighbors became terms related to targeting, sgRNA, and gRNA, as well as other genome editing strategies, 'talen' and 'zfns' (Table {@tbl:cas9_neighbor_table}).
For some terms, we detected multiple change points within the studied interval.
We detected change points for 'SARS' from 2002 to 2003 and 2019 to 2020 (Figure {@fig:preprint_published_changepoints}D), consistent with the emergences of SARS-CoV [@doi:10.1046/j.1440-1843.2003.00517.x] and SARS-CoV-2 [@doi:10.1016/j.ijantimicag.2020.105924; @doi:10.1038/s41564-020-0695-z] as observed human pathogens.
We found miscellaneous neighbors before each change point, with use consistent with the acronym for Severe Acute Respiratory Syndrome after each (Tables {@tbl:sars_neighbor_table_one} and {@tbl:sars_neighbor_table_two}).

Out of all change points, we observed 200 tokens with at least one change point in each corpus.
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

We constructed an online application that allows users to examine how tokens change through time.
The application supports token input as text strings or as MeSH IDs, Entrez Gene IDs, and Taxonomy IDs.
Users might elect to explore the term 'pandemic', for which we detected a change point between 2019 and 2020.
Users can examine the token's nearest neighbors through time (Figure {@fig:website_walkthrough}A).
Using the token 'pandemic' as an example, users can observe that 'epidemic' remains similar through time, but taxid:114727 (the H1N1 subtype of influenza) only entered the nearest neighbors with the swine flu pandemic in 2009 and that MeSH:C000657245 (COVID-19) appeared in 2020.
The application also shows a frequency chart depicting how often the particular token is used each year (Figure {@fig:website_walkthrough}B), which can be displayed as a raw count or adjusted by the total size of the corpus.
When change points are detected, they are indicated on this panel (Figure {@fig:website_walkthrough}B).
The final visualization shows the union of the nearest 25 neighbors from each year ordered by the number of years that neighbor was present (Figure {@fig:website_walkthrough}C).
This visualization has a comparison function allowing users to examine years' differences.
All functionalities are fully supported across the PMCOA and preprint corpora, and users can toggle between the two.


# Discussion

Language is rapidly evolving, and the usage of words changes over time, with words assimilating new meanings or associations [@doi:10.1093/acrefore/9780199384655.013.323].
Some efforts have been made to study semantic change using biomedical text [@doi:10.1142/9789811232701_0011;@arxiv:2102.07836; @doi:10.2196/22635]; however, no such work has examined the changes evident in both pre-publication peer-reviewed and preprinted biomedical text.

We examined semantic changes within open-access biomedical corpora, Pubmed (PMCOA), and bioRxiv/MedRxiv, for the 2000-2022 interval.
We developed a novel statistic incorporating multiple Word2Vec models to examine semantic changes over two decades.
Before calculating our novel statistic, we used orthogonal processes that align each model (Figure {@fig:word2vec_alignment}).
We found that word vectors are closer together after alignment; however, the best approach to align models still remains open for future investigation [@doi:10.1007/978-3-030-32233-5_58].
As previously reported [@doi:10.1162/tacl_a_00008; @doi:10.48550/arXiv.1804.09692], we did find that without a correction step for the variability within and across years, comparing stable and unstable models is challenging.
Our correction approach showed that the average distances in the earlier years have less variability using multiple models than a single model (Figure {@fig:novel_distance_validation}).

After correcting year variability, our analysis revealed more than 41,000 changepoints, including tokens such as 'cas9', 'pandemic', and 'sars' (Figure {@fig:preprint_published_changepoints}).
Many changepoints overlapping between PMCOA and preprints were related to COVID-19 (Table {@tbl:published_preprint_change_table}), indicating that the COVID-19 pandemic has been strong and immediate enough to induce rapid semantic change across both publishing paradigms [@doi:10.1371/journal.pbio.3000959; @doi:10.1371/journal.pone.0240123].
We developed a web application that allows users to manually examine individual tokens, making examining other examples within our 41,000 changepoints easier.
However, approaches that can automatically validate these changepoints is an essential area that remains open for future investigation.


# Conclusion

We uncovered semantic changes within biomedical literature using a novel approach that accounts for inter- and intra-year variability.
Our approach found 41,000 changepoints that include well-known examples such as 'cas9', 'pandemic', and 'sars'.
We constructed a web application that allows users to manually examine these individual changepoints.
As an extension to this project, future work may be able to determine the consistency and time-lag of semantic change between preprint and pre-publication peer-reviewed text - potentially predicting future change in pre-publication peer-reviewed text.
Furthermore, including other preprint repositories may reveal consistencies across a broader swath of fields, or within-field analyses may reveal the earliest starting points of semantic changes that ultimately sweep through biomedicine.
Overall, this work is one starting point regarding semantic change within biomedical literature, and we are excited to see how this landscape will change as time progresses.


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

