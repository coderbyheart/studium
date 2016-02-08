---
layout: post
status: publish
published: true
title: Links in LaTeX-Dokumenten
author:
  display_name: Markus Tacker
  login: m
  email: m@tacker.org
  url: http://tckr.cc/
author_login: m
author_email: m@tacker.org
author_url: http://tckr.cc/
wordpress_id: 973
wordpress_url: http://studium.coderbyheart.de/?p=973
date: '2012-02-29 12:24:57 +0100'
date_gmt: '2012-02-29 10:24:57 +0100'
categories:
- Uncategorized
tags:
- fachseminar
- latex
comments: []
---
<p>Mit dem Paket <em>hyperref</em> wird es in LaTeX möglich Sprungmarken zu aktivieren, so dass man in einem PDF-Reader direkt zu zu Kapiteln oder Seiten springen kann. Das gleiche Paket ermöglicht auch Hyperlinks zu externen URLs zu definieren.</p>
<p>Die Verwendung des Pakets mit den Standardeinstellungen hat aber eine unschöne Eigenschaft: Links werden mit hässlichen Kästen markiert.</p>
<p><img class="alignnone size-medium wp-image-975" src="http://studium.coderbyheart.de/wp-content/uploads/2012/02/hyperref-defaults-500x144.png" alt="LaTeX Paket hyperref mit Standardeinstellungen" width="500" height="144" /></p>
<p>Mit <a href="http://www.tug.org/applications/hyperref/manual.html#x1-120003.8">wenigen Einstellungen</a> lässt sich das aber beheben:</p>
<p>[cc lang=latex]<br />
\usepackage{hyperref} % hyperref Paket aktivieren<br />
\usepackage[usenames,dvipsnames]{xcolor} % Zusätzliche Farbdefinitionen laden<br />
\hypersetup { % Verhalten von hyperref anpassen<br />
bookmarks=true, % Kapitelsprunkmarken aktivieren<br />
colorlinks=true, % Links einfärben (und nicht umranden)<br />
linkcolor=NavyBlue, % Farbe für Links<br />
citecolor=NavyBlue, % Farbe für Links zum Literaturverzeichnis<br />
urlcolor=NavyBlue % Farbe für URLs<br />
}<br />
[/cc]</p>
<p>So erhält man angenehme lesbare Links, auch zu externen URLs.</p>
<p><img src="http://studium.coderbyheart.de/wp-content/uploads/2012/02/hyperref-nice-500x107.png" alt="LaTeX Paket hyperref mit angepassten Einstellungen" title="hyperref-nice" width="500" height="107" class="alignnone size-medium wp-image-980" /></p>
