# WiViCo | Wikipedia Vikidia Corpus
### A general-purpose parallel sentence simplification dataset for French

<p align="center">
<br>
    <a href="https://github.com/lormaechea/wivico/raw/main/wivico_v.1/wivico_dataset_v1.tar.gz">
        <img src="https://img.shields.io/badge/WIVICO--V1--DATASET-DOWNLOAD-DOWNLOAD?style=for-the-badge&logo=github">
    </a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://github.com/lormaechea/wivico/raw/main/wivico_v.2/wivico_dataset_v2.tar.gz">
        <img src="https://img.shields.io/badge/WIVICO--V2--DATASET-DOWNLOAD-DOWNLOAD?style=for-the-badge&logo=github">
    </a>
</p>

<br>

## General Presentation \& Repo Structure: 

This repository provides a general-purpose *complex-simpler* parallel sentence simplification dataset for French language: __*Wikipedia-Vikidia Corpus*, WiViCo__. It results from the development of a two-step automatic filtering method, that mines register-diversified comparable corpora so as to extract __complex-simpler pairs__. To do so, we sequentially address the two primary conditions that must be satisfied for a simplified sentence to be considered valid:

- __preservation of the original meaning__, that we addressed with the use of n:m-aware SBERT-based cosine similarities; and
- __simpliciy gain with respect to the source text__, that we treated with a text simplicity classification model.

This repository currently contains __two different versions__: 
- The ```wivico_v.1``` subfolder. It comprises the initial version of the dataset, by which we operated the aforementioned conditions with the use of *n:m*-aware SBERT-based cosine similarities (as a proxy to meaning retention) and an FFNN-based simplicity gain classifier. It results from the experiments conducted in the following article:

    ```bibtex 
    @inproceedings{ormaechea-2023-extracting-simplification-pairs,
        title = {Extracting Sentence Simplification Pairs from {F}rench Comparable Corpora Using a Two-Step Filtering Method},
        author = {Lucía Ormaechea and Nikos Tsourakis},
        booktitle = {Proceedings of the 8th edition of the Swiss Text Analytics Conference},
        month = {6},
        year = {2023},
        location = {Neuchâtel, Switzerland},
        publisher = {Association for Computational Linguistics},
        url = {https://aclanthology.org/2023.swisstext-1.4/},
        pages = {30--40}
    }
    ```

- The ```wivico_v.2``` subfolder, that includes the newest the version of WiViCo. The data derives from SBERT-based cosine similarities to assess meaning preservation, but it uses a finer-grained method to capture *complex-simpler* sentence pairs than the one used in the first version. It results from the experiments performed in the following paper:

    ```bibtex 
    @inproceedings{ormaechea-2023-simple-simpler-beyond,
        title = {Simple, Simpler and Beyond: A Fine-Tuning BERT-Based Approach to Enhance Sentence Complexity Assessment for Text Simplification},
        author = {Lucía Ormaechea, Nikos Tsourakis, Didier Schwab, Pierrette Bouillon and Benjamin Lecouteux},
        booktitle = {Proceedings of the 6th International Conference on Natural Language and Speech Processing (ICNSLP)},
        month = {12},
        year = {2023},
        location = {Trento, Italy},
        publisher = {Association for Computational Linguistics},
        url = {https://aclanthology.org/2023.icnlsp-1.12/},
        pages = {120--133}
    }
    ``` 

## Authors:

__Contact person__: [Lucía Ormaechea](https://luciaormaechea.com/), [lucia.ormaecheagrijalba@unige.ch](mailto:lucia.ormaecheagrijalba@unige.ch)

If you have further questions, don't hesitate to send us an email.
