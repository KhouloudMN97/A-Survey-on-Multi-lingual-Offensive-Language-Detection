# A Survey on Multi-lingual Offensive Language Detection <img src="Figures/Logo.jpeg" width="200">

## This version is currently a work in progress and is not yet finalized. We are actively working on it and anticipate that it will be ready for release in the near future.

### Please let us know if you find out a mistake or have any suggestions by e-mail: khouloud.mnassri@telecom-sudparis.eu

# Table of Contents 📑
#### The repository structure refers to our survey paper "A Survey on Multi-lingual Offensive Language Detection"
- [Definition of Hate Speech and Offensive Language](#definition-of-Hate-Speech-and-Offensive-Language) 🗣️
- [Background on Multilingual Hate Speech Phenomena](#background-on-multilingual-hate-speech-phenomena) 🌍
- [Approaches on Multilingual Hate Speech Detection](#approaches-on-multilingual-hate-speech-detection) 🧠
- [Datasets on Multilingual Hate Speech Detection](#datasets-on-Multilingual-Hate-Speech-Detection) 📊
- [Resources for Multilingual Hate Speech Detection](#resources-for-multilingual-hate-speech-detection) 🧰
- [Computational limitations](#computational-limitations) 💻


## Definition of Hate Speech and Offensive Language
![Figure 1: Categories of Offensive Content](Figures/Fig%201.%20Categories%20of%20Offensive%20Content.png)
*Categories of Offensive Content*

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



## Approaches on Multilingual and and Cross-Lingual Hate Speech Detection

An overview of approaches for multilingual and cross-lingual hate speech detection.

Abbreviations: LR (Logistic Regression), TL (Transfer Learning), MT (Machine Translation), EL (Ensemble Learning), Meta-L (Meta Learning), Multitask-L (Multitask Learning), UL (Unsupervised Learning), GAE (Graph Auto-Encoders). Language abbreviations are based on [ISO 639 language codes list](https://www.loc.gov/standards/iso639-2/php/code_list.php).

$\diamondsuit$/$\clubsuit$: $\diamondsuit$ refers to **Multilingual** methods & $\clubsuit$ refers to **cross-lingual** methods. Feature extraction methods are put between ().

| Techniques                               | Ref. $\diamondsuit$/$\clubsuit$ | Focused Languages                       | Approach (Feature Extraction Methods)         | Year |
|:-----------------------------------------|:------------------------------------|:---------------------------------------|:-----------------------------------------------|:-----|
| **Logistic Regression (LR)**              | [1](https://www.mdpi.com/2078-2489/12/1/5) $\diamondsuit$              | Hi, En and Code Mixed                  | Word embedding for feature extraction            | 2020 |
|                                          | [2](https://arxiv.org/abs/2004.06465)  $\diamondsuit$                | Ar, En, De, Id, It, Pl, Pt, Es and Fr | MUSE and LASER for feature extraction           | 2020 |
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
| **UL - Adversarial**                      | [1](https://www.sciencedirect.com/science/article/pii/S0045790622002725) $\clubsuit$        | En, Da, Ar, El and Tr          | Based mBERT               | 2022   

## Datasets on Multilingual Hate Speech Detection

A summary of the available datasets for hate speech detection.

Abbreviations notes: For the column names, Ref.:Reference, Cit.:Citation by May-2023, and
Av.:Available. Language names have been shortened using the [ISO 639 language codes list](https://www.loc.gov/standards/iso639-2/php/code_list.php).

Under the “Main Subject” column: HS:Hate Speech, OL:Offensive Language, CN:Counter-Narrative,
and Agr.:Aggressiveness. In “Size” column: Approx.:Approximately. In “Av.” column: Y:Yes and N:No.


| Ref | Year | Language(s) | Main Subject | Source | Size | Cit. | Av. |
|-----|------|-------------|--------------|--------|------|------|-----|
| [carvalho2022hate](https://aclanthology.org/2022.lrec-1.253/) | 2022 | Pt | HS | Twitter | 63450 | <10 | N |
| [wang2022political](https://ieeexplore.ieee.org/document/9738642) | 2022 | Zh | HS | LINE Today | 47844 | <10 | N |
| [ollagnier2022cyberagressionado](https://aclanthology.org/2022.lrec-1.91/) | 2022 | Fr | Agr. | Aggressive multiparty chats collected through a role-playing game | 19 conversations | <10 | [Y](https://github.com/aollagnier/CyberAgressionAdo-v1) |
| [beyhan2022turkish](https://aclanthology.org/2022.lrec-1.443/) | 2022 | Tr | HS | Twitter | IstanbulConv:1206 Refugee:1278 | <10 | [Y](https://github.com/verimsu/Turkish-HS-Dataset) |
| [madhu2023detecting](https://dl.acm.org/doi/10.1016/j.eswa.2022.119342) | 2023 | Hi-En | HS and OL | Twitter | 7088 | <10 | [Y](https://hasocfire.github.io/hasoc/2021/dataset.html) |
| [mohapatra2021automatic](https://www.mdpi.com/2076-3417/11/18/8575) | 2021 | Or/Or-En | HS | Facebook | 5000 | <10 | N |
| [steinberger2017cross](https://aclanthology.org/R17-1089/) | 2017 | Cs, En, Fr, It, De | Flames | User-generated news article discussions | Cs:1812 De:1122, En:1007 Fr:487 It:649 | <10 | [Y](http://nlp.kiv.zcu.cz/projects/flame) |
| [fernquist2019study](https://ieeexplore.ieee.org/document/9005534) | 2019 | Sv | HS | A Swedish discussion forum | 3056 | <10 | N |
| [rahman2021information](https://arxiv.org/abs/2106.09775) | 2021 | En | HS | Twitter | 9667 | <50 | [Y](https://github.com/mdmustafizurrahman/An-Information-Retrieval-Approach-to-Building-Datasets-for-Hate-Speech-Detection) |
| [zampieri2022predicting](https://link.springer.com/article/10.1007/s13278-022-00906-8) | 2022 | Mr | OL | Twitter | MOLD2.0: 3611 SeMold: 8000 | <50 | [Y](https://github.com/tharindudr/MOLD) |
| [nascimento2019hate](https://dl.acm.org/doi/10.1145/3323503.3360619) | 2019 | Pt-BR | OL | Twitter and Brazilian 55chan imageboard | 7672 | <50 | [Y](https://github.com/LaCAfe/Dataset-Hatespeech) |
| [akhtar2021whose](https://arxiv.org/abs/2106.15896) | 2021 | En | HS, Agr., OL, and Stereotype | Twitter | 4480 | <50 | N |
| [mubarak2022emojis](https://arxiv.org/abs/2201.06723) | 2022 | Ar | HS and OL | Twitter | 12698 | <50 | N |
| [ombui2019hate](https://ieeexplore.ieee.org/document/8932845) | 2019 | En, Sw, Other East African Languages | HS and OL | Twitter | 260k | <50 | N |
| [evkoski2022retweet](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0265602) | 2022 | Sl | HS | Twitter | 12961136 | <50 | [Y](https://www.clarin.si/repository/xmlui/handle/11356/1423) |
| [satapara2021overview](https://ceur-ws.org/Vol-3159/T1-2.pdf) | 2021 | Hi-En | HS | Twitter | 7088 | <50 | [Y](https://hasocfire.github.io/hasoc/2023/dataset.html) |
| [luu2021large](https://link.springer.com/chapter/10.1007/978-3-030-79457-6_35#:~:text=We%20constructed%20a%20large%2Dscale,save%20time%20for%20data%20annotating.) | 2021 | Vi | HS and OL | Facebook and YouTube | 33400 | <50 | [Y](https://github.com/sonlam1102/vihsd) |
| [fanton2021human](https://arxiv.org/abs/2107.08720) | 2021 | En | HS / CN | | 5000 HS/CN pairs | <50 | [Y](https://github.com/marcoguerini/CONAN) |
| [ali2022hate](https://dl.acm.org/doi/abs/10.1016/j.csl.2022.101365) | 2022 | Ur | HS and OL | Twitter | 10526 | <50 | N |
| [ljubevsic2018datasets](https://aclanthology.org/W18-5116/) | 2018 | Sl, Hr | Moderated News Comments | The Slovene RTV MCC and Croatian 24sata News Portals | 24639651 | <50 | [Y(1)](https://www.clarin.si/repository/xmlui/handle/11356/1201), [Y(2)](https://www.clarin.si/repository/xmlui/handle/11356/1202) |
| [vu2020hsd](https://arxiv.org/abs/2007.06493) | 2020 | Vi | HS and OL | Facebook | 5431 | <50 | [Y](https://github.com/vietnlp/vlsp2019_hatespeech_task/) |
| [ptaszynski2019results](https://ruj.uj.edu.pl/xmlui/bitstream/handle/item/152265/ptaszynski_pieciukiewicz_dybala_results_of_the_poleval_2019.pdf?sequence=1&isAllowed=y) | 2019 | Pl | HS and Cyberbullying | Twitter | 11041 | <50 | [Y](https://github.com/ptaszynski) |
| [gaikwad-etal-2021-cross](https://aclanthology.org/2021.ranlp-1.50/) | 2021 | Mr | OL | Twitter | MOLD 1.0: 2499 | <50 | [Y](https://github.com/tharindudr/MOLD) |
   | [haddad2019t](https://www.springerprofessional.de/en/t-hsab-a-tunisian-hate-speech-and-abusive-dataset/17242764) | 2019 | Tunisian Ar | HS and Abusive | Different social media platforms | 6075 | <50 | [Y](https://github.com/Hala-Mulki/T-HSAB-A-Tunisian-Hate-Speech-and-Abusive-Dataset) |
   | [das2021bangla](https://arxiv.org/abs/2203.16775) | 2021 | Bn | HS | Facebook | 7425 | <50 | N |
   | [rizwan2020hate](https://aclanthology.org/2020.emnlp-main.197/) | 2020 | Roman Ur | HS | Twitter | 10012 | <50 | [Y](https://github.com/haroonshakeel/roman_urdu_hate_speech) |
   | [guest2021expert](https://aclanthology.org/2021.eacl-main.114/) | 2021 | En | Misogyny | Reddit | 6567 | <50 | [Y](https://github.com/ellamguest/online-misogyny-eacl2021) |
   | [leite2020toxic](https://aclanthology.org/2020.aacl-main.91/) | 2020 | Pt-BR | Toxic Speech | Twitter | 21K | <50 | [Y](https://github.com/JAugusto97/ToLD-Br) |
   | [ishmam2019hateful](https://ieeexplore.ieee.org/document/8999254) | 2019 | Bn | HS | Facebook | 5126 | <50 | [Y](https://github.com/IshmamAlvi/Hate-Speech-for-Bengali-language) |
   | [moon2020beep](https://aclanthology.org/2020.socialnlp-1.4.pdf) | 2020 | Ko | Toxic Speech (HS and OL) | A popular domestic entertainment news aggregation platform | 9381 | <100 | [Y](https://github.com/kocohub/korean-hate-speech) |
   | [mandl2021overview](https://arxiv.org/abs/2112.09301) | 2021 | En, Hi, Mr | HS and OL | Twitter | En:3843 Mr:1874 Hi:4594 | <100 | [Y](https://hasocfire.github.io/hasoc/2023/dataset.html) |
   | [de2017offensive](https://sol.sbc.org.br/index.php/brasnam/article/view/3260) | 2016 | Pt-BR | OL | Brazilian Web (g1.globo.com) | OFFCOMBR-2: 1250, OFFCOMBR-3: 1033 | <100 | [Y](https://github.com/rogersdepelle/OffComBR) |
   | [fortuna2019hierarchically](https://aclanthology.org/W19-3510/) | 2019 | Pt | HS | Twitter | 5668 | <100 | [Y](https://github.com/paulafortuna/Portuguese-Hate-Speech-Dataset) |
   | [alvarez2018overview](https://ceur-ws.org/Vol-2150/overview-mex-a3t.pdf) | 2018 | Es-MX | Agr. | Twitter | 10856 | <100 | [Y](https://mexa3t.wixsite.com/home/copia-de-description) |
   | [fivser2017legal](https://aclanthology.org/W17-3007/) | 2017 | Sl | Socially Unacceptable Discourse | Spletno Oko1 (Web Eye) hotline service | 13000 | <100 | N |
   | [mossie2020vulnerable](https://dl.acm.org/doi/10.1016/j.ipm.2019.102087) | 2020 | Am | HS and Vulnerable Community | Facebook | 491424 | <100 | N |
   | [kumar2020evaluating](https://arxiv.org/abs/1803.09402) | 2020 | Bn, Hi, En | Agr. | YouTube | Approx. 6000 per lang. | <100 | [Y](https://sites.google.com/view/trac2/shared-task) |
   | [ibrohim2018dataset](https://www.sciencedirect.com/science/article/pii/S1877050918314583) | 2018 | Id | HS | Twitter | 2016 | <100 | [Y](https://github.com/okkyibrohim/id-abusive-language-detection) |
   | [mulki2019hsab](https://aclanthology.org/W19-3512/) | 2019 | Levantine Ar | HS and Abusive | Twitter | 5846 | <150 | N |
   | [ccoltekin2020corpus](https://aclanthology.org/2020.lrec-1.758/#:~:text=The%20corpus%20contains%2036%20232,the%20target%20of%20the%20offense) | 2020 | Tr | OL | Twitter | 36232 | <150 | [Y](https://coltekin.github.io/offensive-turkish/) |
   | [mathur2018detecting](https://aclanthology.org/W18-3504/) | 2018 | Hi-En | HS and OL | Twitter | 3679 | <150 | N |
   | [pitenis2020offensive](https://aclanthology.org/2020.lrec-1.629/) | 2020 | El | OL | Twitter | OGTD 1.0: 4779, OGTD 2.0: 10287 | <150 | [Y](https://opendatalab.com/OGTD) |
   | [chung2019conan](https://aclanthology.org/P19-1271/) | 2019 | En, Fr, It | HS / CN | Generated by experts | 4078 HS/CN pairs | <150 | [Y](https://github.com/marcoguerini/CONAN) |
   | [sigurbergsson2019offensive](https://aclanthology.org/2020.lrec-1.430/) | 2019 | Da | HS and OL | Reddit and Facebook | 3600 | <150 | [Y](https://huggingface.co/datasets/DDSC/dkhate) |
   | [pavlopoulos2017deep](https://aclanthology.org/W17-3004/) | 2017 | El | User Comment Moderation | A Greek news portal (http://www.gazzetta.gr/) | Approx. 1.6M | <150 | [Y](http://nlp.cs.aueb.gr/software.html) |
   | [ibrohim2019multi](https://aclanthology.org/W19-3506/) | 2019 | Id | HS and Abusive | Twitter | 13169 | <150 | [Y](https://github.com/okkyibrohim/id-multi-label-hate-speech-and-abusive-language-detection) |
   | [pereira2019detecting](https://www.mdpi.com/1424-8220/19/21/4654) | 2019 | Es | HS | Twitter | 6000 | <150 | [Y](https://zenodo.org/record/2592149#.ZGuEKXZByUk) |
   | [kumar2018aggression](https://aclanthology.org/L18-1226/) | 2018 | Hi-En | Agr. | Facebook and Twitter | Approx. 18k tweets and 21k Facebook comments | <150 | N |
   | [Alfina2017hate](https://ieeexplore.ieee.org/document/8355039) | 2017 | Id | HS | Twitter | 520 | <200 | [Y](https://github.com/ialfina/id-hatespeech-detection) |
   | [ousidhoum2019multilingual](https://aclanthology.org/D19-1474/) | 2019 | En, Fr, Ar | HS | Twitter | En:5647 Fr:4014 Ar:3353 | <200 | [Y](https://github.com/HKUST-KnowComp/MLMA_hate_speech) |
   | [bohra2018dataset](https://aclanthology.org/W18-1105/) | 2018 | Hi-En | HS | Twitter | 4575 | <200 | [Y](https://github.com/deepanshu1995/HateSpeech-Hindi-English-Code-Mixed-Social-Media-Text) |
   | [sanguinetti2018italian](https://aclanthology.org/L18-1443/) | 2018 | It | HS | Twitter | 6009 | <200 | [Y](https://github.com/msang/hate-speech-corpus) |
   | [fersini2018overview](https://ceur-ws.org/Vol-2150/overview-AMI.pdf) | 2018 | Es, En | Misogyny | Twitter | En:3977 Es:4138 | <250 | [Y](https://amiibereval2018.wordpress.com/important-dates/data/) |
   | [mandl2019overview](https://dl.acm.org/doi/abs/10.1145/3368567.3368584) | 2019 | En, Hi, De | HS and OL | Twitter and Facebook | En:5852, Hi:4665, De:3819 | <350 | [Y](https://hasocfire.github.io/hasoc/2019/dataset.html) |
   | [zampieri2020semeval](https://aclanthology.org/2020.semeval-1.188/) | 2020 | Ar, Da, En, El, Tr | OL | Twitter, Facebook, Reddit, a local newspaper: Ekstra Bladet | En:1448861, Ar:1589, Da:384, El:2486, Tr:6131 | <400 | [Y](https://sites.google.com/site/offensevalsharedtask/offenseval-2020?authuser=0) |
   | [del2017hate](https://ceur-ws.org/Vol-1816/paper-09.pdf) | 2017 | It | HS | Facebook | ? | <400 | N |
   | [basile-etal-2019-semeval](https://aclanthology.org/S19-2007/) | 2019 | Es, En | HS | Twitter | En:13000, Es:6600 | <750 | [Y](https://github.com/cicl2018/HateEvalTeam) |





![Datasets distribution based on languages](Figures/Fig%202.%20Datasets%20distribution%20based%20on%20languages.jpg)
*Datasets distribution based on languages*


Number of papers studies in this survey and their
impact (based on citations @May 2023).

Note: English (47 papers with 11k citations) is excluded from the figure to have a better visualization in
the distribution

## Resources for Multilingual Hate Speech Detection
Collaborative International and European Projects on Hate Speech

| Project                                                                                                          | Partners                                                                                                      | Year         |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|--------------|
| [DARE: Dialogue About Radicalisation and Equality](https://www.dare-h2020.org) Not provided now!                                   | Belgium, Croatia, France, Germany, Greece, Malta, Norway, Poland, Russian Federation, The Netherlands, Tunisia, Turkey and the UK | 2017-2020    |
| [MANDOLA: Monitoring and Detecting OnLine Hate Speech](https://mandola-project.eu/)                               | Greece, Ireland, France, Spain, Bulgaria and Cyprus                                                         | 2017         |
| [PRO2HATERS: PROactive PROfiling of HATE speech spreadeRs](https://www.symanto.com/nlp-resources/cdti-prohaters/) | Germany                                                                                                       | 2017         |
| [Hatemeter: Hate speech tool for monitoring, analyzing and tackling Anti-Muslim hatred online](http://hatemeter.eu/?pageid=197) | Italy, France and the UK | 2018-2020 |
| [sCAN: specialised Cyber-Activists Network](https://scan-project.eu/the-project/)                                | France, Germany, Italy, Belgium, Czech Republic, Austria, Slovenia, Croatia and Latvia | 2018-2020 |
| [PANACEA: Protection and privAcy of hospital and health iNfrastructures with smArt Cyber sEcurity and cyber threat toolkit for dAta and people](https://cordis.europa.eu/project/id/826293) | Italy, UK, Greece, France, Belgium, Netherlands, Germany and Ireland | 2019-2022 |
| [DTCT: Detect Then Act](https://dtct.eu/)                                                                        | Belgium, Germany, the UK and the Netherlands                                                                 | 2019-2021    |
| [Identrics](https://identrics.ai/hate-speech-detection/)                                                        | Bulgaria                                                                                                      | 2023         |
| [OHI: Online Hate Index](https://www.adl.org/online-hate-index)                                                | USA                                                                                                           | Released in 2018 |
| [ProPublica’s Documenting Hate Project](https://projects.propublica.org/graphics/hatecrimes)                   | USA                                                                                                           | Started in 2017  |


##
##
Summary of Community Challenges on Multilingual Hate Speech Detection

| Challenge Name                                                                                                                                   | Languages                                                                                                                | Year  |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|-------|
| [TRAC-1: Aggression Identification](https://sites.google.com/view/trac1/shared-task) | English, Hindi (Roman and Devanagari scripts)                                                                         | 2018  |
| [SemEval-2019 Task 5: Multilingual Detection of Hate Speech Against Immigrants and Women in Twitter](https://competitions.codalab.org/competitions/19935) | English, Spanish | 2019  |
| [Kaggle’s Jigsaw Multilingual Toxic Comment Classification](https://www.kaggle.com/c/jigsaw-multilingual-toxic-comment-classification) | Multilingual (trained on English data) | 2020  |
| [Hate Speech Detection (HASOC) Competition](https://competitions.codalab.org/competitions/26027) | English, German, Hindi | 2020  |
| [TRAC 2020: Trolling, Aggression, and Cyberbullying](https://sites.google.com/view/trac2/shared-task) | English, Hindi (Roman and Devanagari scripts), Bangla (Roman and Bangla scripts) | 2020  |
| [Kaggle IIIT-D Multilingual Abusive Comment Identification](https://www.kaggle.com/competitions/iiitd-abuse-detection-challenge) | Multiple Indic languages | 2021  |
| [PAN shared task of Profiling Hate Speech Spreaders on Twitter](https://pan.webis.de/clef21/pan21-web/author-profiling.html) | English, Spanish | 2021  |



##
##

Github Repositories for Multilingual source code projects of Hate Speech
| **Name** | **Languages** | **Link** | **Study if available** | **Year** |
| --- | --- | --- | --- | --- |
| Enhancing social network hate detection using back translation and GPT-3 augmentations during training and test-time | En, Fr, De, Es and No | [code](https://github.com/OrKatz7/parler-hate-speech) | [COHEN2023101887](https://www.sciencedirect.com/science/article/pii/S1566253523002038) | 2023 |
| Highly Generalizable Models for Multilingual Hate Speech Detection | En, Ar, De, Id, It, Pt, Es, Fr, Tr, Da and Hi | [code](https://github.com/vidhur2k/Multilngual-Hate-Speech/tree/main/models) | [DBLP:journals/corr/abs-2201-11294](https://arxiv.org/abs/2201.11294) | 2022 |
| Multilingual-Abuse-Comment-Detection | 17 Hi languages | [code](https://github.com/deekshakoul/Multilingual-Abuse-Comment-Detection) | Non available | 2022 |
| HateCheck: Functional Tests for Hate Speech Detection Models | Ar, Nl, Fr, De, Hi, It, Zh, Pl, Pt and Es | [code](https://github.com/rewire-online/multilingual-hatecheck) | [rottger-etal-2021-hatecheck](https://aclanthology.org/2021.acl-long.4/) | 2022 |
| Deep Learning Models for Multilingual Hate Speech Detection | Ar, En, De, Id, It, Pl, Pt, Es and Fr | [code](https://github.com/hate-alert/DE-LIMIT) | [10.1007/978-3-030-67670-4_26](https://link.springer.com/chapter/10.1007/978-3-030-67670-4_26) | 2021 |
| EACL 2021 OffensEval in Dravidian Languages | Kn, Ml and Ta | [code](https://github.com/murali1996/eacl2021-OffensEval-Dravidian) | [jayanthi-gupta-2021-sj](https://aclanthology.org/2021.dravidianlangtech-1.44/) | 2021 |
| Leveraging Multilingual Transformers for Hate Speech Detection | En, De and Hi | [code](https://github.com/sayarghoshroy/Hate-Speech-Detection) | [DBLP:journals/corr/abs-2101-03207](https://arxiv.org/abs/2101.03207) | 2021 |
| Offensive Language Detection from Multilingual Code-Mixed Text using Transformers | Kn, Ml and Ta | [code](https://github.com/eftekhar-hossain/CUET_NLP-EACL_2021) | [DBLP:journals/corr/abs-2103-00455](https://aclanthology.org/2021.dravidianlangtech-1.35/) | 2021 |
| Multi-oli | Da, Ko and En | [code](https://github.com/jiminsun/multi-oli) | The language-adversarial training pipeline inspired from [keung-etal-2019-adversarial](https://aclanthology.org/D19-1138/) | 2021 |
| Indonesian Text Classification Multilingual | En and Id | [code](https://github.com/ilhamfp/indonesian-text-classification-multilingual) | [DBLP:journals/corr/abs-2009-05713](https://ieeexplore.ieee.org/document/9429038) | 2021 |
| Detoxify: Toxic Comment Classification with Pytorch Lightning and Transformers | En, Fr, Es, It, Pt, Tr and Ru | [code](https://github.com/unitaryai/detoxify) | Non available | 2020 |
| NLPDove at SemEval-2020 Task 12: Improving Offensive Language Detection with Cross-lingual Transfer | En, El, Da, Ar and Tr | [code](https://github.com/hwijeen/OffensEval2020) | [DBLP:journals/corr/abs-2008-01354](https://aclanthology.org/2020.semeval-1.206/) | 2020 |
| Multilingual Fairness LREC | En, It, Pl, Pt, Es | [code](https://github.com/xiaoleihuang/Multilingual_Fairness_LREC) | [huang-etal-2020-multilingual](https://aclanthology.org/2020.lrec-1.180/) | 2020 |



![Summary of APIs and their Language Capabilities in Hate Speech Detection](Figures/Table%208.%20Summary%20of%20APIs%20and%20their%20Language%20Capabilities%20in%20Hate%20Speech%20Detection.PNG)
*Summary of APIs and their Language Capabilities in Hate Speech Detection*


## Computational limitations
![Comparative Analysis of Affordable Computational Resources for Machine Learning Training](Figures/Table%209.%20Comparative%20Analysis%20of%20Affordable%20Computational%20Resources%20for%20Machine%20Learning.PNG)

*Comparative Analysis of Affordable Computational Resources for Machine Learning Training*

## Citation
Not yet provided