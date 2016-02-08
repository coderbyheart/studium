---
layout: post
permalink: what-the-foto-workpackages
title: 'What The Foto: WorkPackages'
excerpt: "<a href=\"http://www.flickr.com/photos/tacker/sets/72157626379556132/\"><img
  class=\"alignright\" src=\"http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg\"
  alt=\"What The Foto?\" /></a>Über die Einführung der WorkPackages hatte ich ja schon
  an anderer Stelle gesprochen.\r\n\r\nHier möchte ich noch kurz <a href=\"/svn/WTF/workpackages/WorkPackages.py\">das
  Python3-Script</a> vorstellen, dass ich verwendet habe, um die Wiki-Seite mit den
  WorkPackages zu erstellen.\r\n"
date: '2011-08-01 06:00:52 +0200'
tags:
- SoftwareTechnik
- WhatTheFoto
- python
---
<p><a href="http://www.flickr.com/photos/tacker/sets/72157626379556132/"><img class="alignright" src="http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg" alt="What The Foto?" /></a>Über die Einführung der WorkPackages hatte ich ja schon an anderer Stelle gesprochen.</p>
<p>Hier möchte ich noch kurz <a href="/svn/WTF/workpackages/WorkPackages.py">das Python3-Script</a> vorstellen, dass ich verwendet habe, um die Wiki-Seite mit den WorkPackages zu erstellen.<br />
<a id="more"></a><a id="more-707"></a><br />
Prinzipiell habe ich dazu einen eigenen Ticket-Typ <em>workpackage</em> erstellt. In diesen Tickets wurde dann speziell formatierte Angaben ausgelesen.<br />
Aus diesen ganzen Angaben werden dann übersichtlich die Infos zu allen WorkPackages erzeugt:</p>
<p><a href="http://www.flickr.com/photos/tacker/5984338818/sizes/o/in/photostream/"><img src="http://farm7.static.flickr.com/6142/5984338818_efebda104c_o.png" width="500" alt="Darstellung eines WorkPackage als Wiki-Seite" /></a></p>
<h3 class="textimage">Standard-Felder mit besonderer Bedeutung</h3>
<dl>
<dt>Status</dt>
<dd>Der status des Tickets bestimmt die Einordnung in aktive WorkPackages (accepted, assigned,<br />
reopened), ausstehende WorkPackages (new) und erledigte Workpackages (closed).</dd>
<dt>Owner, CC</dt>
<dd>Der Verantwortliche für ein WorkPackage ist der owner des Tickets, die Mitarbeiter werden aus dem<br />
Feld CC ausgelesen, wobei die Usernamen dort mit der Liste der Entwickler<br />
abgeglichen wird.</p>
<p>Der Owner eines Workpackages ist für dessen Umsetzung verantwortlich, die Personen im Feld CC<br />
sind ebenfalls mit der Umsetzung beauftragt.</dd>
<dt>Kommentare</dt>
<dd>Die Kommentare, die in einem WorkPackage-Ticket hinterlassen werden, sind das Protokoll über<br />
den Verlauf des WorkPackages.</dd>
</dl>
<h3 class="textimage">@-tags in der Beschreibung</h3>
<p>@-tags werden in der Beschreibung des Tickets eingetragen.</p>
<dl>
<dt>@start und @end</dt>
<dd>Diese beiden Tags beschreiben den Beginn und das Ende eines WorkPackages. Sie müssen im Format <em>YYYY-MM-DD</em> sein und werden verwendet um die WorkPackages nach Beginn<br />
zu sortieren.</dd>
<dt>@status</dt>
<dd>Die Ampel des WorkPackages wird durch den Tag @status bestimmt, der standardmäßig auf grün steht. Mögliche weitere Werte sind rot und gelb. Die einzelnen Stati<br />
bedeuten dabei:<br />
<em>grün</em>: Alles in Ordnung, Zeitplan wird eingehalten, keine Probleme, Fragen, offene Abhängigkeiten, etc<br />
<em>gelb</em>: es gibt kleinere Probleme<br />
<em>rot</em>: Akutes dringendes Problem, das (sofort) gelöst werden muss</dd>
<dt>@task</dt>
<dd>Mit @task beschreibt man, welche Person welche Aufgabe für dieses WorkPackage hatte. Die Beschreibung sollte dabei stichpunktartig sein. Das Format ist<br />
<em>@task [person] [Beschreibung der Aufgabe]</em><br />
wobei <em>[person]</em> das Kürzel aus der Liste der Entwickler ist und <em>[Beschreibung der Aufgabe]</em> der beschreibende Text.</dd>
</dl>
<h3 class="textimage">Zuordnung von Tickets zu WorkPackages</h3>
<p>Tickets ordnet man einem Workpackage zu, in dem man in den Keywords des Tickets das Keyword des Workpackages einträgt, z.B. <em>workpackage-115</em>.</p>
