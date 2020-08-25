# mixtec-multilingual-corpus
Ugur Yavuz, August 2020

This is a Mixtec-Spanish-English multilingual corpus I compiled during my internship at the [Natural Language Group @ ISI](https://nlg.isi.edu/) under the supervision of Dr. Jonathan May.

The corpus contains sentences from more than 20 varieties of Mixtec into English and Spanish. This corpus was originally compiled by a team of researchers from UNAM [(Montaño et al., 2019)](https://www.semanticscholar.org/paper/A-Mixtec-Spanish-Parallel-Corpus-Monta%C3%B1o-Sierra/391a89b6f373a9b28e96aac39ee241f808de9d82), whose work is available [online](http://www.geco.unam.mx/concordance_paralle). I gathered the documents by querying this database, scraped their metadata, cleaned them and translated the Spanish ones into English.

## Important

* You should install [Git LFS](https://git-lfs.github.com/) in order to be able to download all the files in the corpus. After installation, make sure you have set up Git LFS for your user account by running ``git lfs install``.

## Structure

* ``corpus/csv``: contains the entire corpus in ``.csv`` format. The corresponding fields are:
  * ``English``, ``Spanish``, ``Mixtec``: the 3 translations
  * ``ES-Document``, ``MX-Document``: Spanish (=English) and Mixtec document names
  * ``Line``: line number within document
  * ``Classification``: text type classification (religious, political etc.)
  * ``Mixtec ISO``: ISO code of the relevant Mixtec variety
* ``corpus/plaintext``: contains the entire corpus in plaintext, with no metadata.
* ``documents``: contains all documents.
* ``metadata/documents.csv``: metadata about all documents.
* ``metadata/pairs.csv``: all document pairings (i.e. variants of the same document, in both Spanish and Mixtec)

## Notes

* Certain Spanish documents have multiple variants, and many Mixtec documents have numerous [varieties](https://en.wikipedia.org/wiki/Classification_of_Mixtec_languages). In consideration of this, I created two versions of the corpus: files that begin with the prefix ``single`` use a single Spanish variant/Mixtec variety pairing (Spanish documents are prioritized alphabetically, and Mixtec varieties are prioritized by frequency in corpus), and files that begin with ``cross`` use the cross product between all Spanish variants and Mixtec varieties, meaning that the same document can be repeated many times.

* The version of the corpus annotated ``single`` contains 18397 distinct tokens and 11728 sentences. ``cross`` contains 69956 distinct tokens and 273699 sentences.
