---
layout: post
status: publish
published: true
title: Dynamische Klassendiagramme mit GraphViz
author:
  display_name: Markus Tacker
  login: m
  email: m@tacker.org
  url: http://tckr.cc/
author_login: m
author_email: m@tacker.org
author_url: http://tckr.cc/
wordpress_id: 970
wordpress_url: http://studium.coderbyheart.de/?p=970
date: '2012-02-29 12:46:43 +0100'
date_gmt: '2012-02-29 10:46:43 +0100'
categories:
- Uncategorized
tags:
- SoftwareTechnik
- uml
- graphviz
- dot
comments: []
---
<p>In der Regel will man Klassendiagramme in Dokumentationen synchron zu einem sich ändernden Quellcode halten. Der manuelle Weg ist einfach, aber nervig. Schöner ist es da doch, wenn man UML-Diagramme programmatisch erzeugen kann. Ein Dienst, der das ermöglich ist <a href="http://yuml.me/">yUML.me</a>, allerdings hat diese Engine einige Bugs, die selbst schon bei kleine Diagrammen auftreten und den Dienst damit unbenutzbar machen.</p>
<p>Für einfachere Klassendiagramme kann man aber auch <a href="http://www.graphviz.org/">GraphViz</a> missbrauchen. Dazu eignet sich der <a href="http://www.graphviz.org/doc/info/shapes.html">Knoten-Typ record</a>, bei dem mit Hilfe des Pipe-Symbols „|“ innerhalb des Namens des Knotens Felder definiert werden können.</p>
<p>Um die Klasse Meeting im Diagramm unten zu erzeugen, verwende ich diesen Text im Label des Knotens (siehe auch Zeile 4 im Quellcode unten): </p>
<pre>{Meeting|+name\l+flags\l+creation_date\l}</pre>
<p> <br />
Das „\l“ bewirkt einen linksbündigen Umbruch (standardmäßig werden Labels in Knoten zentriert dargestellt).</p>
<p><img class="alignnone size-medium wp-image-986" title="Klassendiagramm erstellt in GraphViz / Dot" src="http://studium.coderbyheart.de/wp-content/uploads/2012/02/models-500x472.png" alt="Klassendiagramm erstellt in GraphViz / Dot" width="500" height="472" /></p>
<p>Der gesamte Quellcode für dieses Diagramm ist extrem kompakt und lässt sich prima aus Klassen-Informationen generieren:</p>
<pre>digraph G {
graph [ rankdir=BT ]
node [ shape=record ]
Meeting [label="{Meeting|+name\l+flags\l+creation_date\l}"]
User [label="{User|+ip\l+creation_date\l}"]
Topic [label="{Topic|+meeting\l+name\l+image\l+creation_date\l}"]
Comment [label="{Comment|+topic\l+user\l+comment\l+creation_date\l}"]
Question [label="{Question|+topic\l+name\l+type\l+mode\l+creation_date\l}"]
QuestionOption [label="{QuestionOption|+question\l+key\l+value\l+creation_date\l}"]
Choice [label="{Choice|+question\l+name\l+creation_date\l}"]
Answer [label="{Answer|+question\l+user\l+answer\l+creation_date\l}"]
edge [ arrowhead=none headlabel="1" taillabel="0..n" fontsize=10 ]
Topic -&gt; Meeting
Comment -&gt; Topic
Comment -&gt; User
Question -&gt; Topic
QuestionOption -&gt; Question
Choice -&gt; Question
Answer -&gt; Question
Answer -&gt; User
}</pre>
