---
layout: post
status: publish
published: true
title: Was ich an Django so mag
author:
  display_name: Markus Tacker
  login: m
  email: m@tacker.org
  url: http://tckr.cc/
author_login: m
author_email: m@tacker.org
author_url: http://tckr.cc/
wordpress_id: 906
wordpress_url: /?p=906
date: '2012-01-27 09:45:51 +0100'
date_gmt: '2012-01-27 07:45:51 +0100'
categories:
- Uncategorized
tags:
- python
- mobile computing
comments:
- id: 169
  author: Dennis Oehme
  author_email: do@dennis-oehme.de
  author_url: ''
  date: '2012-01-27 18:19:13 +0100'
  date_gmt: '2012-01-27 16:19:13 +0100'
  content: Klingt sehr interessant und bin gespannt auf deine weiteren Erfahrungswerte,
    vor allem bei Themen der Flexibilität und Erweiterbarkeit. Die CRUD-Mechanismen,
    die z.B. Rails und scheinbar auch Django bieten, sehe als ein zweischneidiges
    Schwert. Auf der einen Seite ermöglicht es anfänglich eine enorm schnelle Entwicklung
    zu einem an sich funktionierendem System. Die Kehrseite ist jedoch, dass im Verlauf
    der Entwicklung View/Controller/Model i.d.R. doch soweit angepasst bzw. doch explizit
    implementiert werden (müssen), dass die anfängliche Zeiteinsparung im Endeffekt
    wieder verloren geht.
- id: 170
  author: Markus Tacker
  author_email: m@tacker.org
  author_url: http://studium.coderbyheart.de/
  date: '2012-01-27 18:27:36 +0100'
  date_gmt: '2012-01-27 16:27:36 +0100'
  content: "Da stimme ich dir voll zu. Man muss ganz klar sagen, dass Django explizit
    darauf ausgerechtet ist diese Basis-Operationen in einer contentlastigen Website
    zu automatisieren. \n\n<blockquote>Developed by a fast-moving online-news operation,
    Django was designed to handle two challenges: the intensive deadlines of a newsroom
    and the stringent requirements of the experienced Web developers who wrote it.
    It lets you build high-performing, elegant Web applications quickly.</blockquote>\n\nWenn
    man eine komplexere Webanwendung mit komplizierteren Businesslogiken hat, stößt
    man mit Django mit Sicherheit relativ schnell an eine Grenze &mdash; dafür fehlt
    es ganz klar auch an der Möglichkeit, Anwendungen wie in Symfony2, Modular auf
    zu bauen. Unter <a href=\"http://www.djangosites.org/\" rel=\"nofollow\">djangosites.org</a>
    findet sich ein große Liste an Referenz-Projekten."
- id: 192
  author: Projektergebnis Mobile Computing &laquo; Markus studiert!
  author_email: ''
  author_url: http://studium.coderbyheart.de/projektergebnis-mobile-computing
  date: '2012-02-22 16:42:54 +0100'
  date_gmt: '2012-02-22 14:42:54 +0100'
  content: "[...] umgesetzt. Auch das hat mir einige „OMG! Wie geil!“-Momente, über
    die habe ich aber schon an anderer Stelle [...]"
---
<p>Nachdem ich im dritten Semester zum ersten Mal intensiveren Kontakt mit Python hatte, habe ich die Sprache in den vergangenen Semestern immer stärker schätzen gelernt.</p>
<p>In diesem Semester setzen wir für die Server-Komponente unseres Mobile-Computing-Projekts ebenfalls auf Python, und zwar in Form des Web-Frameworks <a href="https://www.djangoproject.com/">Django</a>. Und das ist wirklich ein Genuss.</p>
<p>Zur Implementierung des Servers lieferte Django bereits alle notwendigen Komponenten. Das Framework bietet den besonderen Vorteil, dass die typischen Aufgaben einer Webanwendung, deren Hauptaufgabe die Verwaltung von Datensätzen ist, also deren Auflisten, Anzeigen, Finden und Editieren (CRUD), nach Erstellung von nur wenig eigenem Code bereits komfortabel zur Verfügung stehen. Es muss lediglich die Datenstruktur in Form von Models definiert werden. Anhand dieser Informationen kann Djongo schon die nötige Datenbankstruktur erzeugen und passende Formulare zum Editieren der Datensätze im mitgelieferten Admin-Bereich erzeugen.</p>
<p>Zur Implementierung der öffentlichen Schnittstellen der Anwendung reichen auch lediglich wenige Zeile Code aus. In Django werden diese mithilfe der Views erstellt, wobei man hier nur Ausnahmen behandeln muss, die über das Anzeigen von einzelnen Datensätzen oder Listen von Datensätzen hinaus gehen. Die für die App zur Verfügung gestellt API wird ebenfalls mit Hilfe der Views erzeugt, wobei dann das Antwort-Format nicht HTML ist, sondern JSON. Die Unterscheidung wird anhand das Accept-Headers in der Anfrage getroffen. Um die Implementierung eines eigenen Controllers muss man sich nicht kümmern, hier übernimmt das Framework bereits alle nötigen Aufgaben, sofern man die vorgegebenen Konventionen befolgt und die bereitgestellten Hilfsfunktionen verwendet.</p>
<p>Auch die Möglichkeit zum Testen seiner Anwendung sind genial, das Test-Framework kümmert sich um alle Aufgaben, lediglich die Unit-Tests muss man selber schreiben - was elegant von der Hand geht, dank einem mitgelieferten Test-Client der URL-Request simuliert.</p>
<p>Django nimmt einem durch viele Konventionen unheimlich viel Arbeit ab, und man kann sich auf das Wesentliche konzentrieren. Die Geschwindigkeit, mit der man in Django entwickeln kann ist beeindruckend und ich bin schwer am Überlegen, es auch für meine Thesis ein zu setzen...</p>
