---
layout: post
status: publish
published: true
title: Leuchttisch Entwicklertagebuch 03
author:
  display_name: Markus Tacker
  login: m
  email: m@tacker.org
  url: http://tckr.cc/
author_login: m
author_email: m@tacker.org
author_url: http://tckr.cc/
excerpt: "Willkommen zur dritten Ausgabe des <em>Leuchttisch</em>-Entwicklertagebuchs,
  in der ich die Ereignisse in der Zeit von Montag, den 4. bis Sonntag, den 10. April
  2011 beleuchten werde.\r\n"
wordpress_id: 494
wordpress_url: http://studium.coderbyheart.de/?p=494
date: '2011-04-11 17:51:38 +0200'
date_gmt: '2011-04-11 15:51:38 +0200'
categories:
- Uncategorized
tags:
- SoftwareTechnik
- WhatTheFoto
comments:
- id: 132
  author: Ticket-Workflow &laquo; Markus studiert!
  author_email: ''
  author_url: http://studium.coderbyheart.de/ticket-workflow
  date: '2011-07-28 12:55:42 +0200'
  date_gmt: '2011-07-28 10:55:42 +0200'
  content: "[...] Tickets. Verwendet man diesen Link, werden Meilenstein, Komponente,
    CC und Owner des jeweiligen WorkPackages übernommen und das Feld Keywords mit
    dem Verweis, auf das WorkPackage [...]"
---
<p>Willkommen zur dritten Ausgabe des <em>Leuchttisch</em>-Entwicklertagebuchs, in der ich die Ereignisse in der Zeit von Montag, den 4. bis Sonntag, den 10. April 2011 beleuchten werde.<br />
<a id="more"></a><a id="more-494"></a></p>
<h3 class="textimage">GUI-Prototypen</h3>
<p>In dieser Woche haben die Frontendentwickler die Ergebnisse ihrer GUI-Prototyp-Entwicklung vorgestellt. Beide Gruppen haben nach knapp zwei Wochen beachtliche Ergebnisse vorzuweisen — mit der Erkenntnis, dass C# und WPF so komfortabel grafisch aufwändige GUIs ermöglichen, dass wir in der finalen Version eine grafisch ansprechende Umsetzung anstreben, die sich nicht durch ein Standardbaukasten an Frames und starren Unterteilungen einschränken lassen wird. Angestrebt ist die Möglichkeit, alle Unterfenster der Anwendung — Panels genannt — frei bewegen, skalieren und ein- und ausblenden zu können.</p>
<dl>
<dt><a href="http://www.flickr.com/photos/tacker/5609709737/"><img src="http://farm5.static.flickr.com/4109/5609709737_aff7c802a3.jpg" alt="Explorer Prototyp: Fullscreen Modus" width="500" /></a></dt>
<dd>Explorer Prototyp: Fullscreen Modus</dd>
</dl>
<p>Zum Start der Entwicklung der GUI, nach der Fertigstellung des Designdokuments, wird das GUI-Team, beide Prototypen zusammenführen um die besten Elemente beider zu kombinieren.</p>
<h3 class="textimage">Domänenmodell und Pflichtenheft</h3>
<p>Nach zwei Wochen Einarbeitung in die neuen Werkzeuge — die auch das Backend-Team genutzt hat, um sich mit Fragen rund um die Schnittstellen zum Server zu beschäftigen, sind wir nun in der Einschätzung der Aufgabe sicher genug, um uns an die Finalisierung des Entwurfs zu machen.</p>
<p>Das Backend-Team entwickelt neben dem Domänenmodell auch bereits das Konzept für die Schnittstellen — das alles natürlich im Austausch mit dem Frontend-Team, dass sich um die schriftliche Niederlegung der bereits im Feature-Brainstorming erarbeiteten Anwendungsfälle kümmert.</p>
<p>Alle diese Arbeiten bilden die Grundlage für das Pflichtenheft, dass ebenfalls bereits in der Entstehung ist und nächste Woche abgegeben wird.</p>
<h3 class="textimage" id="workpackages">Work packages</h3>
<p><img class="alignright size-full wp-image-495" title="Grüne Ampel" src="http://studium.coderbyheart.de/wp-content/uploads/2011/04/ampel-gruen-150.png" alt="" width="55" height="150" />Ein alter bekannter aus dem letzten Semester ist auch wieder mit dabei: die Ampel. Sie kommt seit ein paar Tagen auf einer Seite im Wiki zum Einsatz, in der die Tickets in <a href="http://en.wikipedia.org/wiki/Work_package">work packages</a> gruppiert werden.</p>
<p>Diese Einteilung soll den Projektverlauf einfacher dokumentieren und bildet die Basis für meinen wöchentlichen Projektleiter-Bericht.</p>
<p>Für Entwickler sind work packages ein gutes Mittel, um schnell einen Überblick über aktuell anstehende Aufgaben zu bekommen und sie gruppieren die vielen Tickets eines Meilensteins in mehrere kleinere, übersichtlichere Einheiten.</p>
<p>Workpackages sind kein Feature von Trac sondern kombinieren nur geschickt verschieden Funktionen, die bereits zur Verfügung stehen. Aus meiner Dokumentation zu diesem Feature lässt sich die Funktion der Seite am besten erklären:</p>
<blockquote><p>WorkPackages unterteilen das Projekt in kleinere Aufgaben-Pakete, ähnlich den Meilensteinen, nur dass WorkPackages thematisch zusammengehörige Tickets gruppieren.</p>
<p>Diese Seite wir automatisch aus den Tickets vom Typ <em>workpackage</em> zusammen gestellt, und berücksichtigt dabei die Angaben <em>@start</em> und <em>@end</em> in der Ticket-Beschreibung, sowie den Owner und die Einträge im Feld CC, wobei die Usernamen dort mit der Liste der Entwickler abgeglichen wird.</p>
<p>Der Status des Tickets bestimmt die Einordnung in Aktive WorkPackages (accepted, assigned, reopened), ausstehende WorkPackages (new) und erledigte Workpackages (closed).</p>
<p>Die Ampel des WorkPackages wird durch den Tag <em>@status</em> bestimmt, der standardmäßig auf<em> grün</em> steht. Mögliche weitere Werte sind <em>rot</em> und <em>gelb</em>.</p>
<p>Der Owner eines Workpackages ist für dessen Umsetzung verantwortlich, die Personen im Feld CC sind ebenfalls mit der Umsetzung beauftragt.</p>
<p>Tickets ordnet man einem Workpackage zu, in dem man in den Keywords des Tickets das Keyword des Workpackages einträgt, z.B. <em>workpackage-115</em>.</p>
<p>Die Kommentare, die in einem WorkPackage-Ticket hinterlassen werden, sind das Protokoll über den Verlauf des WorkPackages.</p></blockquote>
<dl>
<dt><img class="alignnone size-full wp-image-496" title="WorkPackage" src="http://studium.coderbyheart.de/wp-content/uploads/2011/04/Bildschirmfoto1.png" alt="" width="500" height="325" /></dt>
<dd>Auszug aus der Wiki-Seite WorkPackages</dd>
</dl>
<h3 class="textimage">Probleme</h3>
<p>Inzwischen sind die Anlaufschwierigkeiten bei Pflegen der Entwickler-Blogs behoben und auch die Zeiterfassung hat sich eingespielt. Das Team arbeitet motiviert und vor allem engagiert.</p>
<h3 class="textimage">Die nächsten Schritte</h3>
<p>In dieser Woche steht das Pflichtenheft (Abgabe nächsten Montag) und das Designdokument im Mittelpunkt der Arbeiten.</p>
<h3 class="textimage">Das Projekt in Zahlen</h3>
<p>Zu guter Letzt noch einen Abzug der Zahlen aus mite für die vergangene Woche und den gesamten Projektverlauf (Endstand: Sonntag, 24 Uhr).</p>
<p>Projektbudget: 1.881h<br />
Davon verbraucht: 342h (18%)</p>
<p>Entwicklung: 185h (54%)<br />
Kommunikation: 157h (46%)</p>
<h4 class="textimage">Erfasste Zeit nach Person</h4>
<p><img src="https://spreadsheets.google.com/oimg?key=0AtTPpgm7INxMdGtxSEpoRFlLTTM4TmFucF84NGJEZmc&amp;oid=4&amp;zx=jnppmh8svmcc" alt="Erfasste Zeit nach Person - Woche 03" /></p>
