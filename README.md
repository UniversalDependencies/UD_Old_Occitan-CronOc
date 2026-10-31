# Summary

This is the first version of the CronOc (Corpus of Occitan Chronicles), created as part of [BREAKTHROUGH project](https://crisco.unicaen.fr/projet-breakthrough/).

Please note that CronOc treebank is still under development. A campaign of revision and morphological annotation is underway and new material is being added to the collection. The structure of the treebank is therefore likely to change in subsequent releases. Please do not hesitate to contact us if you have any questions, suggestions or comments.

# Introduction

The corpus currently contains one text, late-thirteenth-century Old Languedocian version of [_Gesta Caroli Magni as Carcassonam et ad Narbonam_](https://www.arlima.net/mp/notre_dame_de_lagrasse.html), known as [_Le Roman de Lagrasse_, or _Le roman de Philomena_](https://www.arlima.net/mp/notre_dame_de_lagrasse/oc_le_roman_de_philomena.html). This is a medieval prose chronicle narrating the legendary events of the foundation of the [Notre Dame de Lagrasse abbey](https://fr.wikipedia.org/wiki/Abbaye_Sainte-Marie_de_Lagrasse) by Emperor Charlemagne.

Two medieval (14th century) manuscripts of the _Roman de Lagrasse_ are extant: the A manuscript (Aix-en-Provence, Biliothèque Méjane, 424 (143)) that lacks the beginning and the end, and the B manuscript (London, BL, Add. 21218) that has the complete text.

Two editions of the _Roman de Lagrasse_ exist:

Schneegans, Fréderic-Edouard (1898) _Gesta Karoli Magni ad Carcassonam et Narbonam. Lateinischer Text und provenzalische Übersetzung mit Einleitung_. Halle: Niemeyer (Romanische Bibliothek, 15).

﻿Simonnet, Émile Jean (1987) _Édition critique du Roman de Notre-Dame de Lagrasse_. PhD Thesis, Université de Paris IV-Sorbonne. (Simonnet's edition and translation can be consulted [here](http://emile.simonnet.free.fr/sitfen/tabsom.htm)).

For CronOc corpus, we used the automatic transcription of the B manuscript from the [COMETA Corpus](https://zenodo.org/records/15300719) (Marinus Wiedner 2025) that was checked against the manuscript and manually segmented into sentences and tokens. Some corrections to the manuscript readings were introduced that are indicated in the MISC column (original=).


# Data Split

| Source | Train (sent) | Train (tok) | Dev (sent) | Dev (tok) | Test (sent) | Test (tok) | Total (sent) | Total (tok) |
|--------|--------------|-------------|------------|-----------|-------------|------------|--------------|-------------|
| Lagrasse | 1229 | 24,500 | 167 | 2,726 | 452 | 10,001 | 1848 | 37,227 |
| Total | 1229 | 24,500 | 167 | 2,726 | 452 | 10,001 | 1848 | 37,227 |

| Split | Sentences | Tokens | % (tokens) |
|-------|-----------|--------|------------|
| train | 1,229 | 24,500 | 65.8% |
| dev | 167 | 2,726 | 7.3% |
| test | 452 | 10,001 | 26.9% |
| total | 1,848 | 37,227 | 100.0% |

The split was created using scripts that can be consulted [here](https://github.com/Corpus-Diachroniques-CRISCO/CorAG_tools).

# Annotation

The corpus was automatically annotated with [BertForDeprel](https://github.com/kirianguiller/BertForDeprel) on [ArboratorGrew](https://arborator.grew.fr/#/) portal and was subsequently manually checked. The first model was trained on the [CorAG](https://github.com/UniversalDependencies/UD_Old_Occitan-CorAG) corpus for Old Gascon and was subsequently adapted to the CronOc data using bootstrapping methodology ([Peng et al 2022](https://hal.science/hal-03846834/document), see also [Romanova et al 2025a](https://lift2-2025.sciencesconf.org/667164) and [Romanova et al 2025b](https://zenodo.org/records/17737727)).

The texts are annotated in PoS and syntactic functions (Universal Dependencies), following, wherever possible, the guidelines for Modern Occitan ([Miletić et al 2020](https://hal.science/hal-04925754v1)).

**Features**

Verbs and auxiliaries have been annotated in verb forms (VerbForm): Inf (infinitive), Fin (conjugated) and Part (participle). Conjugated forms are annotated in Person (1,2,3), Number (Sing, Plur), Mood (Ind, Cdn, Sub, Imp) and Tense (Past, Present). For compound tenses, each token is annotated individually.

Participles are annotated in Tense (Past, Pres). Please note that past participles without dependents are annotated as adjectives but are also provided with morphological features of participles (VerbForm, Tense).

Pronouns are annotated in type (PronType: Prs, Dem, Ind, Int, Rel). Reflexive pronouns are annotated as Prs with an additional Reflexive=Yes feature. Possessive pronouns do not have a PronType feature but have the feature Poss=Yes.

Personal pronouns are annotated in Person (1,2,3) and, wherever possible, Number (Sing, Plur), Gender (Masc, Fem, Neut). Neut is used for the pronoun "o".

Demonstrative pronouns, wherever possible, are annotated in Number (Sing, Plur) and Gender (Masc, Fem). 

Indefinite pronouns are annotated, wherever possible, in Number (Sing, Plur) and Gender (Masc, Fem).

Relative pronoun have no further morphological annotation at present.

Tokens with negative polarity (that belong to ADJ, ADP, ADV, CCONJ, DET and PRON categories) have Polarity=Neg feature.

# Lemmatization

With the exception of proper names that remain unlemmatized, the corpus was lemmatized manually using _lemmata_ from the [DOM-en-ligne](https://dom-en-ligne.de/) lemmata. For pronouns and determiners, we used singular masculine forms as lemmata. 

# Acknowledgments

The treebank is being created as part of the [BREAKTHROUGH project](https://crisco.unicaen.fr/projet-breakthrough/), led by Professor [Pierre Larrivée](https://www.researchgate.net/profile/Pierre-Larrivee-2) at the CRISCO Lab, University of Caen ([CaeSAR](https://caesar-project.unicaen.fr/) project, reference ANR-23-EXES-0001).

Data annotation and lemmatisation was performed by [Natasha Romanova](https://cv.hal.science/natasha-romanova). Technical support: [Rayan Ziane](https://cv.hal.science/rayan-ziane).

We thank [Barbara Francioni](https://cv.hal.science/barbara-francioni) and [Barbara Vance](https://linguistics.indiana.edu/about/faculty/vance-barbara.html]) for their help.

## References

* (forthcoming)


# Changelog

* 2026-11-15 v2.19
  * Initial release in Universal Dependencies.


<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.19
License: CC BY-SA 4.0
Includes text: yes
Parallel: no
Genre: fiction
Lemmas: manual native
UPOS: manual native
XPOS: not available
Features: manual native
Relations: manual native
Contributors: Romanova, Natalia; Ziane, Rayan
Contributing: here
Contact: natalia.romanova@unicaen.fr
===============================================================================
</pre>
