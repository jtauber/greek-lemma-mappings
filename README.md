# greek-lemma-mappings

mappings between the headwords of various NT Greek lexicons, the lemmas of MorphGNT and Nestle 1904, and Strongs and GK numbers

Note that the focus of this repo is in data (and soon code) for mapping between lemmas and other identifiers for lexical items. It is not intended to be the home of glosses, definitions, morphological information, etc. Rather it is a Rosetta Stone of sorts to help integrate various resources with that information.


## License

This data is made available under a [CC-BY-SA 4.0 License](https://creativecommons.org/licenses/by-sa/4.0/).


## History

Back in 2006, Ulrik Sandborg-Petersen and I spent time integrating various Greek New Testament analyses we'd separately worked on. One output of that work was our joint paper [A New Numbering System for Greek New Testament Lexemes](https://www.academia.edu/19660777/A_New_Numbering_System_for_Greek_New_Testament_Lexemes_2006_). A few years later, as part of my larger work on a Morphological Lexicon of New Testament Greek, I started a broader integration of various lexical resources including BDAG, Danker's Concise Lexicon and even an old word list Bill Mounce had shared with me in 1997. A lot of the data and scripts for that work are in the [morphgnt/morphological-lexicon](https://github.com/morphgnt/morphological-lexicon) GitHub repo. But when it recently became clear many people were not aware of the existing work, I decided it was worth extracting lemma mapping data and code out of that repo (where it's easy for it be lost) and start a new repo with much more focus. This repo is the in-progress result.


## What's Here Now

The main file is `lexemes.yaml`. The keys in this file are the lemmas used by the [SBLGNT edition of the MorphGNT](https://github.com/morphgnt/sblgnt). The properties under each key are:

  * `full-citation-form` the canonical full citation form (with genitive and article for nouns, etc)
  * `bdag-headword` the corresponding headword in BDAG
  * `danker-entry` the corresponding full citation form from Danker's Concise Lexicon
  * `dodson-entry` the corresponding full citation form from Dodson's lexicon
  * `mounce-headword` the corresponding headword from the list Bill Mounce gave me in 1997 (I need to update this with his much more up-to-date data)
  * `abbott-smith-header` the corresponding headword from Abbott-Smith **NEW**
  * `abbott-smith-entry` the corresponding full citation form from Abbott-Smith **NEW** (probably has some extraneous info I need to manually remove)
  * `strongs` the corresponding strongs number
  * `gk`  the corresponding G/K number

There are also some additional mapping files (all derived from `lexemes.yaml`):

  * `alt_mapping.yaml` a mapping from alternative spellings to the key found in `lexemes.yaml`
  * `gk_mapping.yaml` a mapping from G/K number to the key found in `lexemes.yaml`
  * `strongs_mapping.yaml` a mapping from Strongs number fo the key found in `lexemes.yaml`

There is also an initial mapping for Nestle 1904 lemmas (via Strongs numbers) at `nestle-match.txt`.

`differences.yaml` and `NOTES.md` contain old notes from my work on this back in 2013. I need to work through them and update them.


## What's Planned

I need to look at more recent data from Mounce, sort out some of the mismatch issues with Nestle 1904, clean up the Abbott-Smith entries more, reintroduce a lot of the validation and utility code from before, integrate other headword lists such as LSJ and possible Brill, and eventually expand things to more GNT editions and a broader corpus of texts.


## Acknowledgements

Ulrik Sandborg-Petersen was my original collaborator on projects that ultimately led to this work. Jonathan Robie is responsible for building the community which has reinvigorated my interest in continuing this and much other work. Eliran Wong encouraged me immensely with his use of earlier versions of this work and the feedback he has given.


## Related Work

For more of my work on linguistics and Ancient Greek, see http://jktauber.com/.
