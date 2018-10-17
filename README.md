# Logbuch Phonetik und Sprachverarbeitung

Dieses Logbuch bietet einen Überblick über das [Bachelor-Studienfach „Phonetik und Sprachverarbeitung“](https://www.phonetik.uni-muenchen.de/studium_lehre/abschluesse/bachelor/index.html) an der [Ludwig-Maximilians-Universität München](https://www.lmu.de/).

Das Logbuch wird laufend von den Mitarbeiter*innen des [Instituts für Phonetik und Sprachverarbeitung](https://www.phonetik.uni-muenchen.de) editiert.

Die initiale Erstellung des Logbuchs wurde 2016 im Rahmen des Multiplikatoren-Projekts durch den Qualitätspakt Lehre ([Lehre@LMU](https://www.uni-muenchen.de/studium/lehre_at_lmu/index.html)) gefördert. Das Multiplikatoren-Projekt ist an das [LMU Center for Leadership and People Mangement angegliedert](https://www.peoplemanagement.uni-muenchen.de/index.html). Der Qualitätspakt Lehre wird aus Mitteln des Bundesministeriums für Bildung und Forschung unter dem Förderkennzeichen 01PL12016 gefördert. Die Verantwortung für den Inhalt dieser Veröffentlichung liegt bei den Autor*innen.

## Kompilieren

Das Logbuch ist in LaTeX gesetzt und kann mit einem beliebigen Latex-Editor oder zum Beispiel mit dem folgenden Kommandos kompiliert werden:

```sh
$ mkdir build
$ pdflatex -output-directory build main.tex
```

## GitBook kompilieren

```sh
find kapitel/ -name "*.tex" -exec pandoc "{}" -t gfm -o "{}.md" ";"
find kapitel/ -name "*.md" -exec sed -e 's/grafiken\//\/grafiken\//g' -i "" "{}" ";"
gitbook serve # or gitboook build
```
