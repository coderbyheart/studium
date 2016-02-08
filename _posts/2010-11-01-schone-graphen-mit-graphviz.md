---
layout: post
title: Schöne Graphen mit GraphViz
excerpt: "<a href=\"http://www.graphviz.org/\">Graphviz</a> ist ein tolles Tool, mit
  dessen Hilfe man mit wenig Quellcode dynamische Graphen erzeugen kann, die sich
  für vielerlei Arten von Visualisierungen verwenden lassen &mdash; unter anderem
  auch in Automatentheorie und formale Sprachen ...\r\n"
date: '2010-11-01 15:51:26 +0100'
tags:
- AFS
- graphviz
- dot
---
<p><a href="http://www.graphviz.org/">Graphviz</a> ist ein tolles Tool, mit dessen Hilfe man mit wenig Quellcode dynamische Graphen erzeugen kann, die sich für vielerlei Arten von Visualisierungen verwenden lassen &mdash; unter anderem auch in Automatentheorie und formale Sprachen ...<br />
<a id="more"></a><a id="more-358"></a></p>
<h3 class="textimage">Beispiel</h3>
<p>[cc lang="dot"]<br />
digraph g {<br />
rankdir=LR<br />
node [shape=circle]<br />
S0 [shape=doublecircle ]<br />
S1 [shape=doublecircle ]<br />
S2 [shape=doublecircle ]<br />
S0 -> S1 [ label=b ]<br />
S0 -> S0 [ label=a ]<br />
S1 -> S0 [ label=a weight=.01 ]<br />
S1 -> S2 [ label=b ]<br />
S2 -> S0 [ label=a weight=.01 ]<br />
S2 -> f [ label=b ]<br />
f -> f [ label="a,b" ]<br />
}<br />
[/cc]</p>
<p>Der resultierende Graph sieht so aus:</p>
<p><img src="http://farm2.static.flickr.com/1107/5136020436_4c1ba8097c.jpg" alt="" /></p>
