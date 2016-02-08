---
layout: post
status: publish
published: true
title: 'What The Foto: TicketTree'
author:
  display_name: Markus Tacker
  login: m
  email: m@tacker.org
  url: http://tckr.cc/
author_login: m
author_email: m@tacker.org
author_url: http://tckr.cc/
excerpt: "<a href=\"http://www.flickr.com/photos/tacker/sets/72157626379556132/\"><img
  class=\"alignright\" src=\"http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg\"
  alt=\"What The Foto?\" /></a>Eine meiner eher wenig nützlichen Ideen für das Projekt
  war eine Wiki-Seite, die die Tickets in Form eines Baumes auflistet.\r\n"
wordpress_id: 703
wordpress_url: /?p=703
date: '2011-08-05 06:00:32 +0200'
date_gmt: '2011-08-05 04:00:32 +0200'
categories:
- Uncategorized
tags:
- SoftwareTechnik
comments: []
---
<p><a href="http://www.flickr.com/photos/tacker/sets/72157626379556132/"><img class="alignright" src="http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg" alt="What The Foto?" /></a>Eine meiner eher wenig nützlichen Ideen für das Projekt war eine Wiki-Seite, die die Tickets in Form eines Baumes auflistet.<br />
<a id="more"></a><a id="more-703"></a><br />
Man konnte in der Beschreibung eines Tickets das Tag<br />
[cc]@depends Ticket 1[, Ticket 2[, ...]][/cc]<br />
einfügen.</p>
<p>Mit <a href="/svn/WTF/tickettree/TicketTree.py">diesem Script</a> habe ich dann alle Tickets nach dem Tag durchsucht und daraus eine Wiki-Seite erzeugt, die diese Abhängigkeiten visualisiert.</p>
<p>Leider ist <a href="http://www.flickr.com/photos/tacker/5983778399/sizes/o/in/photostream/">das Ergebnis</a> eher weniger nützlich.</p>
<p>Übrigens verfügt auch Trac selber <a href="http://trac.edgewall.org/wiki/ticket/31">immer noch nicht</a> über eine Funktion, mit der das möglich ist. Ein gutes Beispiel wie sowas aussehen kann, <a href="http://www.redmine.org/projects/redmine/wiki/RedmineIssues#Related-issues">ist in Redmine implementiert</a>.</p>
