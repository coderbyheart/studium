---
layout: post
permalink: ticket-workflow
title: Ticket-Workflow
excerpt: "<a href=\"http://www.flickr.com/photos/tacker/sets/72157626379556132/\"><img
  class=\"alignright\" src=\"http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg\"
  alt=\"What The Foto?\" /></a>Nachfolgend findet sich der offizielle Ticket-Workflow
  für unser Projekt.\r\n\r\nEinige der Angaben sind <a href=\"http://trac.edgewall.org/\">Trac</a>-spezifisch,
  können aber leicht auch in anderen Tools zur Softwareverwaltung implementiert werden.\r\n\r\nDer
  Prozess zur Qualitätssicherung wurde bei uns mit <em>Keywords</em> realisiert &mdash;
  besser wäre natürlich die Verwendung des <a href=\"http://trac.edgewall.org/wiki/TracWorkflow\">eigenen
  Workflows von Trac</a> gewesen, da wir aber in der Hochschule keinen Einfluss auf
  die trac.ini haben, war das leider nicht möglich.\r\n"
date: '2011-06-26 11:36:10 +0200'
tags:
- SoftwareTechnik
- WhatTheFoto
---
<p><a href="http://www.flickr.com/photos/tacker/sets/72157626379556132/"><img class="alignright" src="http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg" alt="What The Foto?" /></a>Nachfolgend findet sich der offizielle Ticket-Workflow für unser Projekt.</p>
<p>Einige der Angaben sind <a href="http://trac.edgewall.org/">Trac</a>-spezifisch, können aber leicht auch in anderen Tools zur Softwareverwaltung implementiert werden.</p>
<p>Der Prozess zur Qualitätssicherung wurde bei uns mit <em>Keywords</em> realisiert &mdash; besser wäre natürlich die Verwendung des <a href="http://trac.edgewall.org/wiki/TracWorkflow">eigenen Workflows von Trac</a> gewesen, da wir aber in der Hochschule keinen Einfluss auf die trac.ini haben, war das leider nicht möglich.<br />
<a id="more"></a><a id="more-599"></a></p>
<h3 class="textimage">Ein Ticket für jede Änderung</h3>
<p>Wie in <a href="/codingstandards">Codingstandards</a> beschrieben, muss es für jede Änderungen am Quellcode, also für jeden Commit ein Ticket geben, dass mittels des Commit-Kommentaresreferenziert wird.</p>
<h3 class="textimage">Ein neues Ticket anlegen</h3>
<p>Um ein neues Ticket an zu liegen klickt man rechts oben in der Hauptnavigation auf <em>New Ticket</em> und füllt das Formular aus.</p>
<p>In der Liste der WorkPackages finden sich ebenfalls bei jedem <a href="https://scm.mi.hs-rm.de/trac/2011swtpro/2011swtpro01/wiki/WorkPackage">WorkPackage</a> zwei Links, zum Anlegen von neuen Tickets. Verwendet man diesen Link, werden Meilenstein, Komponente, CC und Owner des jeweiligen <a href="/leuchttisch-entwicklertagebuch-03#workpackages">WorkPackages</a> übernommen und das Feld Keywords mit dem Verweis, auf das WorkPackage belegt.</p>
<p>Eine sinnvolle und allgemein verständliche Beschreibung der Aufgabe bzw. des Fehlers ist hier besonders wichtig. Trac bietet zur Strukturierung einer Beschreibung umfangreiche Formatierungsmöglichkeiten, die in <a href="http://trac.edgewall.org/wiki/WikiFormatting">WikiFormatting</a> erläutert sind.</p>
<p>Gut ist es auch, wenn man die Beschreibung mit Verweisen mit Querverweisen, z.B. zum Quellcode ergänzen kann, wie das geht, ist in <a href="http://trac.edgewall.org/wiki/TracLinks">TracLinks</a> erklärt.</p>
<h3 class="textimage">Ticket einer Person zuweisen</h3>
<p>Wenn man sich sicher ist, wer sich um das Ticket kümmern soll, kann man das Ticket einer Person zu weisen.</p>
<p>Hierzu wählt man im Ticket um Formular in dem DropDown <em>Modify Ticket</em> ganz unten die Option <em>reassign to</em> und trägt im Feld dort den Nutzernamen oder die E-Mail-Adresse der jeweiligen Person ein.</p>
<p>Das kann man auch schon beim Anlegen eines Tickets machen, in dem man den Nutzernamen oder die E-Mail-Adresse der jeweiligen Person im Feld <em>owner</em> einträgt.</p>
<h3 class="textimage">Ticket annehmen</h3>
<p>Im DropDown <em>Modify Ticket</em> findet sich ganz unten die Option <em>accept</em>. Diese Aktion hat nur eine symbolische Bedeutung, der Besitzer des Tickets wird auf den aktuell eingeloggten Benutzer geändert sowie der Status auf <em>accepted</em> gesetzt.</p>
<p>Die Aussage ist aber sehr hilfreich, so bekommen andere Beobachter des Tickets mit, das an der Aufgabe gearbeitet wird.</p>
<p>Auch kann man so in der Liste aller Tickets sehen, woran gerade am gesamten Projekt gearbeitet wird.</p>
<h3 class="textimage">Ticket bearbeiten</h3>
<p>Die Bearbeitung eines Tickets sollte unbedingt lückenlos dokumentiert werden.</p>
<p>Gerade im Hinblick auf die Qualitätssicherung (s.u.) ist es notwendig, den Vorgang zur Lösung des Tickets auch für Dritte nachvollziehbar zu machen.</p>
<p>Im Zweifel sind ausführlichere Kommentare kurzen Hinweisen vor zu ziehen.</p>
<p>Bei Änderungen am Quellcode sind die in den <a href="/codingstandards">CodingStandards</a> festgelegten Prozesse zu verwenden. Insbesondere sei hier auf die Abschnitte <em>Commit-Kommentare</em> und <em>Änderungen am Quellcode</em> verwiesen.</p>
<p>Ist die Bearbeitung eines Tickets abgeschlossen, wird dieses an die Qualitätsicherung übergeben. Hierzu ergänzt man im Feld <em>keywords</em> das Keyword <em>qs-me</em>. Offene Tickets, die auf Qualitätsicherung warten, werden auf der Startseite oder in mit Hilfe eines Queries aufgelistet.</p>
<h3 class="textimage">Qualitätsicherung</h3>
<p>Qualitätsicherung bedeutet, dass eine zweite Person die Lösung eines Tickets kontrolliert. Hier ist es in den meisten Fällen ausreichend, zu überprüfen, ob der betroffene Teil dasmacht, was beabsichtigt war.</p>
<p>Zur Qualitätsicherung gehört auch das Kontrollieren der Änderungen auf mögliche Fehler, Unschönheiten und Mißverständnisse. Das Durchsehen des Diffs der Änderungen bietet hierzu schon einen guten Einstieg.</p>
<p>Ist man mit der Umsetzung zufrieden, schreibt man dieses als Kommentar zu dem Ticket und ergänzt im Feld <em>keywords</em> das Keyword <em>qs-ok</em>.</p>
<p>Nun kann das Ticket geschlossen werden.</p>
<h3 class="textimage">Ticket schließen</h3>
<p>Nachdem ein Ticket vollständig erledigt wurde, und auch die Qualitätsicherung zufrieden ist, kann ein Ticket geschlossen werden.</p>
<p>Nun ist es Zeit, ein Bier zu trinken.</p>
