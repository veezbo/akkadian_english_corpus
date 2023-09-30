# Akkadian English Corpus
This dataset is a cleaned English-translated Akkadian language dataset. This dataset can and has been used for text generation tasks, for example to fine-tune LLMs.

## How it was generated
At a high level, these are steps that were taken:
- Sourced a high-quality dataset of English-translated Akkadian by experts
- Enforced a minimum line length
- Removed duplicate lines
- Removed textual notes and other generic notes within parantheses
- Inserted translation notes and literal notes in place (preserving grammar and adding clarity to the corpus)

For the exact details, please visit the [prepare_akkadian_english_corpus](https://github.com/veezbo/akkadian_english_corpus/blob/main/prepare_akkadian_english_corpus.ipynb) Jupyter notebook in this repo.

## Data
The raw data file can be found in the data folder in this repo for convenience: [english_translated_akkadian_corpus.txt](https://github.com/veezbo/akkadian_english_corpus/blob/main/data/english_translated_akkadian_corpus.txt)

Additionally, I converted this text file to a [HuggingFace dataset](https://huggingface.co/datasets/veezbo/akkadian_english_corpus) for even faster integration into existing training workflows. 

## Credit
Credit for the aggregation of the raw data belongs to the [Akkademia](https://github.com/gaigutherz/Akkademia/tree/master) project. Specifically, the exact data file used as the starting dataset is linked [here](https://github.com/gaigutherz/Akkademia/blob/master/NMT_input/train.en) and was also used to train their SOTA neural machine translation Akkadian->English model as described in their recent [paper](https://academic.oup.com/pnasnexus/article/2/5/pgad096/7147349) Gutherz et al. 2023 [1].

Credit for the original source of the raw data belongs to the incredible Open Richly Annotated Cuneiform Corpus ([ORACC](http://oracc.org)) project [2]. Specifically, as noted by the Akkademia project above, the RINAP 1, 3, 4, and 5 datasets are the source of the original raw data.

## Citations
[1] Gai Gutherz, Shai Gordin, Luis Sáenz, Omer Levy, Jonathan Berant, Translating Akkadian to English with neural machine translation, PNAS Nexus, Volume 2, Issue 5, May 2023, pgad096, https://doi.org/10.1093/pnasnexus/pgad096  
[2] Jamie Novotny, Eleanor Robson, Steve Tinney, Niek Veldhuis, et al. Open Richly Annotated Cuneiform Corpus, http://oracc.org
