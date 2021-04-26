# How Domain Terminology Affects Meeting Summarization Performance

We provide annotated domain terminology for the COLING 2020 paper ["How Domain Terminology Affects Meeting Summarization Performance"](https://arxiv.org/abs/2011.00692). If you find the information useful, please cite the following:

    @inproceedings{koay-etal-2020-domain,
        title = {How Domain Terminology Affects Meeting Summarization Performance},
        author = {Jia Jin Koay and Alexander Roustai and Xiaojin Dai and Dillon Burns and Alec Kerrigan and Fei Liu},
        booktitle = {Proceedings of the 28th International Conference on Computational Linguistics},
        year = {2020}}

## Domain Terminology

We solicit annotations from undergraduate students majoring in computer science and designate words and expressions that are beyond the scope of their knowledge as domain terminology. The annotators are able to annotate all of the 75 ICSI meetings for jargon terms. The unique jargon terms for each file are provided. Below is a snippet of the human transcript with domain terminology shown in bold. The original meeting transcripts can be downloaded [here](http://groups.inf.ed.ac.uk/ami/icsi/download/). 

__Start__ | __End__ | __Spoken Utterance__
-- | -- | --
247.255 | 252.672 | with Andreas' help um Andreas put together a sort of no frills recognizer which is uh
252.672 | 258.837 | gender-dependent but like no adaptation, __no cross-word models, no trigrams - a bigram recognizer__
258.837 | 262.221 | and that's trained on __Switchboard__ which is telephone conversations.
263.983 | 267.154 | and thanks to Don's help wh- who - Don took
267.154 | 270.431 | the first meeting that Jane had transcribed
270.431 | 277.520 | and um you know separated - used the individual channels we segmented it in- into the segments that Jane had used
277.520 | 279.952 | and uh Don sampled that so -
281.374 | 289.611 | um and then we ran up to I guess the first twenty minutes, up to __synch time__ of one two zero zero so is that - that's twenty minutes or so?
289.611 | 296.601 | Um yeah because I guess there's some, and Don can talk to Jane about this, there's some bug in __the actual synch time file__ that

## Errata

The ROUGE scores reported in this paper were obtained by running [pyrouge] (https://pypi.org/project/pyrouge/) against a single human reference summary using ROUGE options `-c 95 -n 2 -a -s -m -2 4 -u`, where `-s` indicates stopwords are removed from system and reference summaries. It was later found that the scores for the ASR summaries were obtained by running pyrouge against three human reference summaries. We report the corrected ASR results run on the single human reference summary (with stopwords removed) below.

We additionally report the results for the system summaries (human and ASR) obtained by running pyrouge against three human references, with stopwords not removed below.

Original ASR results in COLING paper (3 human references, stopwords removed):



| | R-1 P(%) | R-1 R(%) | R-1 F(%) | R-2 P(%) | R-2 R(%) | R-2 F(%) | R-SU4 P(%) | R-SU4 R(%) | R-SU4 F(%)
-- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | --
ASR | Ours (w/o Jargon) | 41.7 | 55.1 | 46.8 | 15.1 | 20.5 | 17.2 | 18.7 | 25.3 | 21.3
| Ours (w/ Jargon) | 39.7 | 57.5 | 46.6 | 15.1 | 21.9 | 17.7 | 18.2 | 26.5 | 21.4


Updated ASR results (single human reference, stopwords removed):

Additional results with three human reference summaries, stopwords not removed:


