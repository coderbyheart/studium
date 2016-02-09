---
layout: post
permalink: what-the-foto-was-wurde-umgesetzt
title: 'What The Foto: Was wurde umgesetzt?'
excerpt: "<a href=\"http://www.flickr.com/photos/tacker/sets/72157626379556132/\"><img
  class=\"alignright\" src=\"http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg\"
  alt=\"What The Foto?\" /></a>Wie schon erwähnt, fanden es die meisten Team-Mitglieder
  schaden, dass wir auf einige <em>coolen</em> Features verzichten mussten, weil wir
  die Komplexität einiger Funktionen unterschätzt hatten. Allerdings muss man zum
  einen einmal betrachten, welche Features wir vom ursprünglichen Plan trotzdem umsetzen
  konnten — schließlich konnten wir zu Beginn des Projektes den Aufwand für die einzelnen
  Funktionen gar nicht abschätzen, denn für das Gesamte Team war es das erste große
  Projekt im Studium, mit einigen bis dahin unbekannten Technologien: WPF mit C#,
  Messaging mit ActiveMQ und ein Java-Server (bisher haben wir immer GUIs gebaut).\r\n"
date: '2011-07-18 10:57:05 +0200'
tags:
- SoftwareTechnik
- WhatTheFoto
---
<p><a href="http://www.flickr.com/photos/tacker/sets/72157626379556132/"><img class="alignright" src="http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg" alt="What The Foto?" /></a>Wie schon erwähnt, fanden es die meisten Team-Mitglieder schaden, dass wir auf einige <em>coolen</em> Features verzichten mussten, weil wir die Komplexität einiger Funktionen unterschätzt hatten. Allerdings muss man zum einen einmal betrachten, welche Features wir vom ursprünglichen Plan trotzdem umsetzen konnten — schließlich konnten wir zu Beginn des Projektes den Aufwand für die einzelnen Funktionen gar nicht abschätzen, denn für das Gesamte Team war es das erste große Projekt im Studium, mit einigen bis dahin unbekannten Technologien: WPF mit C#, Messaging mit ActiveMQ und ein Java-Server (bisher haben wir immer GUIs gebaut).<br />
<a id="more"></a><a id="more-647"></a></p>
<h3 class="textimage">Wie sind wir zu unseren Features gekommen?</h3>
<dl>
<dt><a href="http://www.flickr.com/photos/tacker/5569095320/in/set-72157626379556132"><img src="http://farm6.static.flickr.com/5053/5569095320_a5e2545d8a_b.jpg" alt="Brainstorming Flipchart" width="500" /></a></dt>
<dd>Brainstorming Flipchart</dd>
</dl>
<p>In einem Brainstorming in der zweiten Woche haben wir uns Gedanken über die Funktionen gemacht, die wir mit Hilfe eines Flipcharts und Karteikarten gesammelt haben. Anschließend haben wir darüber abgestimmt, was wir implementieren wollen.</p>
<h3 class="textimage">Was wurde dann umgesetzt?</h3>
<p>Herausgekommen ist eine Liste von Features, von denen wir bis zum Entwicklungsende auch die meisten implementieren konnten (grün). Die nicht implementierten (rot) sind meiner Meinung nach keinesfalls kritisch, und dass wir auf diese Verzichten konnten, zeigt auch, dass wir uns gut strukturiert zuerst um die wichtigen Dinge gekümmert haben — lediglich für das Auslesen der EXIF-Daten gab es zum Zeitpunkt des Entwicklungsendes funktionsfähigen Code, der wieder entfernt wurde.</p>
<p>Schade fanden die meisten den Verzicht auf die Druckfunktion und die Effekte, wobei man hier relativierend sagen kann, dass der technische Aufwand dafür eher begrenzt gewesen wäre. So viel dann die Entscheidung nach der zweiten Demo zu Gunsten der Stablisierung der bis dahin implementierten Funktionen.</p>
<p>Rein nominell haben wir 64% der geplanten Funktionen implementiert, vom Umfang her dürften diese aber bei schätzungsweise 90% liegen, was man auch gut <a href="{{ '/what-the-foto-demo-videos' | prepend: site.baseurl | prepend: site.url }}">in den Demo-Videos begutachten kann</a>.</p>
<p>Grau markiert sind die Features, die bereits im Brainstorming durchgefallen sind.</p>
<table class="normal features">
<tbody>
<tr>
<td class="impl">1</td>
<td class="impl">Fotos bewerten</td>
</tr>
<tr>
<td class="impl">2</td>
<td class="impl">Lightbox ist nach dem Kauf unveränderbar</td>
</tr>
<tr>
<td class="impl">3</td>
<td class="impl">Titel (Beschreibung) eines Fotos setzen</td>
</tr>
<tr>
<td class="impl">4</td>
<td class="impl">Benutzer-Profil</td>
</tr>
<tr>
<td class="impl">5</td>
<td class="impl">Taggen von Fotos</td>
</tr>
<tr>
<td class="impl">6</td>
<td class="impl">Freigabe der Lightbox</td>
</tr>
<tr>
<td class="impl">7</td>
<td class="impl">Freigabe-Adressbuch</td>
</tr>
<tr>
<td class="impl">8</td>
<td class="impl">ZIP-Download der gekauften Fotos einer Lightbox</td>
</tr>
<tr>
<td class="impl">9</td>
<td class="impl">Der Fotograf kann Preise für seine Fotos festlegen</td>
</tr>
<tr>
<td class="impl">10</td>
<td class="impl">Chat in der Lightbox</td>
</tr>
<tr>
<td class="impl">11</td>
<td class="impl">Lightbox verwalten</td>
</tr>
<tr>
<td class="impl">12</td>
<td class="impl">Fotograf registriert sich selbst</td>
</tr>
<tr>
<td class="impl">13</td>
<td class="impl">Suche</td>
</tr>
<tr>
<td class="impl">14</td>
<td class="impl">Server liefert on demand verschiede Größen eine Fotos</td>
</tr>
<tr>
<td class="impl">15</td>
<td class="impl">Kategorien</td>
</tr>
<tr>
<td class="impl">16</td>
<td class="impl">Mitarbeiter verwalten</td>
</tr>
<tr>
<td class="impl">17</td>
<td class="impl">Kunden verwalten</td>
</tr>
<tr>
<td class="impl">18</td>
<td class="impl">Der Kunde darf alle Fotos der Fotodatenbank sehen</td>
</tr>
<tr>
<td class="impl">19</td>
<td class="impl">Liste mit gekauften Fotos</td>
</tr>
<tr>
<td class="impl">20</td>
<td class="impl">Gekaufte Fotos lassen sich herunterladen</td>
</tr>
<tr>
<td class="impl">21</td>
<td class="impl">Fotos löschen</td>
</tr>
<tr>
<td class="impl">22</td>
<td class="impl">Agentur legt global oder pro Foto Gebühren fest</td>
</tr>
<tr>
<td class="notimpl">23</td>
<td class="notimpl">i18n</td>
</tr>
<tr>
<td class="notimpl">24</td>
<td class="notimpl">Lightbox-spezifische Einstellungen für Fotoeffekte</td>
</tr>
<tr>
<td class="notimpl">25</td>
<td class="notimpl">Pro-Uploader<br />
<small><em>Unser normaler Uploader ist eigentlich schon sehr "Pro".</em></small></td>
</tr>
<tr>
<td class="notimpl">26</td>
<td class="notimpl">Statistik-Modul</td>
</tr>
<tr>
<td class="notimpl">27</td>
<td class="notimpl">Server stellt Foto-Effekte zur Verfügung</td>
</tr>
<tr>
<td class="notimpl">28</td>
<td class="notimpl">Wasserzeichen</td>
</tr>
<tr>
<td class="notimpl">29</td>
<td class="notimpl">Auslesen von EXIF-Daten</td>
</tr>
<tr>
<td class="notimpl">30</td>
<td class="notimpl">Druckfunktion Lightbox</td>
</tr>
<tr>
<td class="notimpl">31</td>
<td class="notimpl">Kunde kann sich aussuchen, ob die Lightbox nach dem Kauf gesperrt wird</td>
</tr>
<tr>
<td class="notimpl">32</td>
<td class="notimpl">Rechnung</td>
</tr>
<tr>
<td class="notimpl">33</td>
<td class="notimpl">Kopie einer Lightbox anlegen</td>
</tr>
<tr>
<td class="notimpl">34</td>
<td class="notimpl">Benachrichtigungen via E-Mail<br />
<small><em>Ist sogar zu etwa 50% implementiert.</em></small></td>
</tr>
<tr>
<td class="discarded">35</td>
<td class="discarded">Agentur kann Fotos eines Fotografen exklusiv kaufen</td>
</tr>
<tr>
<td class="discarded">36</td>
<td class="discarded">Liste mit Fotos, die einem Kunden präsentiert wurden</td>
</tr>
<tr>
<td class="discarded">37</td>
<td class="discarded">Fotos sperren</td>
</tr>
<tr>
<td class="discarded">38</td>
<td class="discarded">Neu registriert Fotografen müssen frei geschaltet werden</td>
</tr>
</tbody>
</table>
