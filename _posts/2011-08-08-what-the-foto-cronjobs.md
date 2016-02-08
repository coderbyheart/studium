---
layout: post
permalink: what-the-foto-cronjobs
title: 'What the Foto: Cronjobs'
excerpt: "<a href=\"http://www.flickr.com/photos/tacker/sets/72157626379556132/\"><img
  class=\"alignright\" src=\"http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg\"
  alt=\"What The Foto?\" /></a>Für einige Aufgaben habe ich Cronjobs eingesetzt, da
  sich diese anders nicht sinnvoll realisieren ließen.\r\n\r\nLeider ist auf unserem
  hochschul-internen Server (linux001) kein Python 3 installiert, so dass ich die
  Cronjobs von meinem eigenen Webserver aus ausgeführt habe.\r\n\r\nDa aber die Trac-Installationen
  auch ohne VPN erreichbar sind, konnte ich so einfach von außen auf die XML-RPC-API
  von Trac zu greifen.\r\n"
date: '2011-08-08 06:00:02 +0200'
tags:
- SoftwareTechnik
- WhatTheFoto
---
<p><a href="http://www.flickr.com/photos/tacker/sets/72157626379556132/"><img class="alignright" src="http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg" alt="What The Foto?" /></a>Für einige Aufgaben habe ich Cronjobs eingesetzt, da sich diese anders nicht sinnvoll realisieren ließen.</p>
<p>Leider ist auf unserem hochschul-internen Server (linux001) kein Python 3 installiert, so dass ich die Cronjobs von meinem eigenen Webserver aus ausgeführt habe.</p>
<p>Da aber die Trac-Installationen auch ohne VPN erreichbar sind, konnte ich so einfach von außen auf die XML-RPC-API von Trac zu greifen.<br />
<a id="more"></a><a id="more-697"></a></p>
<h3 class="textimage">Öffentlicher RSS-Feed</h3>
<p>Der RSS-Feed unserer Trac-Installationen ist nur mit dem Login und Passwort des Hochschul-Accounts erreichbar. Für <a href="http://google.de/reader/">Google Reader</a> und anderer browserbasierte Feedreader ist es unmöglich, mit Passwort geschützte Feeds ab zu holen — man will ja auch nicht unbedingt die Zugangsdaten zum eigenen Hochschul-Account in der Wildnis verteilen.</p>
<p>Also habe ich einen Cronjob definiert, der den RSS-Feed aus Trac zieht und in einem über HTTP frei zugänglichen Ort ablegt:</p>
<p>[cc lang="bash"]wget -q --no-check-certificate --user {username} --password {password} {rss-url} -O {local file}[/cc]</p>
<h3 class="textimage">Wiki-Seiten automatisch generieren</h3>
<p>Wie bereits geschrieben, habe ich einige Script geschrieben, die spezielle Wiki-Seiten für unser Projekt erzeugen, z.B. die Seite mit den <a href="/what-the-foto-workpackages">Workpackages</a>, dem <a href="/what-the-foto-tickettree">TicketTree</a> oder die <a href="/what-the-foto-api-dokumentation">API-Dokumentation</a>. Hierfür hatte ich Cronjobs, die die jeweiligen Python3-Scripte regelmäßig aufgerufen haben.</p>
<h3 class="textimage">Frontend-Release in der Dropbox</h3>
<p>Zum einfacheren Testen unseres Clients habe ich ein Script geschrieben, dass sich aus dem SVN alle 30 Minuten die Frontend.exe und alle nötigen Bibliotheken holt und diese in einen Ordnern kopiert, der mit einem ebenfalls auf dem Server laufenden <a href="http://db.tt/NYepoPI">Dropbox-Client</a> verknüpft ist.</p>
<p>So konnte man auf allen Rechnern, mit denen man das Frontend testen wollte einfach nur diesem Dropbox-Ordner beitreten und musst nicht extra TortoiseSVN oder gar Visual Studio starten.</p>
<p>[cc lang="bash"]#!/bin/bash</p>
<p>svn export -q https://scm.mi.hs-rm.de/svn/2011swtpro/2011swtpro01/Client/trunk/Frontend/Frontend/bin/Release /tmp/release<br />
rsync -a --delete /tmp/release /data/dropbox/Dropbox/Studium/Semester\ 4/Softwaretechnik/Client<br />
chown -R dropbox: /data/dropbox/Dropbox/Studium/Semester\ 4/Softwaretechnik/Client<br />
rm -rf /tmp/release[/cc]</p>
