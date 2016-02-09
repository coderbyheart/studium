---
layout: post
permalink: schone-graphen-mit-graphviz
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
[Graphviz](http://www.graphviz.org/) ist ein tolles Tool, mit dessen Hilfe man mit wenig Quellcode dynamische Graphen erzeugen kann, die sich für vielerlei Arten von Visualisierungen verwenden lassen &mdash; unter anderem auch in Automatentheorie und formale Sprachen ...

<h3 class="textimage">Beispiel</h3>

    digraph g {
    rankdir=LR
    node [shape=circle]
    S0 [shape=doublecircle ]
    S1 [shape=doublecircle ]
    S2 [shape=doublecircle ]
    S0 -> S1 [ label=b ]
    S0 -> S0 [ label=a ]
    S1 -> S0 [ label=a weight=.01 ]
    S1 -> S2 [ label=b ]
    S2 -> S0 [ label=a weight=.01 ]
    S2 -> f [ label=b ]
    f -> f [ label="a,b" ]
    }

Der resultierende Graph sieht so aus:

![dot Graph](http://farm2.static.flickr.com/1107/5136020436_4c1ba8097c.jpg)
