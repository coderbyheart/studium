---
layout: post
status: publish
published: true
title: Leuchttisch Entwicklertagebuch 01
author:
  display_name: Markus Tacker
  login: m
  email: m@tacker.org
  url: http://tckr.cc/
author_login: m
author_email: m@tacker.org
author_url: http://tckr.cc/
excerpt: "<img class=\"alignright size-full wp-image-459\" title=\"Leuchttisch Logo\"
  src=\"/uploads/2011/03/Leuchttisch-250.png\"
  alt=\"\" width=\"250\" height=\"260\" />Willkommen zur ersten Ausgabe des <em>Leuchttisch</em>-Entwicklertagebuchs!\r\n"
wordpress_id: 457
wordpress_url: /?p=457
date: '2011-03-28 22:13:03 +0200'
date_gmt: '2011-03-28 20:13:03 +0200'
categories:
- Uncategorized
tags:
- SoftwareTechnik
- WhatTheFoto
comments: []
---
<p><img class="alignright size-full wp-image-459" title="Leuchttisch Logo" src="/uploads/2011/03/Leuchttisch-250.png" alt="" width="250" height="260" />Willkommen zur ersten Ausgabe des <em>Leuchttisch</em>-Entwicklertagebuchs!<br />
<a id="more"></a><a id="more-457"></a></p>
<h3 class="textimage">Das Projekt</h3>
<p><em>Leuchttisch</em> — so haben wir unser Projekt getauft — ist ein kollaborative Software zum Erstellen von Fotosammlungen und wird als Teil der Veranstaltung Softwaretechnik im 4. Semester des Studienganges <a href="http://www.hs-rm.de/medieninformatik">Medieninformatik</a> an der <a href="http://hs-rm.de/">Hochschule RheinMain</a> durch die Studenten entwickelt.</p>
<p>Die Rahmenbedingungen sind dabei vorgegeben: In 14 Wochen entsteht in Teams zu je etwa 10-12 Personen ein Standalone-Client auf Basis von <a href="http://de.wikipedia.org/wiki/Windows_Presentation_Foundation">WPF</a> (C#), sowie auf Server, der in Java geschrieben wird. Client und Server dürfen nur über Schnittstelle miteinander kommunizieren und haben ansonsten keine gemeinsame Datenbasis.</p>
<p>Der Funktionsumfang ist ebenfalls abgesteckt: Zu erstellen ist ein interaktives System für eine verteilte Foto-Agentur mit <strong>Echtzeit-Interaktions-/Kollaborationsmöglichkeiten</strong>, mit dem Agentur-Mitarbeiter den Bildbestand sichten, taggen, durchsuchen, kategorisieren, beschreiben können und in Echtzeit Bildermappe mit Vorschlägen  für einen Kunden vorbereiten und diskutieren können.</p>
<p>Natürlich soll sich auch der Kunde in die Diskussion mit einschalten können, und Fotografen laden ihre Fotos hoch.</p>
<h3 class="textimage">Die Wochenberichte</h3>
<p>Neben dem rein technischen Aspekt liegt auch ein großer Augenmerk auf der systematischen und organisierten Arbeit — meine Aufgabe als Projektleiter ist weniger das Programmieren sondern vielmehr das Organisieren und Planen. Ein Teil dieser Aufgabe sind auch wöchentliche Reportings an den Veranstaltungsleiter, deren Basis diese Wochenberichte bilden.</p>
<h3 class="textimage">Die erste Woche: Projektstart</h3>
<p>Nachdem am Donnerstag, den 17. März das Thema des Projekts vorgestellt wurde, hatten sich auch recht zügig unser Projekt-Team gefunden. Als erste Maßnahme musste die Projekt-Infrastruktur aufgesetzt werden, die Werkzeuge, die wir bis jetzt verwenden sind im Einzelnen:</p>
<h4 class="textimage">Twitter</h4>
<p>Im Team leider etwas unterrepräsentiert, für mich aber sehr hilfreich: ein eigener Twitter-Account für das Projekt: <a href="http://twitter.com/swt2011">@swt2011</a></p>
<p>Dort fließen dann mit Hilfe von <a href="http://twitter.com/twitterfeed">@twitterfeed</a> die RSS-Feeds der Trac-Timeline hinein. So hat man immer schnelle, kompakte Infos darüber, was im Projekt geschieht.</p>
<h4 class="textimage">Facebook</h4>
<p>Im Gegensatz zu Twitter hat jeder im Team einen Account bei diesem Sozialen Netzwerk, hier ist also eine eigene, geschlossene Gruppe das Mittel der Wahl für schnelle Abstimmungen.</p>
<h4 class="textimage">Google Docs</h4>
<p>Die Office Suite von Google hat einen entscheidenden Vorteil: Alle Dokumente lassen sich gleichzeitig mit vielen bearbeiten — besonders in Meetings ist das extrem wertvoll, da so gemeinsam ein Protokoll entsteht, und jeder Ergänzungen und Korrekturen vornehmen kann.</p>
<p>Hierfür benötigt man ebenfalls ein eigenes Google-Konto, dieser "Aufwand" ist aber angesichts des Mehrwerts absolut sinnvoll.</p>
<p>Auch beim Erarbeiten von umfangreichen Dokumenten ist das Arbeiten in  der Cloud unschlagbar — niemand überschreibt jetzt einen Stand und alle  arbeiten stets mit der neuesten Version.</p>
<p>Als Workflow hat sich etabliert, Dokumente in Google Docs an zu legen,  bis diese einen finalen Stand erreicht hat. Dieser wird dann zur Archivierung ins Trac Wiki übertragen.</p>
<h4 class="textimage">Google Calendar</h4>
<p>Alle Termine des Projekts werden in eine zentralen Google Calendar verwaltet. Dieser biete iCal-Exporte, so dass er auch in externen Kalender-Anwendungen importiert werden kann.</p>
<h4 class="textimage">mite</h4>
<p>Zeiterfassung ist ein wichtiger Bestandteil der Projektplanung und -kontrolle, daher setzen wir zur sekundengenauen Zeiterfassung auf <a href="http://mite.yo.lk/">mite</a>.</p>
<h4 class="textimage">Dropbox</h4>
<p>Für die Fälle, in denen man Dateien <em>mal eben schnell</em> austauschen möchte, ist die <a href="http://db.tt/NYepoPI">Dropbox</a> die erste Wahl — denn nicht alle Dateien müssen zwangsläufig mit einer SVN-Revision verewigt werden.</p>
<h4 class="textimage">Doodle</h4>
<p>Als unerlässliches Hilfsmittel bei der Entscheidungs- und Terminfindung hat sich <a href="http://www.doodle.com/">Doodle</a> bewährt — das intuitive Interface geht bei Abstimmungen einfach viel besser von der Hand, als in Trac Kommentare zu zählen. Die Funktionen zur Terminfindung sind gerade mit der Integration von Google Calendar grandios.</p>
<h4 class="textimage">Trac</h4>
<p>Neben Subversion war <a href="http://trac.edgewall.org/">Trac</a> als Mittel zur Organisation und Dokumentation der Entwicklung vorgegebenen — und wäre auch meine erste Wahl gewesen.</p>
<p>Hier habe ich das Wiki soweit wie möglich mit allen zum jetzigen Zeitpunkt bekannten Informationen befüllt, und Vorlagen für das Entwickler-Blog angelegt, die von jedem Projektmitarbeiter wöchentlich zu führen sind.</p>
<h4 class="textimage">Subversion (+Git)</h4>
<p>Mit <a href="http://subversion.apache.org/">Subversion</a> als Versionsverwaltungssystem verbinden die meisten im Studiengang inzwischen eine Hassliebe — als Unterstützung nehmen wir je nach Geschmack noch <a href="http://www.kernel.org/pub/software/scm/git/docs/git-svn.html">GIT-SVN</a> dazu.</p>
<h3 class="textimage">Das erste Meeting</h3>
<p>Im ersten Meeting ging es dann erst mal um banale Dinge. Im Vordergrund stand nebem dem Projektnamen — über den dann später in Doodle abgestimmt wurde — ging es mir vor allem um die Vorstellung der eben aufgezählten Werkzeuge und ihren jeweiligen Platz im Projektverlauf.</p>
<p>Ein wichtiger Punkt war die grundsätzliche Ausrichtung des Desktop-Clients: Wollen wir lieber den klassischen Fenster-Aufbau mit Menüleiste &amp; Co oder bevorzugen wir einen eher haptischen Ansatz?</p>
<p>Da wir auch noch nicht besonders mit den Fähigkeiten von WPF vertraut sind, haben wir beschlossen, zwei Teams zu bilden, die jeweils einen sehr einfachen Prototyp entwickeln um ein Gefühl für die neue Umgebung zu bekommen, einmal in einer klassischen "Explorer"-Version und einmal in der "Advanced"-Variante.</p>
<h3 class="textimage">Das zweite Meeting</h3>
<p>Ein wichtiger Punkt dieses Meetings war neben der Festlegung der Teams für die Prototypen auch eine erste Planung der Termine für die vorgegebenen Meilensteine des Projekts zu erarbeiten.</p>
<h4 class="textimage">Zwei feste Meeting-Termine pro Woche</h4>
<p>Wir haben uns in der vergangenen Woche auf zwei fester Termine pro Woche geeinigt: Dienstags und Donnerstags. Diese etwa einstündigen Termine sind für alle Projektteilnehmer verpflichten und dienen dazu, regelmäßig den aktuellen Stand aus zu tauschen.</p>
<h4 class="textimage">Projektfahrplan</h4>
<p>Nach dem zweiten Meeting haben wir schon einen ungefähren Ablaufplan für das Projekt:</p>
<p>Projektdauer ab heute: ca. 14 Wochen</p>
<ul>
<li>Abgabe der Anforderungsspezifikation nach etwa 4 Wochen</li>
<li>Abgabe der System-Architektur nach etwa 5 Wochen</li>
<li>1. Zwischendemo (Demonstriert elementare "round trips") nach etwa 6 Wochen</li>
<li>2. Zwischendemo (Kernanforderungen sind umgesetz) nach etwa 10 Wochen</li>
<li>Release nach etwa 14 Wochen</li>
</ul>
<p>Entsprechend den Aufwänden in Credit Points für das Fach Softwaretechnik errechnet sich ein geplanter Aufwand für die Umsetzung des Projekts wie folgt:</p>
<table class="normal">
<tbody>
<tr>
<td>7 Creditpoints</td>
<td>·  30h</td>
<td>= 210</td>
</tr>
<tr>
<td>- 1,5h Vorlesung</td>
<td>·  13 Wochen</td>
<td>= -19,5h</td>
</tr>
<tr>
<td>- 3h Praktikum</td>
<td>·  4 Wochen</td>
<td>= -12h</td>
</tr>
<tr>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>= 178,5h</td>
</tr>
</tbody>
</table>
<p>Bei 11 Mitarbeitern stehen also für das Projekt theoretisch 1963h = 245 Manntage zur Verfügung, wobei sich eine wöchentliche Belastung von ca. 13 Stunden pro Person (zzgl. Vorlesung und Praktikum ergibt).</p>
<h3 class="textimage">Das dritte Meeting: Feature-Brainstorming</h3>
<p>In diesem gut zweistündigen Meeting haben wir uns intensiv mit dem Funktionsumfang der Anwendung beschäftigt und eine gut 40 Punkte umfassende Liste mit groben Feature-Beschreibungen erarbeitet und diese den verschiedenen Benutzerrollen zugeschrieben. In teils ausgiebiger Diskussion wurde Sinn und Unsinn von allen Vorschlägen abgewogen und letztendlich per Abstimmung festgelegt, welche Features dem Rotstift zum Opfer fallen.</p>
<p><a href="http://www.flickr.com/photos/tacker/5569095320/">Hier</a> ist das Ergebnis des Brainstormings in voller Pracht.</p>
<h3 class="textimage">Logo</h3>
<p>Mittlerweile hat das Projekt auch ein Logo bekommen, damit es nicht so ganz nackt da steht.</p>
<h3 class="textimage">Das Projekt in Zahlen</h3>
<p>Zu guter Letzt noch einen Abzug der Zahlen aus mite für die vergangene Woche und den gesamten Projektverlauf (Endstand: Sonntag, 24 Uhr).</p>
<p>Projektbudget: 1.881h<br />
Davon verbraucht: 78,5h (4%)</p>
<p>Entwicklung: 42h (53%)<br />
Kommunikation: 37h (47%)</p>
<h4 class="textimage">Erfasste Zeit nach Person</h4>
<p><img src="https://spreadsheets.google.com/oimg?key=0AtTPpgm7INxMdGtxSEpoRFlLTTM4TmFucF84NGJEZmc&oid=1&zx=5sf0tpl6fi1x" alt="Erfasste Zeit nach Person - Woche 01" /></p>
