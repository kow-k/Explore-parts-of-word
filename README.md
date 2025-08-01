# Extracting formal components of word

Data and scripts for analysis used for Unsupervised extraction of components of word spell and pronunciation,

# Scripts for data analysis

Scripts for analysis. word-level analysis only

1. [character $n$-gram-based "parts-of-word" extraction](explore-parts-of-word.ipynb)

Running was confirmed on Python 3.10, 3.11, and 3.12.

## Important Parameters:

0. **doc_type** [string]: either "spell" or "sound"
1. **max_doc_size** [integer]: maximum character length for docs to process
2. **min_doc_size** [integer]: minimum character length for docs to process
3. **target_lang_key** [string]: a selector for target language name
4. **selects_word_class** [boolean]: flag for POS-aware processing
5. **selects_gender** [boolean]: flag for gender-aware processing
6. **source_sampling** [boolean]: a flag to perform sampling

Other paramers used are not recommended to modify. Do so at your own risk.

## Prerequisites

Needed Python packages

possibly Cython

# Data

## English

1. [English spell/sound pairs (.csv) from open-dict-ipa](data/open-dict-ipa/data1/en_US.csv.gz)
2. [English noun spell/sound pairs (.csv) from wn3 x open-dict-ipa](data/wn3/en_N_only.csv)
3. [English verb spell/sound pairs (.csv) from wn3 x open-dict-ipa](data/wn3/en_V_only.csv)
4. [English adjective spell/sound pairs (.csv) from wn3 x open-dict-ipa](data/wn3/en_A_only.csv)
5. [English adverb spell/sound pairs (.csv) from wn3 x open-dict-ipa](data/wn3/en_R_only.csv)
6. [English noun spells (.csv) from wn3](data/wn3/en_N_only.csv)
7. [English verb spells (.csv) from wn3](data/wn3/en_V_only.csv)
8. [English adjective spells (.csv) from wn3](data/wn3/en_A_only.csv)
9. [English adverb spells (.csv) from wn3](data/wn3/en_R_only.csv)

Data 6, 7, 8 and 9 are class-wise extractions from [WordNet 3](http://wordnet.princeton.edu/).

Data 2, 3, 4 and 5 are the reduced/filtered versions of data 6, 7, 8 and 9, whereby spells are paired with IPA symbols in open-dict-ipa [en_US.csv](data/open-dict-ipa/data1/en_US.csv.gz).

The "data1" directory is a copy of the directory of the same name provided at [open-dict-ipa](https://github.com/open-dict-data/ipa-dict).

## German

1. [German words](data/open-dict-ipa/data1/de.csv.gz)
2. [German nouns](data/open-dict-ipa/data1a/de_N_only.csv.gz)
3. [German non-nouns](data/open-dict-ipa/data1a/de_non_N_only.csv.gz)

The classfication between nouns and non-nouns is made (too) simply in that nouns are those words that start with a capital letter and non-nouns are those that do not, without using any lexcial resources.

## Irish

1. [Irish adjectives (spell)](data/irish/irish-spell-A_only.csv)
1. [Irish nouns (spell)](data/irish/irish-spell-N_only.csv)
1. [Irish verbs (spell)](data/irish/irish-spell-V_only.csv)

# Results

[English major parts of spell (A, N, V)](results/English/spell)
[English major parts of spell (A, N, V)](results/English/sound)

[German major parts of spell (N vs non_N)](results/Germa/spell/)
[German major parts of sound (N vs non_N)](results/Germa/sound/)

[Irish major parts of spell (A, N, V)](results/Irish/spell)
