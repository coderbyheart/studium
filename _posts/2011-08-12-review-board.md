---
layout: post
title: Review Board
excerpt: "Für das <a href=\"/tag/WhatTheFoto\">Softwaretechnik-Projekt</a>
  hatte ich nach eine Möglichkeit gesucht, komfortable Code-Reviews zu machen. Mein
  Professor ist dann auf <a href=\"http://www.reviewboard.org/\">Review Board</a>
  gestoßen.\r\n"
date: '2011-08-12 06:00:58 +0200'
tags:
- SoftwareTechnik
- WhatTheFoto
---
<p>Für das <a href="/tag/WhatTheFoto">Softwaretechnik-Projekt</a> hatte ich nach eine Möglichkeit gesucht, komfortable Code-Reviews zu machen. Mein Professor ist dann auf <a href="http://www.reviewboard.org/">Review Board</a> gestoßen.<br />
<a id="more"></a><a id="more-628"></a></p>
<blockquote><p>Review Board is a powerful web-based code review tool that offers developers an easy way to handle code reviews. It scales well from small projects to large companies and offers a variety of tools to take much of the stress and time out of the code review process.</p></blockquote>
<p>Auf den ersten Blick hört sich das natürlich toll an.</p>
<p>Beim tatsächlichen Einsatz haben sich dann aber große Nachteile herauskristallisiert:</p>
<p>Zum einen ist es ein großes Problem, ein Tool zu verwenden, dass <em>neben</em> dem SCM-Tool (in unserem Fall <a href="trac.edgewall.org">Trac</a>) läuft. Trac bietet einen tollen Quellcode-Browser, und ist natürlich auch die Stelle, an der Diskussionen rund um das Projekt führt. Lagert man nun einen Teil der Diskussion aus in ein anderes Tool, muss man ständig die Stati aus Review Board wieder manuell in Trac eintragen &mdash; das geht praktisch nie gut.</p>
<p>Zum anderen ist Review Board ein Alptraum, wenn es um die Bedienung geht. Es gibt so viele nicht intuitive Micro-Workflows die beachtet werden müssen, dass es keinen Spaß macht, mit dem Tool zu arbeiten &mdash; selbst wenn die Funktionaliät wirklich ausgesprochen gut ist.</p>
<h3 class="textimage">Fazit</h3>
<p>Es braucht also ein SCM-Tool, dass neben dem reinen Quellcode-Browsen dort direkt auch die Möglichkeit bietet, den Quellcode zu kommentieren. Wie eine intuitive Implementierung aussehen könnte, zeigt <a href="http://github.com/">GitHub</a>.</p>
<p><a href="/uploads/2011/08/git-code-comments.png"><img src="/uploads/2011/08/git-code-comments-500x233.png" alt="" title="Quellcode-Kommentare mit GitHub" width="500" height="233" class="alignnone size-medium wp-image-785" /></a></p>
