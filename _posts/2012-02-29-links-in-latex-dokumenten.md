---
layout: post
permalink: links-in-latex-dokumenten
title: Links in LaTeX-Dokumenten
date: '2012-02-29 12:24:57 +0100'
tags:
- fachseminar
- latex
---
<p>Mit dem Paket <em>hyperref</em> wird es in LaTeX möglich Sprungmarken zu aktivieren, so dass man in einem PDF-Reader direkt zu zu Kapiteln oder Seiten springen kann. Das gleiche Paket ermöglicht auch Hyperlinks zu externen URLs zu definieren.</p>
<p>Die Verwendung des Pakets mit den Standardeinstellungen hat aber eine unschöne Eigenschaft: Links werden mit hässlichen Kästen markiert.</p>
<p><img class="alignnone size-medium wp-image-975" src="/uploads/2012/02/hyperref-defaults-500x144.png" alt="LaTeX Paket hyperref mit Standardeinstellungen" width="500" height="144" /></p>
<p>Mit <a href="http://www.tug.org/applications/hyperref/manual.html#x1-120003.8">wenigen Einstellungen</a> lässt sich das aber beheben:</p>

    \usepackage{hyperref} % hyperref Paket aktivieren
    \usepackage[usenames,dvipsnames]{xcolor} % Zusätzliche Farbdefinitionen laden
    \hypersetup { % Verhalten von hyperref anpassen
    bookmarks=true, % Kapitelsprunkmarken aktivieren
    colorlinks=true, % Links einfärben (und nicht umranden)
    linkcolor=NavyBlue, % Farbe für Links
    citecolor=NavyBlue, % Farbe für Links zum Literaturverzeichnis
    urlcolor=NavyBlue % Farbe für URLs

<p>So erhält man angenehme lesbare Links, auch zu externen URLs.</p>
<p><img src="/uploads/2012/02/hyperref-nice-500x107.png" alt="LaTeX Paket hyperref mit angepassten Einstellungen" title="hyperref-nice" width="500" height="107" class="alignnone size-medium wp-image-980" /></p>
