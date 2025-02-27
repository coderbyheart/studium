---
layout: post
permalink: codingstandards
title: Codingstandards
excerpt: "<a href=\"http://www.flickr.com/photos/tacker/sets/72157626379556132/\"><img
  class=\"alignright\" src=\"http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg\"
  alt=\"What The Foto?\" /></a>Für das Projekt haben wir uns auf Codingstandards geeignet,
  die wir mit Hilfe von <a href=\"http://cobertura.sourceforge.net/\">Cobertura</a>
  auch in Eclipse und in der Continuous Integration überprüfen.\r\n\r\nDa mit Cobertura
  auch Tests auf Basis von regulären Ausdrücken ausgeführt werden können, konnten
  wir auch den C#-Quellcode des Frontendteams zumindest rudimentären Tests unterziehen.
  Unsere Cobertura-Checks finden sich <a href=\"/svn/WTF/codingstandards/cobertura/\">hier</a>.
  \r\n"
date: '2011-06-24 22:13:09 +0200'
tags:
- SoftwareTechnik
- WhatTheFoto
---
<p><a href="http://www.flickr.com/photos/tacker/sets/72157626379556132/"><img class="alignright" src="http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg" alt="What The Foto?" /></a>Für das Projekt haben wir uns auf Codingstandards geeignet, die wir mit Hilfe von <a href="http://cobertura.sourceforge.net/">Cobertura</a> auch in Eclipse und in der Continuous Integration überprüfen.</p>
<p>Da mit Cobertura auch Tests auf Basis von regulären Ausdrücken ausgeführt werden können, konnten wir auch den C#-Quellcode des Frontendteams zumindest rudimentären Tests unterziehen. Unsere Cobertura-Checks finden sich <a href="{{ '/svn/WTF/codingstandards/cobertura/' | prepend: site.baseurl | prepend: site.url }}">hier</a>.<br />
</p>
<h3 class="textimage">Coding-Standards für Quellcode</h3>
<ul>
<li>Zeilenenden: Unix</li>
<li>Codierung: UTF-8</li>
<li>Einrückung:
<ul>
<li>Backend: Tab (<strong>kein</strong> Tab vor Code auf oberster Ebene)</li>
<li>Frontend: Space (<strong>kein</strong> Space vor Code auf oberster Ebene)</li>
</ul>
</li>
<li>Code-Dokumentation
<ul>
<li>Jede Quellcode-Datei <strong>muss</strong> mindestens den Namen des Autors enthalten</li>
<li>Jede Klassen-Deklaration <strong>muss</strong> mindestens den Namen des Autors enthalten</li>
<li>Methoden-Deklarationen <strong>sollten</strong> den Namen des Autors enthalten. Wenn alle Methoden einer Klasse von einem Autor erstellt wurden, kann dieser Hinweis entfallen.</li>
<li>bei mehreren Autoren, oder Erweiterungen durch eine zweite Person wird die Liste der Autoren erweitert</li>
<li>es darf ein selbstgewähltes Kürzel verwendet werden, dieses Kürzel <strong>muss</strong> in der Datei AUTHORS im Projekt-Root beschrieben werden</li>
<li>Sprache der Code-Dokumentation: <strong>deutsch</strong> oder <strong>englisch</strong></li>
</ul>
</li>
<li>Identifier werden <strong>englisch</strong> benannt.</li>
</ul>
<h3 class="textimage">Coding-Standards für Commit-Kommentare</h3>
<p>Zu jedem Commit <strong>muss</strong> es ein aussagekräftiges Kommentar geben.</p>
<p><em>Schlechte</em> Beispiele sind z.B.:</p>
<ul>
<li>Fix</li>
<li>Blubb</li>
<li>.</li>
</ul>
<p><em>Gute</em> Beispiele sind z.B.:</p>
<ul>
<li>Behebe Darstellungsfehler in der Tabellen-Komponente. See #8.</li>
<li>Korrigiere Syntaxfehler. Fixes #9.</li>
<li>Neue Methode zum Rotieren von Bildern dazu. See #10.</li>
</ul>
<h3 class="textimage">Referenzen auf Tickets</h3>
<p>Noch besser ist die Verwendung von Referenzen auf Tickts in den Kommentaren.</p>
<p>Trac erkennt dabei eine bestimmte Syntax in den Kommentaren, die <a href="http://trac.edgewall.org/wiki/CommitTicketUpdater"> hier</a><br />
erläutert ist, und fügt einen Verweis in den Kommentaren zum jeweiligen<br />
Ticket ein.</p>
<p>Beispiel:</p>
<ul>
<li>Behebe Darstellungsfehler in der Tabellen-Komponente. See #8, #9, #11</li>
<li>Korrigiere Syntaxfehler. Fix #4</li>
<li>Neue Methode zum Rotieren von Bildern dazu. See #18 and #19</li>
</ul>
<p>Der große Vorteil davon ist, dass man zu jedem Commit automatisch den Verweis auf das Ticket mit der Aufgabenbeschreibung hat und in jedem Ticket die Commit-History zu sehen ist.</p>
<p>Mit der <a href="http://www.eclipse.org/mylyn/"> Mylyn</a>-Integration von Trac bekommt man dann auch fremde Commits an seinen eigenen Tickets mit.</p>
<p><a href="http://tasktop.com/videos/mylyn/webcast-mylyn-3.0.html"> Webinar zur Verwendung von Mylyn</a>.</p>
<h3 class="textimage">Änderungen am Quellcode</h3>
<p>Zu jeder Änderung <strong>muss</strong> es ein Ticket geben, auf das beim committen referenziert werden <strong>muss</strong>.</p>
<p>Ist so ein Ticket nicht vorhanden, muss dieses angelegt werden.</p>
<p>Änderungen am Quellcode, der zu einem anderen Team gehört, ohne Absprache mit dessen Teamleiter sind nicht erlaubt.</p>
<p>Wenn es Probleme mit der Implementieren des anderen Teams gibt, gibt es zwei Möglichkeiten, eine Änderung / Anpassung des Codes zu bewirken:</p>
<ol>
<li>Einen Bug zu melden</li>
<li>Ihr macht euch eine Kopie des Codes via svn copy und bearbeitet diese. Anschließen kann der geänderte Code vom zuständigen Team wieder integriert werden.</li>
</ol>
