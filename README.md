# Assignment2, Collecting Data, MA Digital Humanities

# Ancient Greek Epitaphs Corpus

## Corpus Description

The Epitaphs Corpus contains three of the most well-known epitaphs from ancient Greek history, written by Demosthenes, Lysias, and Thucydides, Ancient Greek orators and historians. 
Epitaphs, in the context of Ancient Greece, are speeches or inscriptions meant to honor the fallen, celebrating their sacrifices and virtues.
These epitaphs are renowned for their exceptional literary and rhetorical quality, their carefully chosen words, and their ability to convey the ideals and values of the societies they were raised from.


## Target Audience and Intended Use

This corpus is designed for:

Researchers in Ancient Greek language and philology, who wish to analyze the rhetorical and literary aspects of these epitaphs.
Students and practitioners of Digital Humanities, particularly those interested in natural language processing (NLP) tasks involving historical texts.
Potential use cases include text classification, tokenization, named entity recognition (NER), and comparative literary analysis.

This corpus is intended for use in computational linguistics, philological research, and NLP-related tasks. The texts are provided in translated, raw and annotated formats for analysis and experimentation.

## Text Selection Criteria
The three selected epitaphs represent some of the most important examples of ancient Greek funeral oratory. These texts were chosen for their:

**Significance**: Each epitaph praises the fallen while emphasizing the ideals and values of the city-state they served.

**Diversity in Style and Purpose**:

`Demosthenes`: Known for his emotional appeal, emphasizing personal sacrifice and patriotism.

`Thucydides`: Philosophical and reflective, highlighting the virtues and principles of the polis.

`Lysias`: Balanced and clear, focusing on collective sacrifice and the historical context, serving as a stylistic "middle ground" between the other two.

**Literary Quality**: These epitaphs exemplify exceptional rhetorical and literary techniques, making them ideal for research and NLP experimentation.

**Accessibility**: The texts and their modern Greek translations are freely available online.

Each author reflects different facets of ancient Greek political and moral life, and their inclusion ensures diversity in writing style and length.

## Data Collection Process

The texts were collected manually from the following sources:

The Greek translated texts were obtained from the Greek Language Center website (https://www.greek-language.gr/).

Translations used: 
**Demosthenes**: Translated by A. Tyflopoulos – Edited by D. Iakovos (2006).

**Thucydides**: Translated by E. Lambridis (1962).

**Lysias**: Translated by G.A. Raptis (2004).

## Cleaning and Preprocessing

The preprocessing steps applied to the texts are as follows:

`Loading Texts`: Created a dictionary associating each file name with its corresponding text.

`Cleaning`: Removed extra spaces and normalized the text for further processing.

`Tokenization and Lemmatization`: Tokenized the text into individual words and lemmatized them using the spaCy NLP library.

`Part-of-Speech (POS) Tagging`: Tagged each token with its POS category.

`Named Entity Recognition (NER)`: Extracted named entities from the texts using spaCy.

However, the model's performance was suboptimal:
The small model misclassified entities, such as identifying Άρης and Θερμόδωντας as geopolitical entities (GPE) rather than persons.
Testing the large model produced as well wrong results.

## Annotations

The annotated data includes:

`Tokenized Text`: Individual tokens extracted from the raw text.
`Lemmatized Text`: Lemmatized forms of the tokens.
`Parts of Speech (POS)`: POS tags for each token.
`Named Entity Labels`: Tags assigned to entities in the text (though the NER results were not fully accurate).
Annotations were generated using the spaCy NLP library.

## File Formats

The corpus is available in the following formats:

**Raw Text Files (.txt)**: Contain the original texts as they were collected manually.
**Annotated Corpus File (.csv)**: Includes all the processed and annotated data.

| CSV Column Names | Description                               |
|------------------|-------------------------------------------|
| 'Filename'       | Name of the source text file              |
| 'Document'       | Raw text from the file                    |
| 'Text'           | Preprocessed text (cleaned and normalized)|
| 'Tokens'         | Tokenized words                           |
| 'Lemmas'         | Lemmatized tokens                         | 
| 'Parts-of-speech'| POS tags for tokens                       |

## Quality Checks

Spot checks were conducted to ensure accuracy in tokenization and lemmatization.
However, NER accuracy remains an area for improvement due to the limitations of the pre-trained models used(both small and large).

## Other Notes

For reproducibility, all preprocessing and annotation steps are included in the Jupyter Notebook.
Researchers and developers are encouraged to adapt and refine the annotations to suit their specific needs.

## Creator 

This dataset was created and curated by Theodora-Stavroula Korma on behalf of the course Collecting Data, for the MA Digital Humanities. 

**Contact Information**:
email: t.s.korma@student.rug.nl

## Usage
This dataset is provided for educational purposes, intended to support the 2nd assignment for the course **Collecting Data**, of 1b semester of MA Digital Humanities. 
