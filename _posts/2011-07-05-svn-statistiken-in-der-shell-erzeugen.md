---
layout: post
permalink: svn-statistiken-in-der-shell-erzeugen
title: SVN Statistiken in der Shell erzeugen
excerpt: "<a href=\"http://www.flickr.com/photos/tacker/sets/72157626379556132/\"><img
  class=\"alignright\" src=\"http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg\"
  alt=\"What The Foto?\" /></a>Mit ein paar geschickt kombinierten Unix-Tools lassen
  sich aus einem SVN Commit-Log interessante Statistiken extrahieren.\r\n"
date: '2011-07-05 10:15:50 +0200'
tags:
- subversion
- SoftwareTechnik
- WhatTheFoto
---
<p><a href="http://www.flickr.com/photos/tacker/sets/72157626379556132/"><img class="alignright" src="http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg" alt="What The Foto?" /></a>Mit ein paar geschickt kombinierten Unix-Tools lassen sich aus einem SVN Commit-Log interessante Statistiken extrahieren.<br />
<a id="more"></a><a id="more-608"></a><br />
Für unser Softwaretechnik-Projekt habe ich einige Statistiken ausgearbeitet:</p>
<h3 class="textimage">Anzahl der Commits pro User</h3>
<p>Aus dem SVN-Log, das so aussieht:</p>
<p>[cc lang="text"]------------------------------------------------------------------------<br />
r1 | mtack001 | 2011-03-18 13:16:42 +0100 (Fr, 18. Mär 2011) | 1 Zeile</p>
<p>Lege Verzeichnisstruktur an.<br />
------------------------------------------------------------------------[/cc]</p>
<p>Holen wir uns mit <code>grep -E "^r[0-9]+ \| "</code> nur diese Zeilen<br />
[cc lang="text"]r1 | mtack001 | 2011-03-18 13:16:42 +0100 (Fr, 18. Mär 2011) | 1 Zeile[/cc]</p>
<p>Mit <code>awk '{ print $3; }'</code> wird daraus der Username <code>mtack001</code> extrahiert.</p>
<p>Alle Zeile werden dann mit <code>sort</code> sortiert und <code>uniq -c</code> zählt dann, wie oft ein Username vorkommt.</p>
<p>Zum Schluss sorgt ein <code>sort -n -r</code> dafür, dass diese Liste noch einmal absteigend sortiert wird.</p>
<p>Das gesamte Kommando:</p>
<p>[cc lang="bash"]svn log http://example.com/svn/repository/ | grep -E "^r[0-9]+ \| " | awk '{ print $3; }' | sort | uniq -c | sort -n -r[/cc]</p>
<p>Diese Kommando liefert eine Liste in der Form "commits username", die man dann im Tabellenkalkulationsprogramm seiner Wahl in ein Chart umwandeln kann.</p>
<p>In unserem Fall ergibt sich folgender Graph (die Usernamen habe ich entfernt):</p>
<p><img class="alignnone size-full wp-image-612" title="Anzahl der Commits" src="/uploads/2011/07/wtf-anzahl-der-commits.png" alt="" width="493" height="364" /></p>
<h3 class="textimage">Anzahl der Commits eines Users pro Tag</h3>
<p>Ähnliches kann man verwenden, um die Anzahl der Commits eines User pro Tag über den Projektverlauf zu visualisieren.</p>
<p>Ähnlich wie bei der vorigen Abfrage, werden hier mit <code>awk '{ print $5, $3; }'</code> nicht nur der Username, sondern auch das Datum des Commits extrahiert.</p>
<p>Ein anschließendes <code>uniq -c</code> zählt dann die Commits pro Tag.</p>
<p>Diese Liste filtern wir dann mit <code>grep username</code> nach den Einträgen des Users, der uns interessiert.</p>
<p><code>awk '{ OFS = ","; print $2, $1; }'</code> sorgt dann dafür, dass das Ergebnis kommasepariert ausgegeben wird, so dass man es in einem Tabellenkalkulationsprogramm verwenden kann.</p>
<p>Meine Commits auf dem Projekt sehen so aus:</p>
<p><img src="/uploads/2011/07/wtf-commits-pro-tag-markus-500x240.png" alt="" title="Meine Commits pro Tag " width="500" height="240" class="alignnone size-medium wp-image-622" /></p>
<p>Das gesamte Kommando:</p>
<p>[cc lang="bash"]svn log http://example.com/svn/repository/ | grep -E "^r[0-9]+ \| " | awk '{ print $5, $3; }' | sort | uniq -c | grep username | awk '{ OFS = ","; print $2, $1; }' > username-commits-per-day.csv[/cc]</p>
<h3 class="textimage">Commits pro Tag</h3>
<p>Leicht abgewandelt, kann man so auch für das gesamte Projekt die Commits pro Tag erhalten:</p>
<p><img src="/uploads/2011/07/wtf-commits-pro-tag-500x239.png" alt="" title="Commits pro Tag" width="500" height="239" class="alignnone size-medium wp-image-618" /></p>
<p>[cc lang="bash"]svn log http://example.com/svn/repository/ | grep -E "^r[0-9]+ \| " | awk '{ print $5; }' | sort | uniq -c | awk '{ OFS = ","; print $2, $1; }' > commits-per-day.csv[/cc]</p>
<h3 class="textimage">Commits pro Stunde</h3>
<p>Die Stunde ist natürlich auch interessant: bei WTF? haben wir quasi rund um die Uhr gearbeitet.</p>
<p><img src="/uploads/2011/07/wtf-commits-nach-uhrzeit-500x296.png" alt="" title="Commits nach Uhrzeit" width="500" height="296" class="alignnone size-medium wp-image-619" /></p>
<p>[cc lang="bash"]svn log http://example.com/svn/repository/ | grep -E "^r[0-9]+ \| " | awk '{ print substr($6, 0, 2); }' | sort | uniq -c | awk '{ OFS = ","; print $2, $1; }' > commits-per-hour.csv[/cc]</p>
<h3 class="textimage">Commits pro Wochentag</h3>
<p>Besonders beliebt war dabei der Donnerstag (der offizielle Projekt-Tag im Semester) und der Sonntag, der natürlich bis in den Montag Auswirkungen hat.</p>
<p><img src="/uploads/2011/07/wtf-commits-pro-wochentag-500x303.png" alt="" title="Commits nach Wochentag" width="500" height="303" class="alignnone size-medium wp-image-620" /></p>
<p>[cc lang="bash"]svn log http://example.com/svn/repository/ | grep -E "^r[0-9]+ \| " | awk '{ print substr($8, 2, 2); }' | sort | uniq -c | awk '{ OFS = ","; print $2, $1; }' > commits-per-weekday.csv[/cc]</p>
