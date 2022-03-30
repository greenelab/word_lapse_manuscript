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
date-meta: '2022-03-30'
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
  <meta name="dc.date" content="2022-03-30" />
  <meta name="citation_publication_date" content="2022-03-30" />
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
  <link rel="alternate" type="text/html" href="https://greenelab.github.io/word_lapse_manuscript/v/d7dec8bb15b27e58c207fe497d08254a5aa0b903/" />
  <meta name="manubot_html_url_versioned" content="https://greenelab.github.io/word_lapse_manuscript/v/d7dec8bb15b27e58c207fe497d08254a5aa0b903/" />
  <meta name="manubot_pdf_url_versioned" content="https://greenelab.github.io/word_lapse_manuscript/v/d7dec8bb15b27e58c207fe497d08254a5aa0b903/manuscript.pdf" />
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
([permalink](https://greenelab.github.io/word_lapse_manuscript/v/d7dec8bb15b27e58c207fe497d08254a5aa0b903/))
was automatically generated
from [greenelab/word_lapse_manuscript@d7dec8b](https://github.com/greenelab/word_lapse_manuscript/tree/d7dec8bb15b27e58c207fe497d08254a5aa0b903)
on March 30, 2022.
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

1. Biomedical language is constantly changing
	1. Scientists make new discoveries
	2. Old technologies are being revamped
	3. More reasons for language changes
2. Diachronic studies aims to capture these types of changes through time
   1. Insert papers for language changes in general
      1. doi:10.1007/s00799-019-00271-6
      2. doi:10.1142/9789811232701_0011
      3. arxiv:1605.09096
      4. arxiv:1806.03537
      5. arxiv:1606.02821
      6. doi:10.18653/v1/N18-1044 
3. Gap in knowledge: 
	1. work has focused majorly on non-biomedical text
	2. biomedical related work is only on abstract and titles
	3. Work has yet to focus on individual tokens and themes.
4. Goal is to examine longitudinal trends for biomedical term changes.
<div style="color:red">
Don't forget in here your methodological contribution to estimate uncertainty with variable-size training datasets in each year by training multiple models and examining variability across them.
</div>


# Methods

1. Pubtator Central
   1. breif description about the dataset
   2. talk about how it contains entities tagged
2. Word2vec Model
   1. training parameters
   2. Use 10 models for each year
   3. min cutoff is 10
3. Orthogonal Procrustes - to align models onto year 2021
   1. Allows for the models to be directly compared
4. Determining semantic change
	1. Cosine metric to determine difference between words
	2. Scaf ratio method to model temporal changes
	3. CUSUM to actually detect change throughout the years
5. Umap visualization
   1. Explain why aligned umap - preserves local and global structure
   2. mention parameters for aligned umap


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
