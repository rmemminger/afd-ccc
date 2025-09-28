# AfD-CCC
A corpus of short texts and parliamentary speech transcripts by the German political party "Alternative für Deutschland" (AfD) addressing the topic of climate change (CC). The collection process and some exemplary usecases of the corpus are outlined in the associated paper and master's thesis. All data sources are clearly demarked in the following section.

## Data Sources
- German Parliament speeches (2017-2022): Extracted from [OpenDiscourse](https://dataverse.harvard.edu/citation?persistentId=doi:10.7910/DVN/FIKIBO) (Richter et al., 2020)
- German Parliament speeches (2022-2025): Retrieved from Government records via the [DIP API](https://dip.bundestag.de).
- European Parliament speeches (2014-2024): Extracted from the [ParlLawSpeech](https://parllawspeech.org/) dataset, Version 1.0 (Schwabach et al., 2025)
- Telegram messages (2019-2025): Scraped from public channels using [FROG](https://journals.sagepub.com/doi/10.1177/20501579241244973) (Priming & Fröschl, 2024)
- Press releases (2017-2021): Extracted from press releases made available by Schaefer et al. (2023)
- Tweets (2017-2022): From Lasser et al. (2022). Due to Twitter privacy regulations, only tweet IDs can be given. 

## Corpus Statistics

The corpus presented here is made up as follows:

| Text Domain    | Texts | Tokens  |
| :------------- | ----: | ------: |
| German Parl.   | 2,284 | 220,894 |
| European Parl. | 668   | 48,025  |
| Press releases | 911   | 85,356  |
| Twitter        | 1,880 | 54,592  |
| Telegram       | 766   | 41,487  |
| **Total**      | **6,509** | **450,354** |


## Version

This is Version 2.0 of the corpus, as of September 2025. Changes from Version 1.0 to 2.0 are as follows:
- Minimum text length reduced from >10 tokens excl. stop words to >=10 tokens incl. stop words
- CC topic filtering process changed from rudimentary keyword search to automated classification with an XGBoost classifier trained for the task
- Added filtered tweets (inly tweet IDs could be supplied)
- Tokenisation now removes punctuation and retains stop words

The [thesis document](Thesis-Memminger.pdf) contains detailed documentation of the topic filtering process in Version 2.0.

Version 1.0, as of May 30, 2025, and as it was presented at ACL 2025, is also contained as an archive in `data`. 

## Citation
To cite this corpus, please cite the paper which presented version 1.0 of the corpus.

> Manfred Stede and Ronja Memminger. 2025. [AfD-CCC: Analyzing the Climate Change Discourse of a German Right-wing Political Party.](https://aclanthology.org/2025.nlp4pi-1.14/) In Proceedings of the Fourth Workshop on NLP for Positive Impact (NLP4PI), pages 163–174, Vienna, Austria. Association for Computational Linguistics.

## Works Cited

 Jana Lasser, Segun Taofeek Aroyehun, Almog Simchon, Fabio Carrella, David Garcia, and Stephan Lewandowsky. 2022. Social media sharing of low-quality news sources by political elites. In: *PNAS Nexus* 1.4.

Florian Primig and Fabian Fröschl. 2024. Introducing the FROG tool for gathering Telegram data. *Mobile Media & Communication*, 12(2):449–453. [https://doi.org/10.1177/20501579241244973](https://doi.org/10.1177/20501579241244973)

Florian Richter, Philipp Koch, Oliver Franke, Jakob Kraus, Fabrizio Kuruc, Anja Thiem, Judith Högerl, Stella Heine, and Konstantin Schöps. 2020. *Open Discourse.* Harvard Dataverse. [https://doi.org/doi:10.7910/DVN/FIKIBO](https://doi.org/doi:10.7910/DVN/FIKIBO).

Robin Schaefer, Christoph M. Abels, Stephan Lewandowsky, and Manfred Stede. 2023. Communicating Climate Change: A Comparison Between Tweets and Speeches by German Members of Parliament. In *Proceedings of the 13th Workshop on Computational Approaches to Subjectivity, Sentiment & Social Media Analysis*, Toronto, Canada and Online. Association for Computational Linguistics.

Jan Schwalbach, Lukas Hetzer, Sven-Oliver Proksch, Christian Rauh, and Miklós Seb˝ok. 2025. [*ParlLawSpeech*](https://parllawspeech.org/data). GESIS, Cologne. [https://doi.org/10.7802/2824](https://doi.org/10.7802/2824)
