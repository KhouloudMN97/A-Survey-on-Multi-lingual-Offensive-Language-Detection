# A Survey on Multi-lingual Offensive Language Detection

## This version is not ready yet, it will be finalized soon.

# Table of Contents
- [Definition of Hate Speech and Offensive Language](#definition-of-Hate-Speech-and-Offensive-Language)
- [Background on Multilingual Hate Speech Phenomena](#background-on-multilingual-hate-speech-phenomena)
- [Approaches on Multilingual Hate Speech Detection](#approaches-on-multilingual-hate-speech-detection)
- [Resources for Multilingual Hate Speech Detection](#resources-for-multilingual-hate-speech-detection)
- [Challenges and Limitations](#challenges-and-limitations)

## Definition of Hate Speech and Offensive Language
![Figure 1: Categories of Offensive Content](Figures/Fig%201.%20Categories%20of%20Offensive%20Content.png)
*Figure 1: Categories of Offensive Content*

Offensive content, hate speech, and aggressive content are distinct but they are often overlapping categories that involve harmful or negative expressions. While there is some overlap between these categories, their distinctions lie in their specific intentions, targets, and impacts on individuals or communities.


## Background on Multilingual Hate Speech Phenomena

In this section, we'll explore the multilingual hate speech phenomena.

| Title                                                                                                       | Main Focus of the Survey                                                                                                      | How to Differentiate it with Our Survey                                                                                       | Year | Type*    |
|:------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|:------|:---------|
| **A Survey on Hate Speech Detection using Natural Language Processing** [1]                                 | Investigating automated identification of hate speech through NLP, using linguistic and semantic features. Highlighting how identifying user profiles involved in spreading hateful content, and presenting supervised and semi-supervised approaches on English data. | No focus on the multilingual aspect of hate speech detection, only on studies conducted on English datasets.                                                                                                        | 2017 | Narrative |
| **Towards generalizable hate speech detection: a review on obstacles and solutions** [2]                  | Presenting NLP methods used for automated hate speech detection on online social media networks.                                                                                                                                                                                  | Not presenting multilingual hate speech detection.                                                                                                                                                                | 2021 | Narrative |
| **A Survey on Automatic Detection of Hate Speech in Text** [3]                                               | Provide an overview of the research conducted in hate speech detection, which includes describing available methods and resources.                                                                                                                                         | General overview about hate speech detection, not focusing on the multilingual aspect of the subject.                                                                                                           | 2018 | Systematic |
| **A systematic review of Hate Speech automatic detection using Natural Language Processing** [4]           | Focusing on the use of deep learning technologies and architectures in hate speech detection, with an emphasis on the sequence of pipeline processing.                                                                                                                               | Although presenting some resources (datasets and some available Github projects) in different languages, but no detailed overview of multilinguality.                      | 2023 | Systematic |
| **Resources and benchmark corpora for hate speech detection: a systematic review** [5]                     | Analyzing the annotated collections of texts released by the broader community, considering their method of creation, topic, language range, and other pertinent factors. | No analysis of the existing methods used in multilingual hate speech detection.                                                                                                                                             | 2021 | Systematic |
| **Towards multidomain and multilingual abusive language detection: a survey** [6]                           | A study of existing researches about the available datasets and methods used in cross-domain and cross-lingual cases.                                                                                                                                                          | Focus on the cross-lingual side only in the hate speech detection. No analysis of the available products or resources in the community, used and can be used in multilingual detection of hate speech. | 2023 | Narrative |
| **A literature survey on multimodal and multilingual automatic hate speech identification** [7]             | A survey of hate speech identification methods (strengths and weaknesses), and popular benchmark datasets.                                                                                                                                                              | Presenting approaches in several languages (monolingual), but no focus on multilingual nor cross-lingual approaches.                                                                                                         | 2023 | Narrative |

**Table 1: Key previous surveys on the topic of (multilingual) hate speech detection.**

**Note:** *A* **narrative review** *is a more subjective and qualitative study used to create a story from the literature in order to summarize the findings. In contrast, a* **systematic review** *is more objective and quantitative, used to discover and evaluate the available literature to address a certain research topic.*

*References can be found in the table titles.*

[1]: https://aclanthology.org/W17-1101/
[2]: https://peerj.com/articles/cs-598/
[3]: https://dl.acm.org/doi/10.1145/3232676
[4]: https://www.sciencedirect.com/science/article/pii/S0925231223003557
[5]: https://link.springer.com/article/10.1007/s10579-020-09502-8
[6]: https://dl.acm.org/doi/abs/10.1007/s00779-021-01609-1
[7]: https://dl.acm.org/doi/abs/10.1007/s00530-023-01051-8



## Approaches on Multilingual Hate Speech Detection
## Overview of Approaches on Multilingual and Cross-Lingual Hate Speech Detection

In this section, we'll provide an overview of approaches for multilingual and cross-lingual hate speech detection.

Abbreviations: LR (Logistic Regression), TL (Transfer Learning), MT (Machine Translation), EL (Ensemble Learning), Meta-L (Meta Learning), Multitask-L (Multitask Learning), UL (Unsupervised Learning), GAE (Graph Auto-Encoders). Language abbreviations are based on [ISO 639 language codes list](https://www.loc.gov/standards/iso639-2/php/code_list.php).

$\diamondsuit$/$\clubsuit$: $\diamondsuit$ refers to **Multilingual** methods & $\clubsuit$ refers to **cross-lingual** methods. Feature extraction methods are put between ().

| Techniques                               | Ref. $\diamondsuit$/$\clubsuit$ | Focused Languages                       | Approach (Feature Extraction Methods)         | Year |
|:-----------------------------------------|:------------------------------------|:---------------------------------------|:-----------------------------------------------|:-----|
| **Logistic Regression (LR)**              | [1](https://www.mdpi.com/2078-2489/12/1/5) $\diamondsuit$                | Hi, En and Code Mixed                  | Word embedding for feature extraction            | 2020 |
|                                          | [2](https://arxiv.org/abs/2004.06465) $\diamondsuit$                | Ar, En, De, Id, It, Pl, Pt, Es and Fr | MUSE and LASER for feature extraction           | 2020 |
| **Deep Neural Network (DNN)**            | [1](https://www.mdpi.com/2078-2489/12/1/5) $\diamondsuit$                | Hi, En and Code Mixed                  | CNN-LSTM (Word embedding)                       | 2020 |
|                                          | [2](https://www.iieta.org/journals/ria/paper/10.18280/ria.340111) $\diamondsuit$                | Ar, It, Pt, Id, En, De, Hi-En Code Mixed | CNN (Character-level representation)           | 2020 |
|                                          | [3](https://arxiv.org/abs/2108.03089) $\clubsuit$                   | En, Es and It: 6 languages pairs      | Bi-LSTM based capsule network (FastText)       | 2021 |
| **Transfer Learning (TL)**               | [1](https://www.mdpi.com/2078-2489/12/1/5) $\diamondsuit$                | Hi, En and code mixed                  | BERT                                           | 2020 |
|                                          | [2](https://arxiv.org/abs/2004.06465) $\diamondsuit$                | Ar, En, De, Id, It, Pl, Pt, Es, Fr    | mBERT                                          | 2020 |
|                                          | [3](https://aclanthology.org/2020.semeval-1.189/) $\diamondsuit$                | En, Tr, Da, El and Ar                 | XLM-R                                          | 2020 |
|                                          | [4](https://arxiv.org/abs/2109.13711) $\diamondsuit$                | En, Hi and Mr                        | XLM-R, mBERT, DistilmBERT (emoji2vec)         | 2021 |
|                                          | [5](https://arxiv.org/abs/2101.03207) $\diamondsuit$                | En, De, Hi                           | XLM-R                                          | 2021 |
|                                          | [6](https://arxiv.org/abs/2201.11294) $\diamondsuit$                | En, Ar, De, Id, It, Pt, Es, Fr, Tr, Da and Hi | mBERT (MUSE and LASER)             | 2022 |
|                                          | [7](https://www.sciencedirect.com/science/article/pii/S1319157821001804) $\diamondsuit$                | En and Ar                            | BERT, mBERT and AraBERT                        | 2022 |
|                                          | [8](https://aclanthology.org/2020.semeval-1.274/) $\clubsuit$                   | En, Da, El, Ar and Tr               | mBERT                                          | 2020 |
|                                          | [9](https://aclanthology.org/2020.emnlp-main.470/) $\clubsuit$                   | En, Hi, Bn and Es                   | XLM-R                                          | 2020 |
|                                          | [10](https://aclanthology.org/2020.semeval-1.290/) $\clubsuit$                  | En, El, Da, Ar and Tr               | XLM-R                                          | 2020 |
|                                          | [11](https://arxiv.org/abs/2004.13850) $\clubsuit$                  | En to Es                            | XLM-R based AXEL                               | 2020 |
|                                          | [12](https://dl.acm.org/doi/10.1145/3457610) $\clubsuit$                  | En, Ar, Bn, Da, El, Hi, Es, and Tr  | XLM-R                                          | 2021 |
|                                          | [13](https://aclanthology.org/2021.hackashop-1.5/) $\clubsuit$                  | En, Es, De, Id and Ar              | mBERT, LASER                                   | 2021 |
|                                          | [14](https://arxiv.org/abs/2111.00981) $\clubsuit$                  | En, Fr                             | mBERT, XLM-R                                   | 2021 |
|                                          | [15](https://www.mdpi.com/2078-2489/12/8/306) $\clubsuit$                  | En and 6 Indian languages: Indo-Aryan (Bn, Hi-En, Ur-En) and Dravidian (Kn-En, Malayalam-En, Ta-En) | mBERT, XLM-R             | 2021 |
|                                          | [16](https://peerj.com/articles/cs-559/) $\clubsuit$                  | Ar, Hr, De, En, and Sl             | mBERT, CseBERT                                  | 2021 |
|                                          | [17](https://dl.acm.org/doi/10.1145/3447535.3462495) $\clubsuit$                  | En, Es                             | MLIAN: Multilingual Interactive Attention Network (LASER, DistilmBERT) | 2021 |
|                                          | [18](https://www.sciencedirect.com/science/article/pii/S0306457322000978) $\clubsuit$                  | En, De, Da, Pl, Ru, Ja and Ko     | mBERT, XLM-R                                   | 2022 |
|                                          | [19](https://ojs.aaai.org/index.php/ICWSM/article/view/19402) $\clubsuit$                  | En, Es, It, De, Ar, El and Tr       | RoBERTa, BERT                                  | 2022 |
| **Machine Translation (MT)**             | [1](https://core.ac.uk/reader/296919330) $\clubsuit$                  | Hi, En, and  Id                     | Google Translate API to translate all data between source and target languages. | 2019 |
|                                          | [2](https://arxiv.org/abs/2004.06465) $\clubsuit$                   | Ar, En, De, Id, It, Pl, Pt, Es and Fr | Google Translate API to translate all the datasets in different languages to English = input to BERT | 2020 |
|                                          | [3](https://dl.acm.org/doi/10.1145/3465336.3475102) $\clubsuit$                   | En, Es and It: 6 languages pairs      | Google Translate API to translate all data between source and target languages  | 2021 |
|                                          | [4](https://www.sciencedirect.com/science/article/pii/S0306457321000510) $\clubsuit$                  | En, Fr, De, Id, It, Pt and Es    | Google Translate API to translate all datasets into En = input to BERT  | 2021 |
| **Ensemble Learning (EL)**               | [1](https://www.sciencedirect.com/science/article/pii/S1566253523002038) $\diamondsuit$               | En, De, Fr, Es and No                | Based DeBERTa: Simple averaging, weighted averaging based on AUC, and LightGBM using predictions as input. | 2023 |
|                                          | [2](https://aclanthology.org/2020.semeval-1.206/) $\clubsuit$                  | En, El, Da, Ar and Tr               | Majority Voting based mBERT                     | 2020 |
|                                          | [3](https://aclanthology.org/2021.ltedi-1.3/) $\clubsuit$                  | En and De                            | Based Bilingual word embeddings: FastText then MUSE | 2021 |
|                                          | [4](https://arxiv.org/abs/2201.05922) $\clubsuit$                  | En and De                            | Based mBERT, CNN and LSTM (Cross-Lingual Word Embeddings) | 2022 |
|                                          | [5](https://link.springer.com/article/10.1007/s10579-023-09637-4) $\clubsuit$                  | En and Es                            | Based mBERT                                     | 2023 |
| **Meta Learning (Meta-L)**               | [1](https://dl.acm.org/doi/abs/10.1145/3503162.3503167) $\clubsuit$                  | Ta-English and Malayalam-English code-mixed | MAML and Proto-MAML, based XLM-R | 2021 |
|                                          | [2](https://ieeexplore.ieee.org/document/9696324) $\clubsuit$                  | Hate speech: En, Ar, Es, De, Id, It, Pt, Fr and Offensive lang. Ar, Da, En, El, Fa and Tr | MAML and Proto-MAML, based XLM-R | 2022 |
|                                          | [3](https://arxiv.org/abs/2303.02513) $\clubsuit$                  | En, Es, Ar, Da, El, Tr, Hi, De, It| HateMAML: domain-adaptive MAML based mBERT and XLM-R | 2023 |
| **Multitask-L - Joint training**          | [1](https://aclanthology.org/2019.jeptalnrecital-court.21/) $\diamondsuit$               | Fr and En                            | Based Bi-LSTM (Glove bilingual word embeddings) | 2019 |
|                                          | [2](https://aclanthology.org/P19-2051/) $\clubsuit$                  | En, It, Es, and De                   | Based MUSE                                    | 2019 |
|                                          | [3](https://www.sciencedirect.com/science/article/pii/S0306457321000510) $\clubsuit$                  | En, Fr, De, Id, It, Pt and Es    | Based MUSE, LASER, mBERT                    | 2021 |
| **Multitask-L - Auxiliary task**          | [1](https://aclanthology.org/2022.jeptalnrecital-taln.41/) $\clubsuit$                  | En, It and Es                        | Based XLM-R, XLM-T                          | 2022 |
|                                          | [2](https://aclanthology.org/2022.findings-aacl.33/) $\clubsuit$                  | En, It and Es                        | Based mBERT, XLM-R, XLM-T                   | 2022 |
| **UL - GAE**                             | [1](https://aclanthology.org/2022.lrec-1.236/) $\diamondsuit$               | En, De, Ru, Tr, Hr and Sq             | Based mBERT, XLM-R (TFIDF)                   | 2022 |
| **UL - Adversarial**                      | [1](https://www.sciencedirect.com/science/article/pii/S0045790622002725) $\clubsuit$           


## Resources for Multilingual Hate Speech Detection
This section provides resources related to multilingual hate speech detection.

## Challenges and Limitations
Explore the challenges and limitations of multilingual hate speech detection in this section.
