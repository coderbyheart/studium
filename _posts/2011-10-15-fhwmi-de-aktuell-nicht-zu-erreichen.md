---
layout: post
permalink: fhwmi-de-aktuell-nicht-zu-erreichen
title: fhwmi.de aktuell nicht zu erreichen
date: '2011-10-15 23:26:34 +0200'
tags:
- allgemein
---
<p>Seit gestern ist die Domain fhwmi.de über die öffentlichen DNS-Server nicht mehr auflösbar.</p>
<p>Über die Nameserver des Domain-Registrars joker ist sie korrekt konfiguriert.</p>
<p># host -t ANY fhwmi.de c.ns.joker.com<br />
fhwmi.de has address 213.133.103.107</p>
<p>Ich hab den Service bereits gestern kontaktiert, bisher ohne Erfolg.</p>
<p>Also Workaround kann man sich den DNS-Eintrag selber bauen:</p>
<p>Einfach diese Zeile<br />
<em>213.133.103.107 fhwmi.de</em><br />
in die Datei<br />
<em>C:\Windows\System32\drivers\etc\hosts</em> (Windows)<br />
bzw. <em>/etc/hosts</em> (Mac & Linux) eintragen.</p>
<h3 class="textimage">Update #1</h3>
<p>Den Grund für den Fehler habe ich gefunden: laut Denic Whois sind die zuständigen Nameserver noch die des alten Providers ...</p>
<p>Auf eine Antwort des Joker-Supports warte ich jetzt schon zwei Tage.</p>
<h3 class="textimage">Update #2</h3>
<p>Inzwischen ist der Nameserver-Eintrag laut Denic korrigiert, in spätestens 48 Stunden dürfte die Domain dann wieder vollständig erreichbar sein.</p>
