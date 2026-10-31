# Summary

This is the first version of the CronOc (Corpus of Occitan Chronicles), created as part of [BREAKTHROUGH project](https://crisco.unicaen.fr/projet-breakthrough/).


# Introduction

The corpus currently contains one text, late-thirteenth-century Old Languedocian version of [_Gesta Caroli Magni as Carcassonam et ad Narbonnam_](https://www.arlima.net/mp/notre_dame_de_lagrasse.html), known as [Le Roman de Notre Dame de Lagrasse,__ _or _Le roman de Philomena_](https://www.arlima.net/mp/notre_dame_de_lagrasse/oc_le_roman_de_philomena.html). This is a medieval prose chronicle narrating the legendary events of the foundation of the [Notre Dame de Lagrasse abbey](https://fr.wikipedia.org/wiki/Abbaye_Sainte-Marie_de_Lagrasse) by Emperor Charlemagne.

Two medieval (14th century) manuscripts of the _Roman de Lagrasse_ are extant: the A manuscript (Aix-en-Provence, Biliothèque Méjane, 424 (143)) that lacks the beginning and the end, and the B manuscript (London, BL, Add. 21218) that has the complete text.

Two editions of the _Roman de Lagrasse_ exist:

Schneegans, Fréderic-Edouard (1898) _Gesta Karoli Magni ad Carcassonam et Narbonam. Lateinischer Text und provenzalische Übersetzung mit Einleitung_. Halle: Niemeyer (Romanische Bibliothek, 15).

﻿Simonnet, Émile Jean (1987) _Édition critique du Roman de Notre-Dame de Lagrasse_. Thèse de doctorat, Université de Paris IV-Sorbonne. (Simonnet's edition and translation can be consulted [here](http://emile.simonnet.free.fr/sitfen/tabsom.htm)).

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



# Acknowledgments

The treebank is being created as part of the BREAKTHROUGH project

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
