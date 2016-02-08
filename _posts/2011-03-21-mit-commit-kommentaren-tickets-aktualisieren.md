---
layout: post
status: publish
published: true
title: Mit commit-Kommentaren Tickets aktualisieren
author:
  display_name: Markus Tacker
  login: m
  email: m@tacker.org
  url: http://tckr.cc/
author_login: m
author_email: m@tacker.org
author_url: http://tckr.cc/
wordpress_id: 447
wordpress_url: /?p=447
date: '2011-03-21 20:22:56 +0100'
date_gmt: '2011-03-21 18:22:56 +0100'
categories:
- Uncategorized
tags:
- svn
- trac
comments: []
---
<p>Seit heute ist in allen Trac-Installationen auf <em>scm.mi.hs-rm.de</em> das <a href="http://trac.edgewall.org/wiki/CommitTicketUpdater">Commit Ticket Updater Plugin</a> aktiviert.</p>
<p>Trac erkennt dadurch eine bestimmte Syntax in den Kommentaren, die  auf der Wiki-Seite des Plugins erläutert ist, und fügt einen Verweis in den Kommentaren zum jeweiligen Ticket ein.</p>
<p>Beispiel:<br />
- Behebe Darstellungsfehler in der Tabellen-Komponente. See #8, #9, #11<br />
- Korrigiere Syntaxfehler. Fix #4<br />
- Neue Methode zum Rotieren von Bildern dazu. See #18 and #19</p>
<p>Das Ergebnis sieht dann z.B. so aus:</p>
<p><img class="alignnone size-full wp-image-448" title="CommitTicketUpdater" src="http://studium.coderbyheart.de/wp-content/uploads/2011/03/CommitTicketUpdater.png" alt="" width="507" height="234" /></p>
<p>Der große Vorteil davon ist, dass man zu jedem Commit automatisch den Verweis auf das Ticket mit der Aufgabenbeschreibung hat und in jedem Ticket die Commit-History zu sehen ist.</p>
<p>Mit der Mylyn-Integration von Trac bekommt man dann auch fremde Commits an seinen eigenen Tickets mit. </p>
