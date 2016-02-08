---
layout: post
permalink: latex-quickwin-tex-early-tex-often
title: 'LaTeX QuickWin: Tex early, tex often!'
date: '2012-04-13 17:40:21 +0200'
tags:
- latex
---
<p>Ähnlich wie beim <a href="http://en.wikipedia.org/wiki/Test-driven_development">Test-driven development</a> (<a href="http://amzn.to/GROBMv">Buchtipp!</a>) in der Softwareentwicklung sollte man beim Erstellen eines LaTeX-Dokumentes sich von Anfang an darum kümmern, ein funktionierendes Dokument zu erzeugen. Sehr hilfreich sind dabei Makefiles.</p>
<p>Die Fehlermeldung von LaTeX sind nämlich recht kryptisch. Liegt eine lange Zeit und viele Änderungen zwischen dem letzten funktionierenden Dokument, wird es zu einem Sisyphusaufgabe, die Stelle im Dokument zu finden, die den Fehler verursacht.</p>
<p>Ich habe mir angewöhnt, immer direkt zu texen, nachdem ich einen oder zwei Abschnitte geändert habe. Bei komplizierteren Strukturen wie Tabellen oder Abbildung texe ich noch öfter.</p>
<p>Eine make-Ausgabe wie</p>
<p><code>make: *** [Thesis.pdf] Fehler 1</code></p>
<p>am Ende der Ausgabe ist dann ein gut sichtbarer Hinweis auf einen Fehler.</p>
<p>Hier noch ein Makefile, wie ich es typischerweise für LaTeX-Projekte verwende:</p>
<p><code><br />
all: Thesis.pdf</p>
<p>Thesis.pdf: Thesis.tex parts/*.tex parts/*.bib<br />
        -xelatex -interaction=nonstopmode Thesis.tex<br />
        -bibtex Thesis.aux<br />
        -xelatex -interaction=nonstopmode Thesis.tex<br />
        xelatex -interaction=nonstopmode Thesis.tex</p>
<p>clean:<br />
        -/bin/rm *.lof *.log *.lot *.aux *.bbl *.toc *.blg *.dvi *~ *.out<br />
</code></p>
