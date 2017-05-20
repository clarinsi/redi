# REDI
Diacritic restoration tool for Croatian, Serbian and Slovene

The tool expects tokenised / verticalised text. If not defined differently, the last column will be rediacritised.

```
$ echo 'Jucer nisam bio u skoli' | ../reldi-tokeniser/tokeniser.py hr | ./redi.py hr
1.1.1.1-5	Jucer	Jučer
1.1.2.7-11	nisam	nisam
1.1.3.13-15	bio	bio
1.1.4.17-17	u	u
1.1.5.19-23	skoli	školi

```

There is an option for using large language models for contextual disambiguation. You can download the models from

* http://nlp.ffzg.hr/data/reldi/wikitweetweb.hr.bin (15G)
* http://nlp.ffzg.hr/data/reldi/wikitweetweb.sr.bin (7.7G)
* http://nlp.ffzg.hr/data/reldi/wikitweetweb.sl.bin (8.3G)

If you have the language models in your working directory, you can disambiguate in context by adding the ```-l``` flag.

## Dependencies

* pypi-kenlm
