---
layout: post
permalink: what-the-foto-tickettree
title: 'What The Foto: TicketTree'
excerpt: "<a href=\"http://www.flickr.com/photos/tacker/sets/72157626379556132/\"><img
  class=\"alignright\" src=\"http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg\"
  alt=\"What The Foto?\" /></a>Eine meiner eher wenig nützlichen Ideen für das Projekt
  war eine Wiki-Seite, die die Tickets in Form eines Baumes auflistet.\r\n"
date: '2011-08-05 06:00:32 +0200'
tags:
- SoftwareTechnik
---
<p><a href="http://www.flickr.com/photos/tacker/sets/72157626379556132/"><img class="alignright" src="http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg" alt="What The Foto?" /></a>Eine meiner eher wenig nützlichen Ideen für das Projekt war eine Wiki-Seite, die die Tickets in Form eines Baumes auflistet.</p>

Man konnte in der Beschreibung eines Tickets das Tag

    @depends Ticket 1[, Ticket 2[, ...]]
    
einfügen.

<p>Mit <a href="{{ '/svn/WTF/tickettree/TicketTree.py' | prepend: site.baseurl | prepend: site.url }}">diesem Script</a> habe ich dann alle Tickets nach dem Tag durchsucht und daraus eine Wiki-Seite erzeugt, die diese Abhängigkeiten visualisiert.</p>
<p>Leider ist <a href="http://www.flickr.com/photos/tacker/5983778399/sizes/o/in/photostream/">das Ergebnis</a> eher weniger nützlich.</p>
<p>Übrigens verfügt auch Trac selber <a href="http://trac.edgewall.org/wiki/ticket/31">immer noch nicht</a> über eine Funktion, mit der das möglich ist. Ein gutes Beispiel wie sowas aussehen kann, <a href="http://www.redmine.org/projects/redmine/wiki/RedmineIssues#Related-issues">ist in Redmine implementiert</a>.</p>
